---
title: Versiones de componentes principales
seo-title: Versiones de componentes principales
description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
seo-description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
uuid: a916a923-8c5e-456a-84b5-b5228e21434
contentOwner: Usuario
content-type: referencia
topic-tags: introducción
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
translation-type: tm+mt
source-git-commit: 6882a0d8247328c403dc11a25ed9d079aefede69

---


# Versiones de componentes principales{#core-components-versions}

La versión actual de los componentes principales es 2.7.0 y es compatible con AEM 6.5. Se publicó en septiembre de 2019 como una actualización importante de la versión 2.0.0. La versión 2.0.0 incorpora nuevos componentes y actualizaciones de la versión 2 de los componentes existentes.

Consulte la sección Historial de [versiones y Compatibilidad](#versions-and-releases) de este documento para obtener más información.

También puede consultar la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library.html)componentes, que muestra la versión actual de los componentes principales y ofrece ejemplos de su uso.

## Versions and Releases {#versions-and-releases}

Core Components are distributed via GitHub. Esto permite a Adobe agregar más rápidamente funciones a los componentes y también permitir la entrada de la comunidad fuera del ciclo de versiones de AEM.

Los componentes principales están disponibles con versiones de AEM definidas con las que son compatibles. Esto significa que una versión de AEM puede admitir varias versiones o versiones de los componentes principales. Esto proporciona más flexibilidad que los antiguos componentes de base, que estaban vinculados a una versión específica de AEM.

### Versiones {#versions}

La iteración principal de los componentes principales son las **versiones**. Cada componente tiene una versión. Las versiones se indican con **v** anexada con un entero positivo distinto de cero, como v1 y v2. Las versiones solo se incrementan para los cambios que no son compatibles con versiones anteriores, lo que normalmente sucede con la introducción de nuevas funciones y funcionalidades.

Los desarrolladores y administradores pueden reconocer versiones de los componentes principales por un número en sus rutas de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal, tal como se define en las directrices [de versiones](https://semver.org/)semánticas.

Para obtener más información sobre las versiones de componentes principales, consulte la documentación para [desarrolladores de los componentes](guidelines.md)principales.

### Versiones {#releases}

Los componentes principales están disponibles a través de **las versiones** y [representan los artefactos publicados reales disponibles en GitHub](https://github.com/adobe/aem-core-wcm-components/releases). Las versiones se indican con un número decimal del formato X.Y.Z y recopilan todos los componentes principales juntos como un paquete de entrega.

* **Las versiones** principales pueden introducir nuevas versiones de componentes existentes junto con componentes completamente nuevos, así como correcciones de errores estándar. Esto se representa mediante un incremento en el componente X del número de versión.
* **Las versiones** importantes pueden introducir nuevas funciones a las versiones existentes de los componentes, junto con correcciones de errores. Esto se representa mediante un incremento en el componente Y del número de versión.
* **Las versiones** menores solo contienen correcciones de errores. Esto se representa mediante un incremento en el componente Z del número de versión.

>[!NOTE]
>
>Las versiones pueden contener varias versiones del mismo componente.
>
>La misma versión de un componente puede aparecer en varias versiones.

## Historial de versiones y compatibilidad {#release-history-and-compatibility}

Los componentes principales se lanzaron por primera vez con AEM 6.3 y están diseñados para ser flexibles y compatibles con todas las versiones de AEM admitidas. Debido a esto, una versión de los componentes puede contener varias versiones del mismo componente.

Las siguientes tablas ilustran la compatibilidad de las versiones de los componentes principales junto con las versiones de los componentes que contienen.

### Historial de versiones y versiones compatibles de AEM {#release-history-supported-aem-versions}

La siguiente tabla, cuyo contenido está [disponible en GitHub con todos los detalles](https://github.com/adobe/aem-core-wcm-components/releases)de la versión, ofrece una visión general de las versiones de los Componentes principales y su compatibilidad con las versiones de AEM y las versiones de Java.

| Versión | Descripción | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | Fecha de lanzamiento |
|---|---|---|---|---|---|---|
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versión incorpora el nuevo componente Incrustar | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 25 de septiembre de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versión incorpora el nuevo componente Fragmento de experiencias | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 6 de septiembre de 2019 |
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
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Se han introducido los componentes Navegación, Navegación de idioma y Búsqueda rápida. Sistema de estilo implementado para todos los componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 16 de enero de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementación de la exportación de JSON en todos los componentes, introducción del componente Fragmento de contenido | 6.3.1.0 | 6.4.0.0+ | - | 8 | 10 de octubre de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Varias correcciones para el componente Imagen | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correcciones del componente de página, del componente de imagen, varias correcciones y mejoras globales | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correcciones para imágenes GIF animadas en el componente Imagen | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 22 de marzo de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versión inicial de los componentes principales | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 20 de marzo de 2017 |

>[!NOTE]
>
>Al igual que con AEM, Adobe recomienda que los desarrolladores utilicen la [última versión y las versiones de los componentes](https://github.com/adobe/aem-core-wcm-components/releases/latest) principales disponibles, compatibles con la versión de AEM que están ejecutando para beneficiarse de las correcciones y funciones más actualizadas.

### Versiones y versiones de componentes {#component-versions-and-releases}

La siguiente tabla detalla las versiones de los componentes que contiene cada versión de los componentes principales.

|  | Versión 1.0.0 - 1.0.6 | Versión 1.1.0 | Versión 2.0.0 - 2.0.8 | Versión 2.1.0 | Versión 2.2.0-2.2.0 | Versión 2.3.0-2.3.2 | Versión 2.4.0 | Versión 2.5.0 | Versión 2.6.0 | Versión 2.7.0+ |
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
| **[Lista de fragmentos de contenido](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Accordion](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Button](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Container](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Descargar](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Fragmento de experiencias](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Embed](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Documentación {#documentation}

[La creación con componentes](authoring.md) principales describe el uso de los componentes principales y las funciones que se exponen a los autores de contenido y a los autores de plantillas. Cada componente se documenta en detalle.

[La biblioteca](http://opensource.adobe.com/aem-core-wcm-components/library.html) de componentes es una muestra de la versión actual de la mayoría de los componentes principales, que ilustra cómo se pueden utilizar.

[Desarrollar componentes](developing.md) principales describe las capacidades técnicas de los componentes principales, cómo utilizarlos en sus proyectos, cómo personalizarlos y prácticas recomendadas.

[La introducción](introduction.md) de los componentes principales ofrece una visión general de la compatibilidad de los componentes principales entre versiones, casos de uso y soporte.

[El tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) WKND es una excelente introducción paso a paso para el desarrollo de AEM, incluido el uso de los componentes principales.
