---
title: Personalización de componentes principales
seo-title: Personalización de componentes principales
description: Los componentes principales implementan varios patrones que facilitan la personalización, desde un estilo simple a una reutilización de funcionalidad avanzada.
seo-description: Los componentes de AEM Core implementan varios patrones que facilitan la personalización, desde un estilo simple a una reutilización de funcionalidad avanzada.
uuid: 38 d 22 b 85-4867-4716-817 a -10 ee 2 f 8 de 6 f 5
contentOwner: Usuario
content-type: referencia
topic-tags: desarrollar
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 c 9 e 0 ade -1 ce 0-4 e 34-ae 04-8 da 63 f 9 b 6 c 4 f
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Personalización de componentes principales{#customizing-core-components}

Los componentes [principales](developing.md) implementan varios patrones que facilitan la personalización, desde un estilo simple a una reutilización de funcionalidad avanzada.

## Arquitectura flexible {#flexible-architecture}

Los componentes principales se diseñaron desde el principio para ser flexibles y extensibles. Un vistazo a una descripción general de su arquitectura revela dónde se pueden personalizar.

![Arquitectura de componentes principales](assets/screen_shot_2018-12-07at093742.png)

* [El cuadro de diálogo](authoring.md#edit-and-design-dialogs) de diseño define lo que los autores pueden o no hacer en el cuadro de diálogo de edición.
* [El cuadro de diálogo](authoring.md#edit-and-design-dialogs) de edición muestra a los autores únicamente las opciones que pueden utilizar.
* [El modelo Sling](#customizing-the-logic-of-a-core-component) comprueba y prepara el contenido para la vista (plantilla).
* [El resultado del modelo Sling](#customizing-the-logic-of-a-core-component) se puede serializar en JSON para casos de uso de SPA.
* [HTL procesa HTML](#customizing-the-markup) en el lado del servidor para la representación tradicional del lado del servidor.
* [El resultado HTML](#customizing-the-markup) es semántica, accesible, motor de búsqueda optimizado y fácil de diseñar.

Y todos los componentes principales implementan el [sistema de estilos](customizing.md).

## Patrones de personalización {#customization-patterns}

### Personalización de diálogos {#customizing-dialogs}

Puede que desee personalizar las opciones de configuración disponibles en un cuadro de diálogo de componente principal, ya sea en el cuadro de diálogo [de diseño o en el cuadro de diálogo Editar](authoring.md).

Cada cuadro de diálogo tiene una estructura de nodos coherente. Se recomienda que esta estructura se repita en un componente heredado para que se pueda utilizar [Sling Resource Fusion](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) and [Ocultar condiciones](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) para ocultar, reemplazar o reordenar secciones del cuadro de diálogo original. La estructura que se va a replicar se define como cualquier cosa hasta el nivel de nodo de elemento de tabulación.

Para ser totalmente compatible con cualquier cambio realizado en un cuadro de diálogo en la versión actual, es muy importante que las estructuras debajo del nivel de elemento de tabulación no se toquen (ocultas, agregadas, reemplazadas, reordenadas, etc.). En su lugar, un elemento de ficha del elemento principal debe ocultarse mediante `sling:hideResource` la propiedad (consulte [Sling Resource Fusion Properties)](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)y agregar nuevos elementos de tabulación que contengan los campos de configuración de bespoke. `sling:orderBefore` se pueden utilizar para reordenar los elementos de la ficha si es necesario.

El siguiente cuadro de diálogo muestra la estructura de diálogo recomendada y cómo ocultar y reemplazar una ficha heredada tal como se describe anteriormente:

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

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

La lógica comercial de los componentes principales se implementa en Sling Models. Esta lógica se puede ampliar utilizando un patrón de delegación Sling.

Por ejemplo, el componente núcleo del título utiliza la `jcr:title` propiedad del recurso solicitado para proporcionar el texto del título. Si no `jcr:title` se define ninguna propiedad, se implementa una alternativa al título de la página actual. Queremos cambiar el comportamiento para que el título de la página actual siempre se muestre.

Dado que la implementación de los modelos de los componentes principales es privada, debe ampliarse con un patrón de delegación.

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

For further details about the delegation pattern see the Core Components GitHub Wiki article [Delegation Pattern for Sling Models](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Personalización del marcado {#customizing-the-markup}

A veces, el estilo avanzado requiere una estructura de marcado diferente del componente.

Esto se puede realizar fácilmente copiando los archivos HTL que deben modificarse desde el componente principal al componente proxy.

Volviendo a tomar el ejemplo del componente de Crumb principal, para personalizar el resultado de la marca, es `breadcrumb.html` necesario copiar el archivo en el componente específico del sitio que tenga un punto apuntado `sling:resourceSuperTypes` al componente de ruta de navegación principal.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

### Estilo de los componentes {#styling-the-components}

La primera forma de personalización es aplicar estilos CSS.

Para facilitar este proceso, los componentes principales representan la marca semántica y siguen una convención de nombre estandarizada inspirada por [Bootstrap](https://getbootstrap.com/). Además, para dirigir y namespace fácilmente los estilos de los componentes individuales, cada componente principal se envuelve en un elemento DIV con las clases &quot; `cmp`&quot; y &quot; `cmp-<name>`&quot;.

Por ejemplo, al ver el archivo HTL del componente v 1 Core Breadcrumb: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que la jerarquía de elementos es `ol.breadcrumb > li.breadcrumb-item > a`. Así, para asegurarse de que una regla CSS solo afecta a la clase de sendero de exploración de ese componente, todas las reglas deben nombrarse como se muestra a continuación:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Además, cada uno de los componentes principales aprovecha la función [de sistema de estilos AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) que permite a los autores de plantillas definir nombres de clases CSS adicionales que los autores de páginas pueden aplicar al componente. Esto permite definir para cada plantilla una lista de estilos de componente permitidos y si uno de ellos debe aplicarse de forma predeterminada a todos los componentes de ese tipo.

## Actualizar compatibilidad de personalizaciones {#upgrade-compatibility-of-customizations}

Se permiten tres tipos diferentes de actualizaciones:

* actualizar la versión de AEM
* actualizar los componentes principales a una nueva versión secundaria
* actualizar los componentes principales a una versión principal

En general, la actualización de AEM a una nueva versión no afectará a los componentes principales ni a las personalizaciones realizadas, siempre que las versiones de los componentes también admitan la nueva versión de AEM que se esté migrando y que las personalizaciones no utilicen API que estén [obsoletas o eliminadas](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

La actualización de los componentes principales sin pasar a una versión principal más reciente no debe afectar a las personalizaciones, siempre y cuando se usen los patrones de personalización descritos en esta página.

Cambiar a una versión principal más reciente de los componentes principales es compatible únicamente con la estructura de contenido, pero es posible que deba volver a factorizar las personalizaciones. Se publicarán registros de cambios de cambio para cada versión de componente para resaltar los cambios que afectarán el tipo de personalizaciones descritas en esta página.

## Compatibilidad con personalizaciones {#support-of-customizations}

Al igual que para cualquier componente de AEM, hay una serie de aspectos que debe tener en cuenta acerca de las personalizaciones:

1. **No modifique directamente el código de los componentes principales.**

   Esto no será compatible completamente y hará que las futuras actualizaciones de los componentes resulten difíciles. En su lugar, utilice los métodos de personalización descritos en esta página.

1. **El código personalizado es su propia responsabilidad.**

   Nuestro programa de soporte no cubre el código personalizado, y los problemas informados que no se pueden reproducir con los componentes de vaincore que [se utilizan como documentados](using.md) no se califican.

1. **Vea la funcionalidad obsoleta y eliminada.**

   Con cada nueva versión de AEM a la que se esté actualizando, asegúrese de que todas las API utilizadas siguen teniendo un buen funcionamiento fijándose en la [página Funciones](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html) obsoletas y eliminadas.

Consulte también [la sección Compatibilidad](developing.md#core-component-support) con componentes principales.

**Siguiente:**

* [Uso de componentes](using.md) principales: familiarícese con los componentes principales en su propio proyecto.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
