---
title: Componente de sendero de exploración
seo-title: Componente de sendero de exploración
description: nulo
seo-description: El componente de ruta de componente principal es un componente de navegación que crea una ruta de vínculos basada en la ubicación de la página en la jerarquía de contenido.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: ecd 237 df -08 b 8-4 deb -9881-66 a 1 f 0 d 65 ef 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Breadcrumb Component{#breadcrumb-component}

El componente de ruta de componente principal es un componente de navegación que crea una ruta de vínculos basada en la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente de sendero de exploración muestra la posición de la página actual dentro de la jerarquía del sitio, permitiendo que los visitantes de la página naveguen por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página de página.

Available options, such as the default navigation level and the ability to show the current page or hidden pages, can be defined by the template author in the [design dialog](#design-dialog). The content editor can then choose if hidden pages should be shown or not and the actual navigation level for the component in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente de sendero de exploración es v 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](breadcrumb-v1.md) | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Breadcrumb Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/breadcrumb.html).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Breadcrumb Component supports [schema.org microdata](https://schema.org/BreadcrumbList).

## Technical Details {#technical-details}

The latest technical documentation about the Breadcrumb Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite que el autor del contenido suprima las páginas ocultas y activas en las rutas, así como la profundidad en la jerarquía que debería mostrar.

![](assets/screen_shot_2018-01-12at124250.png)

* **Nivel** de inicio de navegación: en la jerarquía, el componente de sendero de navegación debería comenzar a desplazarse hacia la página actual. Por ejemplo, en We. Retail:

   * 0 starts at `/content`

   * 1 starts at `/content/we-retail`
   * 2 starts at `/content/we-retail/<country>`

* **Mostrar elementos** de navegación ocultos: Mostrar páginas marcadas como ocultas en la ruta (de forma predeterminada, no se mostrarán)
* **Ocultar la página actual**: Eliminar la página actual en la ruta (de forma predeterminada se mostrará)

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los valores predeterminados para las opciones para eliminar las páginas ocultas y activas en las rutas, así como la profundidad en la jerarquía que debería mostrar.

### Main Tab {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **Nivel** de inicio de navegación: define el valor predeterminado para donde en la jerarquía el componente de sendero de exploración debería comenzar a bajar a la página actual cuando se agrega el componente de sendero de migas a una página.
* **Mostrar elementos** de navegación ocultos: define el valor predeterminado de la opción **Mostrar elementos** de navegación ocultos cuando se agrega el componente de ruta de navegación a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar página actual**: define el valor predeterminado de la opción **Ocultar página** actual cuando se agrega el componente de sendero de migas a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

### Styles Tab {#styles-tab}

The Breadcrumb Component supports the AEM [Style System](authoring.md#component-styling).