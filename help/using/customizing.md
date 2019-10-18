---
title: Personalización de componentes principales
seo-title: Personalización de componentes principales
description: Los componentes principales implementan varios patrones que permiten una fácil personalización, desde el estilo simple hasta la reutilización avanzada de la funcionalidad.
seo-description: Los componentes principales de AEM implementan varios patrones que facilitan la personalización, desde el estilo simple hasta la reutilización de funciones avanzadas.
uuid: 38d22b85-4867-4716-817a-10ee2f8de6f5
contentOwner: User
content-type: reference
topic-tags: desarrollo
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3c9e0ade-1ce0-4e34-ae04-8da63f9b6c4f
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Personalización de componentes principales{#customizing-core-components}

Los componentes [](developing.md) principales implementan varios patrones que permiten una fácil personalización, desde el estilo simple hasta la reutilización avanzada de la funcionalidad.

## Arquitectura flexible {#flexible-architecture}

Los componentes principales fueron diseñados desde el principio para ser flexibles y ampliables. Un vistazo a una visión general de su arquitectura revela dónde se pueden realizar las personalizaciones.

![Arquitectura de componentes principales](assets/screen_shot_2018-12-07at093742.png)

* [El cuadro de diálogo](authoring.md#edit-and-design-dialogs) de diseño define qué pueden o no pueden hacer los autores en el cuadro de diálogo de edición.
* [El cuadro de diálogo](authoring.md#edit-and-design-dialogs) de edición muestra a los autores solo las opciones que pueden utilizar.
* [El modelo](#customizing-the-logic-of-a-core-component) Sling comprueba y prepara el contenido para la vista (plantilla).
* [El resultado del modelo](#customizing-the-logic-of-a-core-component) Sling se puede serializar en JSON para casos de uso de SPA.
* [El HTL procesa el servidor HTML](#customizing-the-markup) para el procesamiento tradicional en el servidor.
* [El resultado](#customizing-the-markup) HTML es semántico, accesible, optimizado para motores de búsqueda y de estilo sencillo.

Y todos los componentes principales implementan el Sistema [de estilos](customizing.md).

## Tipo de archivo del proyecto AEM {#aem-project-archetype}

[El arquetipo](overview.md) de proyecto de AEM crea un proyecto mínimo de Adobe Experience Manager como punto de partida para sus propios proyectos, incluido un ejemplo práctico del componente HTL personalizado con SlingModels para la lógica y la correcta implementación de los componentes principales con el patrón proxy recomendado.

## Patrones de personalización {#customization-patterns}

### Personalización de cuadros de diálogo {#customizing-dialogs}

Es posible que desee personalizar las opciones de configuración disponibles en un cuadro de diálogo de componentes principales, ya sea el cuadro de diálogo [Diseño o el cuadro de diálogo](authoring.md)Editar.

Cada cuadro de diálogo tiene una estructura de nodos consistente. Se recomienda que esta estructura se replique en un componente heredado para que se puedan usar las [fusiones](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) de recursos de Sling y las condiciones de [](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) ocultación para ocultar, reemplazar o reordenar secciones del cuadro de diálogo original. La estructura que se va a replicar se define como cualquier elemento hasta el nivel de nodo de elemento de ficha.

Para ser totalmente compatible con cualquier cambio realizado en un cuadro de diálogo en su versión actual, es muy importante que no se toquen las estructuras situadas debajo del nivel de elemento de ficha (ocultado, agregado, sustituido, reordenado, etc.). En su lugar, se debe ocultar un elemento de ficha del elemento principal mediante la `sling:hideResource` propiedad (consulte [Sling Resource Merger Properties](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)) y se deben agregar nuevos elementos de ficha que contengan los campos de configuración personalizados. `sling:orderBefore` se puede utilizar para reordenar elementos de ficha si es necesario.

El cuadro de diálogo siguiente muestra la estructura de cuadro de diálogo recomendada, así como cómo ocultar y reemplazar una ficha heredada como se describe anteriormente:

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
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### Personalización de la lógica de un componente principal {#customizing-the-logic-of-a-core-component}

La lógica empresarial de los componentes principales se implementa en los modelos de Sling. Esta lógica se puede ampliar utilizando un patrón de delegación de Sling.

Por ejemplo, el componente principal del título utiliza la `jcr:title` propiedad del recurso solicitado para proporcionar el texto del título. Si no se define ninguna `jcr:title` propiedad, se implementa una alternativa al título de la página actual. Queremos cambiar el comportamiento para que siempre se muestre el título de la página actual.

Dado que la implementación de los modelos de componentes principales es privada, deben ampliarse con un patrón de delegación.

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

Para obtener más información sobre el patrón de delegación, consulte el artículo sobre los componentes principales de GitHub Wiki [Patrón de delegación para modelos](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models)Sling.

### Personalización del marcado {#customizing-the-markup}

A veces, el estilo avanzado requiere una estructura de marcado diferente del componente.

Esto se puede hacer fácilmente copiando los archivos HTML que deben modificarse del componente principal al componente proxy.

Tomando de nuevo el ejemplo del componente Core Breadcrumb, para personalizar su salida de marcado, el `breadcrumb.html` archivo tendría que copiarse en el componente específico del sitio que tiene un `sling:resourceSuperTypes` que apunta al componente Core Breadcrumb.

### Estilo de los componentes {#styling-the-components}

La primera forma de personalización consiste en aplicar estilos CSS.

Para facilitar esto, los Componentes principales procesan el marcado semántico y siguen una convención de nombres estandarizada inspirada en [Bootstrap](https://getbootstrap.com/). Además, para establecer fácilmente como objetivo y como espacio de nombres los estilos de los componentes individuales, cada componente principal se envuelve en un elemento DIV con las clases " `cmp`" y " `cmp-<name>`".

Por ejemplo, mirando el archivo HTL del componente Core Breadcrumb v1: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que la salida de jerarquía de elementos es `ol.breadcrumb > li.breadcrumb-item > a`. Para asegurarse de que una regla CSS solo afecta a la clase breadcrumb de ese componente, todas las reglas deben tener un espacio de nombres como se muestra a continuación:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Además, cada uno de los componentes principales aprovecha la función [AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) Style System que permite a los autores de plantillas definir nombres de clase CSS adicionales que los autores de la página pueden aplicar al componente. Esto permite definir para cada plantilla una lista de estilos de componente permitidos y si uno de ellos debe aplicarse de forma predeterminada a todos los componentes de ese tipo.

## Compatibilidad de actualización de personalizaciones {#upgrade-compatibility-of-customizations}

Se pueden realizar tres tipos diferentes de actualizaciones:

* actualización de la versión de AEM
* actualización de los componentes principales a una nueva versión secundaria
* actualización de los componentes principales a una versión principal

En general, la actualización de AEM a una nueva versión no afectará a los componentes principales ni a las personalizaciones realizadas, siempre que las versiones de los componentes también admitan la nueva versión de AEM a la que se está migrando y que las personalizaciones no utilicen API que se hayan [desaprobado o eliminado](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

La actualización de los componentes principales sin cambiar a una versión principal más reciente no debería afectar a las personalizaciones, siempre que se utilicen los patrones de personalización descritos en esta página.

El cambio a una versión principal más reciente de los componentes principales solo es compatible con la estructura de contenido, pero es posible que sea necesario refactorizar las personalizaciones. Se publicarán registros de cambios claros para cada versión del componente a fin de resaltar los cambios que podrían afectar al tipo de personalizaciones descritas en esta página.

## Compatibilidad con personalizaciones {#support-of-customizations}

Al igual que para cualquier componente de AEM, hay que tener en cuenta varias cosas en relación con las personalizaciones:

1. **Nunca modifique directamente el código de los componentes principales.**

   Esto haría que no fueran totalmente compatibles y que las futuras actualizaciones de los componentes fueran un proceso doloroso. En su lugar, utilice los métodos de personalización descritos en esta página.

1. **El código personalizado es su propia responsabilidad.**

   Nuestro programa de soporte no cubre el código personalizado, y los problemas informados que no pueden reproducirse con los componentes principales de vainilla que se [utilizan como documentados](using.md) no serán válidos.

1. **Observar la funcionalidad obsoleta y eliminada.**

   Al actualizar cada nueva versión de AEM, asegúrese de que todas las API utilizadas siguen teniendo actualidad, vigilando la página Funciones [](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html) obsoletas y eliminadas.

Consulte también la sección Compatibilidad con [](developing.md#core-component-support) componentes principales.

**Consulte lo siguiente:**

* [Uso de componentes](using.md) principales: obtenga y ejecute los componentes principales en su propio proyecto.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
