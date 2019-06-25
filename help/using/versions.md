---
title: Versiones de componentes principales
seo-title: Versiones de componentes principales
description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. Este documento explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
seo-description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. Este documento explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
uuid: a 916 a 923-8 c 5 e -456 a -84 b 5-b 52228 e 21434
contentOwner: Usuario
content-type: referencia
topic-tags: introducción
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 3 a 98 b 2 f -65 bf -4493-82 ad -01717938 fdbc
translation-type: tm+mt
source-git-commit: 144494c03ffed068b403d80f62fdfddc73a53748

---


# Core Components Versions{#core-components-versions}

La versión actual de los componentes principales es 2.4.0 y es compatible con AEM 6.5. Se lanzó en mayo de 2019 como una actualización secundaria de la versión 2.0.0. La versión 2.0.0 introdujo nuevos componentes junto con actualizaciones v 2 de componentes existentes.

See the section [Release History and Compatibility](#versions-and-releases) of this document for more information.

You can also check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

## Versions and Releases {#versions-and-releases}

Los componentes principales se distribuyen mediante github. Esto permite que Adobe agregue más rápidamente funcionalidad a los componentes y también permita la entrada de comunidad fuera del ciclo de publicación de AEM.

Los componentes principales están disponibles con versiones de AEM definidas con las que son compatibles. Esto significa que una versión de AEM puede admitir varias versiones o versiones de los componentes principales. Esto proporciona más flexibilidad que los componentes base anteriores, que estaban ligados a una versión específica de AEM.

### Versiones {#versions}

The major iteration of the Core Components are the **versions**. Cada componente tiene una versión. Versions are denoted with **v** appended with a nonzero, positive integer such as v1 and v2. Las versiones solo se incrementan para los cambios que no son retrocompatibles, lo cual suele ocurrir con la introducción de nuevas funciones y funcionalidades.

Los desarrolladores y administradores pueden reconocer versiones de los componentes principales según un número en las rutas de tipo de recurso y en los nombres de clases Java completos de sus implementaciones. This version number represents a major version as defined by [semantic versioning guidelines](https://semver.org/).

For more details about core component versions, see the [developer documentation of the Core Components](guidelines.md).

### Releases {#releases}

The core components are made available through **releases** and [represent the actual published artifacts available on GitHub](https://github.com/adobe/aem-core-wcm-components/releases). Las versiones se indican con un número decimal del formato X.Y.Z y recopilan todos los componentes principales juntos como un paquete que se puede entregar.

* **Las versiones** principales pueden introducir nuevas versiones de componentes existentes junto con componentes completamente nuevos, así como correcciones de errores estándar. Esto se representa mediante un incremento en el componente X del número de lanzamiento.

* **Las versiones importantes** pueden introducir nuevas funciones para las versiones existentes de componentes junto con correcciones de errores. Esto se representa mediante un incremento en el componente Y del número de lanzamiento.

* **Las versiones menores** solo contienen correcciones de errores. Esto se representa mediante un incremento en el componente Z del número de lanzamiento.

>[!NOTE]
>
>Las versiones pueden contener varias versiones del mismo componente.
>
>La misma versión de un componente puede aparecer en varias versiones.

## Release History and Compatibility {#release-history-and-compatibility}

Los componentes principales se lanzaron por primera vez con AEM 6.3 y están diseñados para ser flexibles y compatibles con todas las versiones de AEM admitidas. Debido a esto, una versión de los componentes puede contener varias versiones del mismo componente.

Las tablas siguientes ilustran la compatibilidad de las versiones de los componentes principales con las versiones de componentes que contienen las versiones.

### Release History &amp; Supported AEM Versions {#release-history-supported-aem-versions}

The following table, the contents of which are [available on GitHub with full release details](https://github.com/adobe/aem-core-wcm-components/releases), gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.

| Versión | Descripción | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java |
|---|---|---|---|---|---|
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versión introdujo el componente Lista de fragmentos de contenido | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versión se centra en refinamientos en la biblioteca de componentes, pero también contiene algunas mejoras de funciones para el componente Separador | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versión se centra en la biblioteca de componentes y presenta el nuevo componente separador, pero también contiene algunas mejoras de funciones para el componente de imagen | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versión se centra principalmente en correcciones de errores, pero también contiene algunas mejoras de funciones para el componente Carrusel. | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Componentes de fichas y carrusel introducidos, mejoras en la imagen, componentes de página y título y seguimiento mejorado | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Componente teaser introducido, mejoras en componentes de imagen y varias correcciones de errores | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Versión de corrección | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Mejoras adicionales, correcciones de errores y pequeñas mejoras, incluida la compatibilidad con el volteo de imágenes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Principalmente mejoras específicas, correcciones de errores, además de mejoras menores en los componentes de imagen, página y fragmento de contenido | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Se introdujeron los componentes Navegación, Navegación por idioma y Búsqueda rápida. Sistema de estilo implementado para todos los componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementación de la exportación JSON en todos los componentes, introducción al componente Fragmento de contenido | 6.3.1.0 | 6.4.0.0+ | - | 8 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Varias correcciones del componente Imagen | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correcciones del componente de página, componente de imagen, varias correcciones y mejoras globales | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correcciones para imágenes GIF animadas en el componente Imagen | 6.3.0.0+ | 6.4.0.0+ | - | 7 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versión inicial de los componentes principales | 6.3.0.0+ | 6.4.0.0+ | - | 7 |

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the [latest release and versions of the Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.

### Component Versions &amp; Releases {#component-versions-and-releases}

En la tabla siguiente se detallan las versiones de los componentes contenidos en las versiones de los componentes principales.

|  | Versión 1.0.0 - 1.0.6 | Versión 1.1.0 | Versión 2.0.0 - 2.0.8 | Versión 2.1.0 | Versión 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[Página](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Título](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Imagen](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Lista](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Ruta de navegación](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Compartir en redes sociales](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contenedor del formulario](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Texto de formulario](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Opciones de formulario](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formulario oculto](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Botón de formulario](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Fragmento de contenido](content-fragment-component.md)** |  | Simulador para pruebas | v1 | v1 | v1 | v1 |
| **[Navegación](navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Navegación por idiomas](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Búsqueda rápida](quick-search.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 |
| **[Fichas](tabs.md)** |  |  |  |  | v1 | v1 |
| **[Carrusel](carousel.md)** |  |  |  |  | v1 | v1 |
| **[Separador](separator.md)** |  |  |  |  |  | v1 |

## Documentación {#documentation}

[La creación con componentes](authoring.md) principales describe el uso de los componentes principales y las funciones expuestas a autores de contenido y autores de plantillas. Cada componente está documentado en detalle.

[Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html) es una vidriera de la versión actual de la mayoría de los componentes principales, ilustrando cómo se pueden utilizar.

[Desarrollar componentes principales](developing.md) describe las capacidades técnicas de los componentes principales, cómo utilizarlos en sus proyectos, cómo personalizar y prácticas recomendadas.

[Introducción a componentes principales](introduction.md) proporciona una descripción general de la compatibilidad de los componentes principales entre las versiones, los casos de uso y la compatibilidad.
