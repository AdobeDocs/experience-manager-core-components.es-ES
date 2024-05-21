---
title: Versiones de componentes principales
description: Los componentes principales se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica cuáles son las versiones y publicaciones y cómo comprender la compatibilidad con los componentes principales y de AEM.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: e25756d808d1deac338f4b7e054fe6f016a6bb97
workflow-type: ht
source-wordcount: '3079'
ht-degree: 100%

---

# Versiones de componentes principales {#core-components-versions}

La versión actual de los componentes principales es 2.25.4, y es compatible con [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es) y con las instalaciones de [AEM On-Premise](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=es).

## Historial y compatibilidad de la versión {#release-history-and-compatibility}

Los componentes principales están diseñados para ser flexibles y compatibles con todas las versiones de AEM admitidas. Debido a esto, una versión de los componentes puede contener varias versiones del mismo componente.

En las siguientes tablas se ilustra la compatibilidad de las versiones de los componentes principales junto con las versiones de los componentes en las que se incluyen.

### Historial y requisitos de la versión {#release-history-requirements}

La siguiente tabla, cuyo contenido está [disponible en GitHub con detalles de versión completos](https://github.com/adobe/aem-core-wcm-components/releases), ofrece una visión general de las versiones de los componentes principales y su compatibilidad con las versiones de AEM y las versiones de Java.

| Versión | Descripción | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Fecha de la versión |
|---|---|---|---|---|---|---|
| [2.25.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.4) | Esta es una versión secundaria que corrige algunos errores de TI. | - | 6.5.22.0+ | Continua | 8, 11 | 10 de mayo de 2024 |
| [2.25.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.2) | Esta es una versión secundaria que corrige algunos errores de TI. | - | 6.5.22.0+ | Continua | 8, 11 | 9 de mayo de 2024 |
| [2.25.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.0) | Esta versión ofrece compatibilidad con smartCrop en Dynamic Media, e incluye mejoras de rendimiento y accesibilidad y varias correcciones de errores. | - | 6.5.21.0+ | Continua | 8, 11 | 2 de mayo de 2024 |
| [2.24.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.6) | Esta versión de parche incluye mejoras para la inicialización de la capa de datos. | - | 6.5.21.0+ | Continua | 8, 11 | 22 de abril de 2024 |
| [2.24.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.4) | Esta versión de parche corrige una inicialización de Sling Model. | - | 6.5.21.0+ | Continua | 8, 11 | 1 de abril de 2024 |
| [2.24.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.2) | Esta versión de parche mejora la estabilidad de las pruebas de integración. | - | 6.5.21.0+ | Continua | 8, 11 | 22 de febrero de 2024 |
| [2.24.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.0) | Esta versión ofrece compatibilidad con la capa de datos de Google Tag Manager e incluye varias correcciones de errores. | - | 6.5.21.0+ | Continua | 8, 11 | 14 de febrero de 2024 |
| [2.23.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.4) | Esta versión del parche incluye varias correcciones de errores. | - | 6.5.17.0+ | Continua | 8, 11 | 15 de septiembre de 2023 |
| [2.23.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.2) | Este parche ha añadido el recorte inteligente de Dynamic Media para recursos remotos a [Imagen](/help/components/image.md) y [Componentes de teaser](/help/components/teaser.md) y corrigió una serie de errores. | - | 6.5.17.0+ | Continua | 8, 11 | 4 de agosto de 2023 |
| [2.23.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.0) | Esta versión añadió compatibilidad con [Recursos remotos de Dynamic Media de próxima generación.](/help/developing/next-gen-dm.md) | - | 6.5.17.0+ | Continua | 8, 11 | 6 de junio de 2023 |
| [2.22.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.12) | Esta versión del parche corrige dos problemas. | - | 6.5.14.0+ | Continua | 8, 11 | 25 de mayo de 2023 |
| [2.22.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.10) | Esta versión del parche corrige dos regresiones. | - | 6.5.14.0+ | Continua | 8, 11 | 11 de mayo de 2023 |
| [2.22.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.8) | Esta versión del parche incorpora funciones que se eliminaron accidentalmente en la versión anterior. | - | 6.5.14.0+ | Continua | 8, 11 | 9 de mayo de 2023 |
| [2.22.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.6) | Esta versión del parche corrige una regresión en el [Componente Contenedor.](/help/components/container.md) | - | 6.5.14.0+ | Continua | 8, 11 | 21 de abril de 2023 |
| [2.22.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.4) | Este es un parche para solucionar problemas en el [Componente de lista de fragmentos de contenido.](/help/components/content-fragment-list.md) | - | 6.5.14.0+ | Continua | 8, 11 | 5 de abril de 2023 |
| [2.22.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.2) | Esta es una versión de mantenimiento para resolver dos problemas introducidos en la versión 2.22.0 | - | 6.5.14.0+ | Continua | 8, 11 | 31 de marzo de 2023 |
| [2.22.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.0) | Esta versión presenta una nueva versión del [Componente Lista](/help/components/list.md) junto con mejoras del [Teaser](/help/components/teaser.md) y la actualización del [Visualizador de PDF](/help/components/pdf-viewer.md) y [Carrusel](/help/components/carousel.md) | - | 6.5.14.0+ | Continua | 8, 11 | 9 de febrero de 2023 |
| [2.21.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2) | Este lanzamiento de parche soluciona un problema con los [Componentes de teaser](/help/components/teaser.md) de las versiones 1 y 2. | - | 6.5.13.0+ | Continua | 8, 11 | 12 de septiembre de 2022 |
| [2.21.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0) | Esta versión incluye una serie de mejoras, incluida la publicación de la API de LinkHandler, mejoras en el [componente de imagen](/help/components/image.md) y en la [capa de datos,](/help/developing/data-layer/overview.md) así como mejoras en los componentes de varios paneles. | - | 6.5.13.0+ | Continua | 8, 11 | 12 de septiembre de 2022 |
| [2.20.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8) | Esta versión corrige un problema en la entrega de imágenes SVG a través de AdaptiveImageServlet. | - | 6.5.13.0+ | Continua | 8, 11 | 4 de agosto de 2022 |
| [2.20.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | Esta versión de parche corrige un problema con el nuevo [Componente Tabla de contenidos.](/help/components/tableofcontents.md) | - | 6.5.13.0+ | Continua | 8, 11 | 7 de julio de 2022 |
| [2.20.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | Esta versión del parche corrige un problema con el nuevo [Componente Tabla de contenidos.](/help/components/tableofcontents.md) | - | 6.5.13.0+ | Continua | 8, 11 | 29 de junio de 2022 |
| [2.20.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | Esta es una versión de parche que corrige un problema en el nuevo [servicio de entrega de recursos optimizado para la web](/help/developing/web-optimized-image-delivery.md) de AEMaaCS. | - | 6.5.13.0+ | Continua | 8, 11 | 20 de junio de 2022 |
| [2.20.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | Esta versión añade un nuevo [Componente en la Tabla de contenidos](/help/components/tableofcontents.md), agrega compatibilidad con el [servicio de entrega de recursos optimizado para la web de AEMaaCS](/help/developing/web-optimized-image-delivery.md) e incluye correcciones de errores. | - | 6.5.13.0+ | Continua | 8, 11 | 9 de junio de 2022 |
| [2.19.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | Esta versión agrega una nueva versión al [Componente Búsqueda](/help/components/quick-search.md) y las funciones de [Componente Botón](/help/components/button.md), así como muchas mejoras de accesibilidad y correcciones de errores. | - | 6.5.10.0+ | Continua | 8, 11 | 7 de abril de 2022 |
| [2.18.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | Esta versión corrige un problema para AEMaaCS. | - | 6.5.10.0+ | Continua | 8, 11 | 17 de marzo de 2022 |
| [2.18.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | Esta es una versión de parche. | - | 6.5.10.0+ | Continua | 8, 11 | 3 de marzo de 2022 |
| [2.18.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | En esta versión principal de los componentes principales se ha introducido un nuevo controlador de vínculos en las nuevas versiones de varios componentes, así como muchas mejoras de accesibilidad y correcciones de errores. | - | 6.5.10.0+ * | Continua | 8, 11 | 16 de febrero de 2022 |
| [2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Esta es una versión de parche. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 13 de diciembre de 2021 |
| [2.17.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Esta es una versión de parche que corrige una regresión introducida con la versión anterior. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 1 de octubre de 2021 |
| [2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | Este parche mejora los componentes [Lista](/help/components/list.md) y [Navegación](/help/components/navigation.md) para mostrar la URL externa para los destinos de redireccionamiento, habilita la herencia de imágenes de página para la próxima versión 2 del componente [Teaser](/help/components/teaser.md), y contiene correcciones de errores adicionales. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 31 de agosto de 2021 |
| [2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | Esta es una versión del parche que corrige un cambio incompatible con versiones anteriores que se introdujo anteriormente. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 2 de agosto de 2021 |
| [2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | Esta versión del parche es compatible con los mapas de sitio para páginas e incluye varias mejoras de accesibilidad. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 29 de julio de 2021 |
| [2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Esta versión del parche incluye una corrección para la [capa de datos](/help/developing/data-layer/overview.md) que no funciona con AEMaaCS. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 8 de julio de 2021 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Esta versión incluye previsualizaciones técnicas de muchas versiones de componentes nuevas que admiten funciones de controlador de vínculos, así como una previsualización técnica de una función de imagen destacada para el [Componente de página.](/help/components/page.md) También se incluyen varias correcciones de errores. | 6.4.8.4+ | 6.5.6.0+ | Continua | 8, 11 | 16 de junio de 2021 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Este es un parche para solucionar un problema con el nuevo controlador de vínculos. | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 19 de mayo de 2021 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Este fue un parche que principalmente solucionaba un problema con el nuevo controlador de vínculos y añadía una mejora para admitir aplicaciones de varias páginas para [PWA.](/help/components/page.md#pwa-support) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 15 de mayo de 2021 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Esta versión se centró en las mejoras de accesibilidad, así como en la introducción de un nuevo controlador de vínculos a los componentes existentes. | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 22 de abril de 2021 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Este fue un parche que principalmente soluciona problemas con compatibilidad con versiones anteriores de [Capa de datos](/help/developing/data-layer/overview.md) y pruebas de TI que fallan en ciertas situaciones. | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 16 de marzo de 2021 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Esta versión incluye compatibilidad con [aplicaciones web progresivas (PWA) en el componente de la página](/help/components/page.md#pwa-support) y admite la versión 2.0.0 de la [capa de datos de Adobe.](/help/developing/data-layer/overview.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 23 de febrero de 2021 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Esta versión incluye nuevas opciones para el [Componente incrustado](/help/components/embed.md) e introduce las Anotaciones de marca en el nivel [página](/help/components/page.md), además de abordar muchos problemas. | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 9 de febrero de 2021 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Este fue un parche que solucionaba un problema con RTE cuando se utilizaba en AEMaaCS | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 16 de diciembre de 2020 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Esta versión incluye nuevas funciones de Dynamic Media para el [Componente de imagen.](/help/components/image.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 4 de diciembre de 2020 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Este fue un parche para la versión 2.12.0 que incluía correcciones menores. | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 11 de noviembre de 2020 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Este fue un parche para 2.12.0 que corregía un error importante en el [Componente de imagen.](/help/components/image.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 5 de noviembre de 2020 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Esta versión introdujo [un nuevo controlador de formularios POST;](/help/components/forms/form-container.md#post-data) la posibilidad de incluir etiquetas personalizadas de CSS, Javascript y metadatos[ a través de una configuración consciente del contexto;](/help/developing/including-clientlibs.md#context-aware-loading) y una utilidad `DataLayerBuilder` para [simplificar la integración de la capa de datos en los componentes personalizados.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 29 de octubre de 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Esta versión introdujo la [compatibilidad con AMP.](/help/developing/amp.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 20 de julio de 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Esta versión introdujo el componente [Visor de PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Continua | 8, 11 | 17 de junio de 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Esta versión habilitó la integración con la [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md) e introdujo el componente [barra de progreso.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Continua | 8, 11 | 29 de mayo de 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Esta versión se centró en correcciones con pequeñas mejoras. | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 5 de diciembre de 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Esta versión introdujo el nuevo [componente incrustado.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 25 de septiembre de 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versión introdujo el nuevo [componente Fragmento de experiencia.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Continua | 8, 11 | 6 de septiembre de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versión introdujo los nuevos [Acordeón,](/help/components/accordion.md) [Botón,](/help/components/button.md) [Contenedor,](/help/components/container.md) y [Descargar componentes.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8, 11 | 25 de junio de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versión introdujo el [componente Lista de fragmentos de contenido.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8, 11 | 7 de mayo de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versión se centró en los refinamientos de la [Biblioteca de componentes,](https://aemcomponents.dev) pero también contenía algunas mejoras en las características del [Componente separador.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Continua | 8 | 14 de marzo de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versión se centró en la [Biblioteca de componentes](https://aemcomponents.dev) e introdujo el nuevo [Componente separador,](/help/components/separator.md), pero también contenía algunas mejoras de características para el [Componente de imagen.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 de febrero de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versión se centró principalmente en la corrección de errores, pero también contenía algunas mejoras en las funciones del [Componente de carrusel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 de noviembre de 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Esta versión introdujo el [Componente de pestañas](/help/components/tabs.md) y el [Componente de carrusel](/help/components/carousel.md), así como mejoras en el [Componente de imagen](/help/components/image.md), el [Componente de página,](/help/components/page.md) y el [Componente de título](/help/components/title.md) y mejoró el seguimiento. | 6.4.2.0+ | - | - | 8 | 16 de octubre de 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Esta versión introdujo el [componente teaser](/help/components/teaser.md) junto con mejoras en el [componente de imagen](/help/components/image.md) y numerosas correcciones de errores. | 6.4.2.0+ | - | - | 8 | 13 de julio de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Esta fue una versión de corrección de errores. | 6.4.0.0+ | - | - | 8 | 12 de junio de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Esta versión añadió mejoras, correcciones de errores y pequeñas mejoras, incluida la compatibilidad con la inversión de imágenes en el [Componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Esta versión se centró principalmente en las mejoras en la parte inferior del capó, las correcciones de errores y algunas mejoras menores en el [Componente de imagen,](/help/components/image.md) [Componente de página,](/help/components/page.md) y [Componente de fragmento de contenido.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 de marzo de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | En esta versión se presentaron el [Componente de navegación,](/help/components/navigation.md) [Componente Navegación de idioma,](/help/components/language-navigation.md) y el [Componente de búsqueda rápida](/help/components/quick-search.md) y se implementó el [sistema de estilos](/help/get-started/authoring.md#component-styling) para todos los componentes. | 6.4.0.0+ | - | - | 8 | 16 de enero de 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Esta versión implementa la exportación de JSON en todos los componentes e introduce el [Componente de fragmento de contenido.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 de octubre de 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Esta versión agrega varias correcciones para el [Componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Esta versión agrega correcciones para el [Componente de página,](/help/components/page.md) [Componente de imagen,](/help/components/image.md) y varias correcciones y mejoras globales. | 6.4.0.0+ | - | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Esta versión agrega correcciones para imágenes GIF animadas en el [Componente de imagen.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 de marzo de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Versión inicial de los componentes principales. | 6.4.0.0+ | - | - | 7 | 20 de marzo de 2017 |

>[!TIP]
>
>Al igual que con AEM, Adobe recomienda que los desarrolladores utilicen la [última versión y las versiones de los componentes principales](https://github.com/adobe/aem-core-wcm-components/releases/latest) disponibles que sean compatibles con la versión de AEM que estén ejecutando para beneficiarse de las correcciones y funciones más actualizadas.

### Publicaciones y versiones de componentes {#component-versions-and-releases}

En la siguiente tabla se detallan las versiones de qué componentes se incluyen en qué versiones de los componentes principales.

|  | Versión 1.0.0: 1.0.6 | Versión 1.1.0 | Versión 2.0.0: 2.0.8 | Versión 2.1.0 | Versión 2.2.0-2.2.0 | Versión 2.3.0-2.3.2 | Versión 2.4.0 | Versión 2.5.0 | Versión 2.6.0 | Versión 2.7.0-2.8.0 | Versión 2.9.0-2.17.14 | Versión 2.18.0 | Versión 2.19.0 | Versión 2.20.0-2.21.2 | Versión 2.22.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Página](components/page.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 |
| **[Título](components/title.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 |
| **[Imagen](components/image.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 |
| **[Lista](components/list.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2, 3, y 4 |
| **[Ruta de navegación](components/breadcrumb.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 | Versiones 1, 2 y 3 |
| **[Compartir en medios sociales](components/sharing.md)** | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 obsoleta | Versión 1 obsoleta | Versión 1 obsoleta | Versión 1 obsoleta |
| **[Contenedor del formulario](components/forms/form-container.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Texto de formulario](components/forms/form-text.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Opciones de formulario](components/forms/form-options.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Formulario oculto](components/forms/form-hidden.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Botón de formulario](components/forms/form-button.md)** | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Fragmento de contenido](components/content-fragment-component.md)** |  | Zona protegida | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Navegación](components/navigation.md)** |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Navegación por idiomas](components/language-navigation.md)** |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Búsqueda rápida](components/quick-search.md)** |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Teaser](components/teaser.md)** |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Pestañas](components/tabs.md)** |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Carrusel](components/carousel.md)** |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Separador](components/separator.md)** |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Lista de fragmentos de contenido](components/content-fragment-list.md)** |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Acordeón](components/accordion.md)** |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Botón](components/button.md)** |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Contenedor](components/container.md)** |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Descargar](components/download.md)** |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Fragmento de experiencias](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Incrustar](components/embed.md)** |  |  |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 | Versión 1, versión 2 |
| **[Barra de progreso](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Visualizador de PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | Versión 1 | Versión 1 | Versión 1 | Versión 1 | Versión 1 |
| **[Tabla de contenido](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | Versión 1 | Versión 1 |

## Versiones y publicaciones {#versions-and-releases}

Los componentes principales se distribuyen a través de GitHub. Esto permite que Adobe agregue más rápidamente funcionalidades a los componentes y también permite la entrada de la comunidad fuera del ciclo de versiones de AEM.

Los componentes principales están disponibles con versiones de AEM definidas con las que son compatibles. Esto significa que una versión de AEM puede admitir varias versiones o publicaciones de los componentes principales.

### Versiones {#versions}

La iteración principal de los componentes principales son las **versiones**. Cada componente tiene una versión. Las versiones se identifican con **v** anexado con un entero positivo distinto de cero, como v1 y v2. Las versiones solo se incrementan para los cambios que no son compatibles con versiones anteriores, como suele ocurrir con la introducción de nuevas funciones y funcionalidades.

Los desarrolladores y administradores pueden reconocer las versiones de los componentes principales mediante una serie de rutas de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal tal como se define en la [guía de semántica de versiones](https://semver.org/).

Para obtener más información sobre las versiones de componentes principales, consulte la [documentación para desarrolladores de componentes principales](developing/guidelines.md).

### Publicaciones {#releases}

Los componentes principales están disponibles a través de las **versiones** y [representan los artefactos reales publicados disponibles en GitHub.](https://github.com/adobe/aem-core-wcm-components/releases) Las versiones se marcan con un número decimal del formato `X.Y.Z` y recopilan todos los componentes principales juntos como un paquete de entrega.

* Las **Versiones principales** introducen componentes completamente nuevos, mejoras en la versión existente de componentes, así como correcciones de errores estándar. Esto se representa mediante un incremento en el componente `X` del número de versión.
* Las **Versiones menores** introducen nuevos componentes, nuevas funcionalidades para las versiones existentes de componentes, así como correcciones de errores. Esto se representa mediante un incremento en el componente `Y` del número de versión.
* Las **versiones de parche** solo contienen las correcciones de errores. Esto se representa mediante un incremento en el componente `Z` del número de versión.

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

El énfasis de Adobe en el desarrollo ha cambiado los componentes principales y se seguirán añadiendo nuevas funciones.

[Casi todos los componentes de base han quedado obsoletos con AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=es) y solo se tendrán en cuenta las correcciones de errores importantes en los componentes de base a partir de ahora.
