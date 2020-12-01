---
title: Versiones de componentes principales
description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica qué versiones y versiones son y cómo comprender la compatibilidad con los componentes principales y AEM.
translation-type: tm+mt
source-git-commit: 2f3d2499e9f6c88453b633c20e49703eac25eff4
workflow-type: tm+mt
source-wordcount: '1870'
ht-degree: 22%

---


# Versiones de componentes principales {#core-components-versions}

La versión actual de los Componentes principales es 2.12.1 y es compatible con [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) y [instalaciones AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) locales. Fue lanzado en noviembre de 2020 como revisión de 2.12.0. La versión 2.12.0 incorpora varias funciones nuevas para formularios, metadatos y la capa de datos.

## Historial de versiones y compatibilidad {#release-history-and-compatibility}

Los componentes principales están diseñados para ser flexibles y compatibles con todas las versiones AEM compatibles. Debido a esto, una versión de los componentes puede contener varias versiones del mismo componente.

Las siguientes tablas ilustran la compatibilidad de las versiones de los componentes principales junto con las versiones de los componentes en las que se incluyen.

### Historial y requisitos de la versión {#release-history-requirements}

La siguiente tabla, cuyo contenido está [disponible en GitHub con detalles completos de la versión](https://github.com/adobe/aem-core-wcm-components/releases), ofrece una visión general de las versiones de los Componentes principales y su compatibilidad con las versiones de AEM y las versiones de Java.

| Versión | Descripción | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service | Java | Fecha de la versión |
|---|---|---|---|---|---|---|
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Esta fue una versión de parche para 2.12.0 que incluye correcciones menores. | 6.4.8.1+ * | 6.5.5.0+ * | Continua | 8, 11 | 11 de noviembre de 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Esta fue una versión de parche para 2.12.0 que corrige un error importante en el [Componente de imagen.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continua | 8, 11 | 5 de noviembre de 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Esta versión introdujo [un nuevo controlador de formularios POST;](/help/components/forms/form-container.md#post-data) la capacidad de incluir etiquetas CSS, Javascript y metadatos [personalizados mediante configuración según el contexto;](/help/developing/including-clientlibs.md#context-aware-loading) y una utilidad `DataLayerBuilder` para [simplificar la integración de capas de datos en componentes personalizados.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | Continua | 8, 11 | 29 de octubre de 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Esta versión introdujo la compatibilidad con [AMP.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continua | 8, 11 | 20 de julio de 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Esta versión introdujo el componente [Visor de PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 17 de junio de 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Esta versión habilitó la integración con la [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md) e introdujo el componente [barra de progreso.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Continua | 8, 11 | 29 de mayo de 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Esta versión se centra en correcciones con pequeñas mejoras. | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 5 de diciembre de 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versión introdujo el nuevo [componente incrustado.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 25 de septiembre de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versión introdujo el nuevo [componente Fragmento de experiencias.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 6 de septiembre de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versión presenta los nuevos [componentes de acordeón,](/help/components/accordion.md) [botón,](/help/components/button.md) [Contenedor,](/help/components/container.md) y [Descargar.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8, 11 | 25 de junio de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versión presenta el [Componente de Lista de fragmento de contenido.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8, 11 | 7 de mayo de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versión se centró en refinamientos de la [Biblioteca de componentes,](https://aemcomponents.dev) pero también contiene algunas mejoras de funciones para el [Componente separador.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8 | 14 de marzo de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versión se centra en la [biblioteca de componentes](https://aemcomponents.dev), así como en la introducción del nuevo [componente separador,](/help/components/separator.md), pero también contiene algunas mejoras de funciones para el [componente de imagen.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 de febrero de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versión se centra principalmente en la corrección de errores, pero también contiene algunas mejoras de funciones para el [componente Carrusel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 de noviembre de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | En esta versión se introdujeron el [Componente de fichas](/help/components/tabs.md) y el [Componente de carrusel](/help/components/carousel.md), así como mejoras en el [Componente de imagen,](/help/components/image.md) [Componente de página,](/help/components/page.md) y [Componente de título](/help/components/title.md) y seguimiento mejorado. | 6.4.2.0+ | - | - | 8 | 16 de octubre de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Esta versión introdujo el [componente Teaser](/help/components/teaser.md) junto con mejoras en el [componente de imagen](/help/components/image.md) y numerosas correcciones de errores. | 6.4.2.0+ | - | - | 8 | 13 de julio de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Esta fue una versión de corrección de errores. | 6.4.0.0+ | - | - | 8 | 12 de junio de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Esta versión ha añadido mejoras en el equipo, correcciones de errores y pequeñas mejoras, incluida la compatibilidad con el cambio de imagen en el [componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Esta versión se centra principalmente en las mejoras en la parte inferior del capó, las correcciones de errores y algunas mejoras menores en el [Componente de imagen,](/help/components/image.md) [Componente de página,](/help/components/page.md) y [Componente de fragmento de contenido.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 de marzo de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Esta versión introdujo el [componente de navegación,](/help/components/navigation.md) [componente de navegación de idioma,](/help/components/language-navigation.md) y el [componente de búsqueda rápida](/help/components/quick-search.md) e implementó el [sistema de estilo](/help/get-started/authoring.md#component-styling) para todos los componentes. | 6.4.0.0+ | - | - | 8 | 16 de enero de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Esta versión implementa la exportación de JSON en todos los componentes e introduce el [Componente de fragmento de contenido.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 de octubre de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Esta versión agrega varias correcciones para el [componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Esta versión agrega correcciones para el [Componente de página,](/help/components/page.md) [Componente de imagen,](/help/components/image.md) y varias correcciones y mejoras globales. | 6.4.0.0+ | - | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Esta versión agrega correcciones para imágenes GIF animadas en [Componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 de marzo de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versión inicial de los componentes principales. | 6.4.0.0+ | - | - | 7 | 20 de marzo de 2017 |

>[!NOTE]
>
>(*) Desde la versión 2.11.0, se requiere `org.apache.sling.models.impl` versión 1.4.12 o superior (debido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Esto se proporcionará para AEM 6.4 y 6.5 en un futuro Service Pack. Hasta entonces, el paquete de modelos Sling se incluye en el paquete `core.wcm.components.all`.

>[!TIP]
>
>Al igual que con AEM, Adobe recomienda que los desarrolladores utilicen la [versión más reciente y las versiones de los Componentes principales](https://github.com/adobe/aem-core-wcm-components/releases/latest) disponibles que sean compatibles con la versión de AEM que están ejecutando para beneficiarse de las correcciones y características más actualizadas.

### Versiones y versiones de componentes {#component-versions-and-releases}

La siguiente tabla detalla las versiones de los componentes que contiene cada versión de los componentes principales.

|  | Versión 1.0.0 - 1.0.6 | Versión 1.1.0 | Versión 2.0.0 - 2.0.8 | Versión 2.1.0 | Versión 2.2.0-2.2.0 | Versión 2.3.0-2.3.2 | Versión 2.4.0 | Versión 2.5.0 | Versión 2.6.0 | Versión 2.7.0-2.8.0 | Versión 2.9.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Título](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Imagen](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lista](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Ruta de navegación](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Compartir en redes sociales](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contenedor del formulario](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Texto de formulario](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opciones de formulario](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulario oculto](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Botón de formulario](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragmento de contenido](components/content-fragment-component.md)** |  | Simulador para pruebas | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Navegación](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navegación por idiomas](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Búsqueda rápida](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Pestañas](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carrusel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Separador](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lista de fragmentos de contenido](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Acordeón](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Botón](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Contenedor](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Descargar](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Fragmento de experiencias](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Incrustar](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Barra de progreso](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 |
| **[Visualizador de PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 |

## Versiones y versiones {#versions-and-releases}

Los componentes principales se distribuyen a través de GitHub. Esto permite a Adobe agregar más rápidamente funcionalidad a los componentes y también permitir la entrada de la comunidad fuera del ciclo de publicación de AEM.

Los componentes principales están disponibles con versiones AEM definidas con las que son compatibles. Esto significa que una versión AEM puede admitir varias versiones o versiones de los componentes principales. Esto proporciona más flexibilidad que los antiguos componentes de base, que estaban vinculados a una versión específica de AEM.

### Versiones {#versions}

La iteración principal de los componentes principales son las **versiones**. Cada componente tiene una versión. Las versiones se indican con **v** anexado con un entero positivo distinto de cero, como v1 y v2. Las versiones solo se incrementan para los cambios que no son compatibles con versiones anteriores, lo que normalmente sucede con la introducción de nuevas funciones y funcionalidades.

Los desarrolladores y administradores pueden reconocer versiones de los componentes principales por un número en sus rutas de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal definida por [directrices semánticas de versiones](https://semver.org/).

Para obtener más información sobre las versiones de componentes principales, consulte la [documentación para desarrolladores de los componentes principales](developing/guidelines.md).

### Versiones {#releases}

Los componentes principales están disponibles mediante **versiones** y [representan los artefactos publicados reales disponibles en GitHub](https://github.com/adobe/aem-core-wcm-components/releases). Las versiones se indican con un número decimal del formato X.Y.Z y recopilan todos los componentes principales juntos como un paquete de entrega.

* **Las** versiones principales pueden introducir nuevas versiones de componentes existentes junto con componentes completamente nuevos, así como correcciones de errores estándar. Esto se representa mediante un incremento en el componente X del número de versión.
* **Las** versiones importantes pueden introducir nuevas funciones a las versiones existentes de los componentes, junto con correcciones de errores. Esto se representa mediante un incremento en el componente Y del número de versión.
* **Las** versiones secundarias solo contienen correcciones de errores. Esto se representa mediante un incremento en el componente Z del número de versión.

>[!NOTE]
>
>Las versiones pueden contener varias versiones del mismo componente.
>
>La misma versión de un componente puede aparecer en varias versiones.

## Compatibilidad con componentes principales {#core-components-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que sucede con otras funciones del producto, la regla general de la fecha de vencimiento es:

* Los componentes se anuncian primero como en desuso antes de eliminarse
* Se eliminarán de la versión de AEM lo antes posible tras realizar el anuncio.

Esto proporciona a los clientes al menos un ciclo de lanzamiento para poder cambiarse a la nueva versión del componente antes de que finalice el servicio de soporte.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más detalles sobre la compatibilidad de la personalización de componentes, consulte la página [Personalización de componentes principales](developing/customizing.md) de la versión del componente principal en cuestión.

## Compatibilidad con componentes de base {#foundation-component-support}

El énfasis del Adobe en el desarrollo se ha desplazado a los componentes principales y se seguirán añadiendo nuevas funciones.

[Casi todos los componentes de base han quedado obsoletos con AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) y solo se tendrán en cuenta correcciones de errores importantes para los componentes de base a partir de ahora.
