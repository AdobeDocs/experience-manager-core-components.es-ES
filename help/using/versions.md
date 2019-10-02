---
title: Versiones de componentes principales
seo-title: Versiones de componentes principales
description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
seo-description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
uuid: a916a923-8c5e-456a-84b5-b5228e21434
contentOwner: Usuario
content-type: referencia
topic-tags: introducción
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
translation-type: tm+mt
source-git-commit: d748bf211ec36d12cac016ca9bf707f24db1ce48

---


# Versiones de componentes principales{#core-components-versions}

La versión actual de los componentes principales es 2.7.0 y es compatible con AEM 6.5. Se publicó en septiembre de 2019 como una actualización importante de la versión 2.0.0. La versión 2.0.0 incorpora nuevos componentes y actualizaciones de la versión 2 de los componentes existentes.

Consulte la sección Historial de [versiones y Compatibilidad](#versions-and-releases) de este documento para obtener más información.

También puede consultar la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library.html)componentes, que muestra la versión actual de los componentes principales y ofrece ejemplos de su uso.

## Versiones y versiones {#versions-and-releases}

Los componentes principales se distribuyen mediante GitHub. Esto permite a Adobe agregar más rápidamente funciones a los componentes y también permitir la entrada de la comunidad fuera del ciclo de versiones de AEM.

Los componentes principales están disponibles con versiones de AEM definidas con las que son compatibles. Esto significa que una versión de AEM puede admitir varias versiones o versiones de los componentes principales. Esto proporciona más flexibilidad que los antiguos componentes de base, que estaban vinculados a una versión específica de AEM.

### Versiones {#versions}

La iteración principal de los componentes principales son las **versiones**. Cada componente tiene una versión. Las versiones se indican con **v** anexada con un entero positivo distinto de cero, como v1 y v2. Las versiones solo se incrementan para los cambios que no son compatibles con versiones anteriores, lo que normalmente sucede con la introducción de nuevas funciones y funcionalidades.

Los desarrolladores y administradores pueden reconocer versiones de los componentes principales por un número en sus rutas de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal, tal como se define en las directrices [de versiones](https://semver.org/)semánticas.

Para obtener más información sobre las versiones de componentes principales, consulte la documentación para [desarrolladores de los componentes](guidelines.md)principales.

### Versiones {#releases}

The core components are made available through releases and represent the actual published artifacts available on GitHub. ****[](https://github.com/adobe/aem-core-wcm-components/releases) Releases are denoted with a decimal number of the format X.Y.Z and collect all core components together as a deliverable package.

* **Major releases can introduce new versions of existing components along with entirely new components as well as standard bug fixes.** This is represented by an increment in the X component of the release number.
* **Important releases can introduce new functionality to existing versions of components along with bug fixes.** This is represented by an increment in the Y component of the release number.
* **Minor releases contain only bug fixes.** This is represented by an increment in the Z component of the release number.

>[!NOTE]
>
>Releases can contain multiple versions of the same component.
>
>The same version of a component can appear in multiple releases.

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components were first released with AEM 6.3 and are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History &amp; Supported AEM Versions {#release-history-supported-aem-versions}

La siguiente tabla, cuyo contenido está [disponible en GitHub con todos los detalles](https://github.com/adobe/aem-core-wcm-components/releases)de la versión, ofrece una visión general de las versiones de los Componentes principales y su compatibilidad con las versiones de AEM y las versiones de Java.

| Versión | Descripción | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | Fecha de lanzamiento |
|---|---|---|---|---|---|---|
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versión incorpora el nuevo componente Incrustar | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 25 de septiembre de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versión incorpora el nuevo componente Fragmento de experiencias | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 6 de septiembre de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versión incorpora los nuevos componentes Acordeón, Botón, Contenedor y Descargar. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 25 de junio de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versión incorpora el componente Lista de fragmentos de contenido | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 7 de mayo de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versión se centra en perfeccionar la biblioteca de componentes, pero también contiene algunas mejoras en las funciones del componente Separador | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 | 14 de marzo de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versión se centra en la biblioteca de componentes y en la introducción del nuevo componente separador, pero también contiene algunas mejoras de funciones para el componente de imagen | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 11 de febrero de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versión se centra principalmente en la corrección de errores, pero también contiene algunas mejoras en las funciones del componente Carrusel | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 27 de noviembre de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Se han introducido fichas y componentes de carrusel, mejoras en los componentes de imagen, página y título y seguimiento mejorado | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 16 de octubre de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Se ha introducido el componente Teaser, se han mejorado los componentes de imagen y se han corregido numerosos errores | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 13 de julio de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Versión de corrección de errores | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 12 de junio de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Mejoras adicionales, correcciones de errores y pequeñas mejoras, incluida la compatibilidad con la inversión de imágenes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Mejoras, correcciones de errores y algunas mejoras menores en los componentes de imagen, página y fragmento de contenido, principalmente en el equipo | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 7 de marzo de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Se han introducido los componentes Navegación, Navegación de idioma y Búsqueda rápida. Sistema de estilo implementado para todos los componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 16 January 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementation of JSON export on all components, introduction of the Content Fragment component | 6.3.1.0 | 6.4.0.0+ | - | 8 | 10 October 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Several fixes for the Image component | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 4 August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fixes of Page Component, Image Component, various global fixes and improvements | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 26 April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Fixes for animated GIF images in Image component | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 22 March 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Initial release of Core Components | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 20 March 2017 |

>[!NOTE]
>
>As with AEM, Adobe recommends that developers use the latest release and versions of the Core Components available that is compatible with the version of AEM that they are running in order to benefit from the most up-to-date fixes and features.[](https://github.com/adobe/aem-core-wcm-components/releases/latest)

### Component Versions &amp; Releases {#component-versions-and-releases}

The following table details which versions of which components are contained in which releases of the Core Components.

|  | Release 1.0.0 - 1.0.6 | Versión 1.1.0 | Versión 2.0.0 - 2.0.8 | Versión 2.1.0 | Versión 2.2.0-2.2.0 | Versión 2.3.0-2.3.2 | Versión 2.4.0 | Versión 2.5.0 | Versión 2.6.0 | Versión 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Título](title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Imagen](image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lista](list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Ruta de exploración](breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Compartir en redes sociales](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contenedor del formulario](form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texto de formulario](form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opciones de formulario](form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulario oculto](form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Botón de formulario](form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento de contenido](content-fragment-component.md)** |  | Simulador para pruebas | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegación](navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegación por idiomas](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Búsqueda rápida](quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Fichas](tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrusel](carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Separador](separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Lista de fragmento de contenido](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Acordeón](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Botón](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Contenedor](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Descargar](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Fragmento de experiencias](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Incrustar](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Documentación {#documentation}

[La creación con componentes](authoring.md) principales describe el uso de los componentes principales y las funciones que se exponen a los autores de contenido y a los autores de plantillas. Each component is documented in detail.

[La biblioteca](http://opensource.adobe.com/aem-core-wcm-components/library.html) de componentes es una muestra de la versión actual de la mayoría de los componentes principales, que ilustra cómo se pueden utilizar.

[Desarrollar componentes](developing.md) principales describe las capacidades técnicas de los componentes principales, cómo utilizarlos en sus proyectos, cómo personalizarlos y prácticas recomendadas.

[La introducción](introduction.md) de los componentes principales ofrece una visión general de la compatibilidad de los componentes principales entre versiones, casos de uso y soporte.

[El tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) WKND es una excelente introducción paso a paso para el desarrollo de AEM, incluido el uso de los componentes principales.
