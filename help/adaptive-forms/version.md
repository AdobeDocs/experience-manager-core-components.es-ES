---
title: Versiones de los componentes principales de AEM Forms
description: Los componentes principales de AEM se publican como versiones que pueden contener más de una versión de los mismos componentes principales. En este documento se explica cuáles son las versiones y publicaciones y cómo comprender la compatibilidad con los componentes principales y de AEM.
role: Architect, Developer, Admin, User
exl-id: 8146a5b1-acf6-4b54-ad6b-6e1747a137f6
source-git-commit: 5ba402a0f781f73fe7eb5afc9b4beb47ba28851e
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 91%

---

# Versiones de componentes principales {#core-components-versions}

La versión actual de los componentes principales 2.0.10 es compatible con [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es) y la versión 1.1.12 de los componentes principales es compatible con instalaciones de [AEM 6.5 Forms On-Premise y AMS](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=es).

## Historial de versiones de AEM as Cloud Service {#aem-as-cs-version-history}

La tabla siguiente presenta una lista de las versiones de los componentes principales compatibles con AEM as a Cloud Service que están disponibles en [GitHub, junto con detalles completos de sus versiones](https://github.com/adobe/aem-core-forms-components/releases).

| Versión | Descripción | AEM as a Cloud Service | Java™ | Fecha de lanzamiento |
|---|---|---|---|---|
| [2.0.76](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.76) | Con esta versión, la pestaña Estilo y la pestaña Propiedades personalizadas se corrigen para el componente Términos y condiciones. Esta versión también corrigió el componente de botón de radio para guardar el valor booleano para el primer clic. | Continua | 8, 11 | 15 de noviembre de 2023 |
| [2.0.74](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.74) | Con esta versión, el error de envío se actualiza para la acción de envío en AEM Forms. | Continua | 8, 11 | 15 de noviembre de 2023 |
| [2.0.70](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.70) | Esta versión agregó compatibilidad para administrar el idioma de la página de Sites en el contenedor de formularios. | Continua | 8, 11 | 10 de noviembre de 2023 |
| [2.0.64](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.64) | Admitir texto enriquecido para etiquetas para componentes de radio/casilla de verificación. Con esta versión, también se añade compatibilidad con el componente Switch. Esta versión también incluye correcciones para el componente Términos y condiciones. | Continua | 8, 11 | 6 de noviembre de 2023 |
| [2.0.62](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.62) | Con esta versión, se añade la compatibilidad con el componente Términos y condiciones. También se ha agregado compatibilidad con Nombres cualificados en los componentes principales. | Continua | 8, 11 | 16 de octubre de 2023 |
| [2.0.60](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.60) | Esta versión incluye correcciones relacionadas con la funcionalidad de propiedades personalizadas, el Asistente y el componente Selector de fecha. | Continua | 8, 11 | 12 de septiembre de 2023 |
| [2.0.56](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.56) | Con esta versión, se añade compatibilidad con las propiedades personalizadas de todos los componentes principales. | Continua | 8, 11 | 12 de septiembre de 2023 |
| [2.0.54](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.54) | Esta versión solucionó el problema relacionado con la localización con el componente Selector de fecha. | Continua | 8, 11 | 30 de agosto de 2023 |
| [2.0.52](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.52) | Compatibilidad con el uso del componente Casilla de verificación en un formulario adaptable. | Continua | 8, 11 | 25 de agosto de 2023 |
| [2.0.50](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.50) | Se ha agregado compatibilidad con fragmentos de formulario en un Formulario adaptable con esta versión. | Continua | 8, 11 | 4 de agosto de 2023 |
| [2.0.48](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.48) | Las principales mejoras de esta versión están relacionadas con el rendimiento de Lighthouse. | Continua | 8, 11 | 25 de julio de 2023 |
| [2.0.42](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.42) | La versión incorpora mejoras al final de la programación. | Continua | 8, 11 | 18 de julio de 2023 |
| [2.0.38](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.38) | La funcionalidad de accesibilidad se ha mejorado con esta versión. | Continua | 8, 11 | 17 de julio de 2023 |
| [2.0.36](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.36) | Con esta versión, puede utilizar el controlador de error personalizado mediante el servicio de invocación del Editor de reglas. | Continua | 8, 11 | 3 de julio de 2023 |
| [2.0.34](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.34) | Se ha agregado compatibilidad con la localización para los mensajes de error predeterminados junto con el botón Agregar/Quitar para el componente Repetible. | Continua | 8, 11 | 28 de junio de 2023 |
| [2.0.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.32) | Con esta versión, se añade compatibilidad con Captcha para Formularios adaptables. | Continua | 8, 11 | 15 de junio de 2023 |
| [2.0.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.26) | Compatibilidad para agregar Formularios adaptables en AEM Sites. | Continua | 8, 11 | 7 de junio de 2023 |
| [2.0.18](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.18) | Con esta versión, se ofrece compatibilidad para una repetibilidad del componente Acordeón. También se ha añadido un nuevo componente como pestañas verticales. | Continua | 8, 11 | 5 de junio de 2023 |
| [2.0.10](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.10) | Con esta versión, se introduce la compatibilidad con un componente Contenedor de formularios adaptables en el editor de Sites. | Continua | 8, 11 | 17 de marzo de 2023 |
| [2.0.8](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.8) | En esta versión se ha introducido la funcionalidad de repetibilidad del componente del asistente. | Continua | 8, 11 | 3 de marzo de 2023 |
| [2.0.6](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | En esta versión se han introducido varios formatos para el componente principal de entrada numérica. | Continua | 8, 11 | 08 de febrero de 2023 |
| [2.0.4](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-2.0.6) | En esta versión se ha introducido compatibilidad con los componentes principales de AEM as a Cloud Service. | Continua | 8, 11 | 30 de enero de 2023 |

## Historial de versiones de AEM 6.5 Forms {#aem-as-form-version-history}

La tabla siguiente presenta una lista de las versiones de los componentes principales compatibles con AEM 6.5 Forms On-Premise y AMS disponibles en [GitHub, junto con detalles completos de sus versiones](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12).

| Versión | Descripción | AEM 6.4 | AEM 6.5 | Java™ | Fecha de lanzamiento |
|---|---|---|---|---|---|
| [1.1.32](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.32) | Esta versión actualizó la información del paquete de información del Service Pack 6.5.18.0 de AEM. | - | 6.5.16.0+ | 8, 11 | 15 de octubre de 2023 |
| [1.1.28](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.28) | Admitir texto enriquecido para etiquetas para componentes de radio/casilla de verificación. Esta versión también incluye compatibilidad con el componente Términos y condiciones y los componentes del conmutador. | - | 6.5.16.0+ | 8, 11 | 15 de octubre de 2023 |
| [1.1.26](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.26) | Con esta versión, se ha añadido la compatibilidad con el componente Casilla de verificación para formularios adaptables y fragmentos de formulario. También incluye mejoras en el rendimiento de Lighthouse. En esta versión también se incluye el controlador de error personalizado que utiliza el servicio de invocación del Editor de reglas. | - | 6.5.16.0+ | 8, 11 | 15 de octubre de 2023 |
| [1.1.24](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.24) | Se ha agregado compatibilidad con la localización para los mensajes de error predeterminados junto con el botón Agregar/Quitar para el componente Repetible. También se ha agregado compatibilidad con recaptcha en Formularios adaptable. | - | 6.5.16.0+ | 8, 11 | 29 de junio de 2023 |
| [1.1.22](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.22) | Compatibilidad para agregar formularios adaptables en AEM Sites. Pestaña Elementos agregados en el cuadro de diálogo de edición del componente Pestañas verticales y Asistente. | - | 6.5.16.0+ | 8, 11 | 7 de junio de 2023 |
| [1.1.12](https://github.com/adobe/aem-core-forms-components/releases/tag/core-forms-components-reactor-1.1.12) | En esta versión se ha introducido la compatibilidad con los componentes principales de AEM Forms On-Premise y AMS. | - | 6.5.16.0+ | 8, 11 | 08 de febrero de 2023 |

## Vea también {#see-also}

{{see-also}}