---
title: Personalización de componentes principales
description: Los Componentes principales implementan varios patrones que facilitan la personalización, desde un estilo sencillo hasta la reutilización avanzada de funcionalidades.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: bd688d422a072a9d5627c27817ac67f95829de4f
workflow-type: ht
source-wordcount: '1041'
ht-degree: 100%

---

# Personalización de componentes principales{#customizing-core-components}

Los [Componentes principales](overview.md) implementan varios patrones que facilitan la personalización, desde un estilo sencillo hasta la reutilización avanzada de funcionalidades.

## Arquitectura flexible {#flexible-architecture}

Los componentes principales se diseñaron desde el principio para que fueran flexibles y ampliables. Un vistazo a una descripción general de su arquitectura revelará dónde se pueden realizar las personalizaciones.

![Arquitectura de componentes principales](/help/assets/screen_shot_2018-12-07at093742.png)

* [El cuadro de diálogo de diseño](/help/get-started/authoring.md#edit-and-design-dialogs) define qué pueden hacer o no los autores en el cuadro de diálogo de edición.
* [El cuadro de diálogo de edición](/help/get-started/authoring.md#edit-and-design-dialogs) muestra a los autores solo las opciones que pueden utilizar.
* [El modelo Sling](#customizing-the-logic-of-a-core-component) comprueba y prepara el contenido para la vista (plantilla).
* [El resultado del modelo Sling](#customizing-the-logic-of-a-core-component) se puede serializar en JSON para casos de uso SPA.
* [HTL procesa el HTML](#customizing-the-markup) del lado del servidor para un procesamiento tradicional del lado del servidor.
* [La salida HTML](#customizing-the-markup) es semántica, accesible, optimizada para motores de búsqueda y fácil de diseñar.

Y todos los componentes principales implementan el [Sistema de estilos](#styling-the-components).

## Tipo de archivo del proyecto AEM {#aem-project-archetype}

[El archivo del proyecto de AEM](/help/developing/archetype/overview.md) procesa un proyecto mínimo de Adobe Experience Manager como punto de partida para sus propios proyectos, incluido un ejemplo del componente HTL personalizado con modelos Sling para la lógica y la correcta implementación de los componentes principales con el patrón de proxy recomendado.

## Patrones de personalización {#customization-patterns}

### Personalización de cuadros de diálogo {#customizing-dialogs}

Puede que quiera personalizar las opciones de configuración disponibles en un cuadro de diálogo de componentes principales, ya sea el [Cuadro de diálogo de diseño o el cuadro de diálogo de edición](/help/get-started/authoring.md).

Cada cuadro de diálogo tiene una estructura de nodos coherente. Se recomienda que esta estructura se duplique en un componente heredado para que la [Fusión de recursos Sling](https://helpx.adobe.com/es/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) y [Ocultar condiciones](https://experienceleague.adobe.com/docs/experience-manager-65/developing/components/hide-conditions.html?lang=es) se puedan usar para ocultar, reemplazar o reordenar secciones del cuadro de diálogo original. La estructura que se va a replicar se define como cualquier elemento hasta el nivel de nodo de elemento de pestaña.

Para ser totalmente compatible con los cambios realizados en un cuadro de diálogo en su versión actual, es muy importante que las estructuras por debajo del nivel del elemento de pestaña no se toquen (oculten, agreguen, sustituyan, reordenen, etc.). En lugar de eso, se debe ocultar un elemento de pestaña del elemento principal mediante la propiedad `sling:hideResource` (consulte [Propiedades de la fusión de recursos Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=es)) y se deben agregar nuevos elementos de pestaña que contengan los campos de configuración personalizados. `sling:orderBefore` se puede utilizar para reordenar los elementos de la pestaña si es necesario.

El siguiente cuadro de diálogo muestra la estructura de diálogo recomendada, así como cómo ocultar y reemplazar una pestaña heredada, tal como se describe anteriormente:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container">
                                  
                               <!-- myTab content -->
                                  
                        </myTab>
                </items>
            </tabs>
        </items>
    </content>
</jcr:root>
```

### Personalización de la lógica de un componente principal {#customizing-the-logic-of-a-core-component}

La lógica empresarial de los componentes principales se implementa en los modelos Sling. Esta lógica se puede ampliar utilizando un patrón de delegación Sling.

Por ejemplo, el componente principal del título utiliza la propiedad `jcr:title` del recurso solicitado para proporcionar el texto del título. Si no se define ninguna propiedad `jcr:title`, se implementará una alternativa al título de la página actual. Debemos cambiar el comportamiento para que el título de la página actual se muestre siempre.

Dado que la implementación de los modelos de los componentes principales es privada, deben ampliarse con un patrón de delegación.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    
    @ScriptVariable private Page currentPage;
    
    @Self @Via(type = ResourceSuperType.class)

    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    
    @Override public String getType() {
        return title.getType();
    }
}
```

Para obtener más información sobre el patrón de delegación, consulte el artículo de la wiki de los componentes principales de GitHub [Patrón de delegación para modelos Sling](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Personalización del marcado {#customizing-the-markup}

A veces, el estilo avanzado requiere una estructura de marcado diferente del componente.

Esto se puede hacer fácilmente copiando los archivos HTL que necesitan modificarse del componente principal al [componente proxy.](guidelines.md#proxy-component-pattern)

Siguiendo de nuevo el ejemplo del componente de ruta de exploración principal, para personalizar su salida de marcado, el archivo `breadcrumb.html` tendría que copiarse en el componente específico del sitio que tenga un `sling:resourceSuperTypes` que apunte al componente de ruta de exploración principal.

### Diseño de los componentes {#styling-the-components}

La primera forma de personalización es aplicar estilos CSS.

Para facilitar esto, los componentes principales procesan el marcado semántico y siguen una convención de nombres estandarizada inspirada en [Bootstrap](https://getbootstrap.com/). Además, para establecer fácilmente como objetivo y espacio de nombres los estilos para los componentes individuales, cada componente principal se envuelve en un elemento DIV con las clases &quot;`cmp`&quot; y &quot;`cmp-<name>`&quot;.

Por ejemplo, observe el archivo HTL del componente de ruta de exploración principal versión 1: [ruta.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que la salida de la jerarquía de elementos es `ol.breadcrumb > li.breadcrumb-item > a`. Por lo tanto, para asegurarse de que una regla CSS solo afecta a la clase de ruta de exploración de ese componente, todas las reglas deben tener un espacio de nombres como se muestra a continuación:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Además, cada uno de los componentes principales aprovecha la función de AEM [Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=es) que permite a los autores de plantillas definir nombres de clase CSS adicionales que los autores de la página pueden aplicar al componente. Esto permite definir para cada plantilla una lista de estilos de componente permitidos y si uno de ellos debe aplicarse de forma predeterminada a todos los componentes de ese tipo.

## Compatibilidad de la actualización de las personalizaciones {#upgrade-compatibility-of-customizations}

Se pueden realizar tres tipos diferentes de actualizaciones:

* actualizar la versión de AEM
* actualizar los componentes principales a una nueva versión secundaria
* actualizar los componentes principales a una versión principal

Por lo general, actualizar AEM a una nueva versión no afectará a los componentes principales ni a las personalizaciones realizadas, siempre que las versiones de los componentes también admitan la nueva versión de AEM a la que se está migrando y que las personalizaciones no utilicen API [obsoletas o eliminadas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=es).

La actualización de los componentes principales sin cambiar a una versión principal más reciente no debería afectar a las personalizaciones, siempre y cuando se utilicen los patrones de personalización descritos en esta página.

El cambio a una versión principal más reciente de los componentes principales solo es compatible con la estructura de contenido, pero es posible que sea necesario refactorizar las personalizaciones. Se publicarán registros de cambios claros para cada versión del componente a fin de resaltar los cambios que podrían afectar al tipo de personalizaciones descritas en esta página.

## Compatibilidad con personalizaciones {#support-of-customizations}

Al igual que para cualquier componente de AEM, hay que tener en cuenta varias cosas sobre las personalizaciones:

1. **Nunca modifique directamente el código de los componentes principales.**

   De este modo, no se admitirían por completo y las futuras actualizaciones de los componentes se convertirían en un proceso doloroso. En lugar de eso, utilice los métodos de personalización descritos en esta página.

1. **El código personalizado es su propia responsabilidad.**

   Nuestro programa de asistencia no se responsabiliza del código personalizado y los problemas notificados que no se puedan reproducir con los componentes principales de vainilla que se [usan como documentados](/help/get-started/using.md) no se califican.

1. **Vea las funciones obsoletas y eliminadas.**

   Con cada versión de AEM nueva a la que se actualiza, asegúrese de que todas las API utilizadas sigan actualizadas, teniendo en cuenta la página [Funciones obsoletas y eliminadas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=es).

Consulte también la sección [Compatibilidad con componentes principales](overview.md#core-component-support).

**Consulte lo siguiente:**

* [Uso de componentes principales](/help/get-started/using.md): ponga en marcha los componentes principales con sus propios proyectos.
* [Directrices de componentes](guidelines.md): para conocer los patrones de implementación de los componentes principales.
