---
title: Introducción a los componentes principales de correo electrónico
description: Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 9%

---


# Introducción a los componentes principales de correo electrónico {#email-core-components-introduction}

Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.

## Información general {#overview}

Los componentes principales de correo electrónico se crean sobre la misma base sólida de los componentes principales. Permiten una creación sencilla y flexible de arrastrar y soltar contenido de correo electrónico que se puede entregar a la audiencia mediante el poder de Adobe Campaign.

## Ventajas {#benefits}

Los correos electrónicos forman parte de la experiencia de marca y del recorrido del cliente. Con los componentes principales de correo electrónico, los autores pueden crear contenido de correo electrónico desde AEM, lo que ofrece una experiencia de marca uniforme y, por lo tanto, aumenta la velocidad de contenido.

* Al igual que las páginas de creación con los componentes principales, los componentes principales de correo electrónico permiten a los autores crear correos electrónicos sin conocimientos técnicos, siempre que sigan las directrices de marca.
* La capacidad de reutilizar recursos y contenido también anima a los autores a seguir las directrices de promoción de la marca y optimizar el proceso de creación de contenido.

## Características {#features}

* Los componentes principales de correo electrónico se basan en la variable [Componentes principales,](/help/introduction.md) y, por tanto, [Plantillas editables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y [Sistema de estilos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=es)
* Hay [diez componentes listos para la producción optimizados para el correo electrónico](#components) para crear contenido de correo electrónico.
* Los componentes principales de correo electrónico proporcionan una personalización avanzada gracias a la inserción de [Variables de Adobe Campaign](campaign-variables.md) en la mayoría de los campos de diálogo.
* El [Componente de segmentación](/help/email/components/segmentation.md) permite una segmentación avanzada del contenido.
* Los componentes principales de correo electrónico proporcionan una salida óptima para el HTML que facilita el correo electrónico gracias al [estilos CSS inliner,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [el HTML atributo inliner,](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) y [el HTML sanitizer.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Puede crear contenido de correo electrónico en cualquier parte inferior `/content`.
* Los componentes principales de correo electrónico son [código abierto.](https://github.com/adobe/aem-core-email-components)

## Requisitos  {#requirements}

Los componentes principales de correo electrónico tienen los siguientes requisitos:

| AEM | Adobe Campaign | Componentes principales  |
|---|---|---|
| AEM 6.5.14.0+<br>On-Premise o AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versión 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Como las integraciones de Adobe Campaign no son compatibles con AEM as a Cloud Service, los componentes principales de correo electrónico tampoco son compatibles con AEM as a Cloud Service.

## Los componentes de correo electrónico {#components}

La versión actual de los componentes principales de correo electrónico incluye los siguientes componentes.

* [Página](components/page.md)
* [Contenedor](components/container.md)
* [Título](components/title.md)
* [Texto](components/text.md)
* [Imagen](components/image.md)
* [Botón](components/button.md)
* [Teaser](components/teaser.md)
* [Fragmento de experiencias](components/experience-fragment.md)
* [Fragmento de contenido](components/content-fragment.md)
* [Segmentación](components/segmentation.md)

## Instalación y uso {#installation-usage}

Consulte la [Uso de los componentes principales de correo electrónico](using.md) documento para obtener más información sobre la instalación de los componentes principales de correo electrónico.
