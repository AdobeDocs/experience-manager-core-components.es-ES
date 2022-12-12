---
title: Introducción a los componentes principales de correo electrónico
description: Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 88%

---


# Introducción a los componentes principales de correo electrónico {#email-core-components-introduction}

Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.

## Información general {#overview}

Los componentes principales de correo electrónico se crean sobre la misma base sólida de los componentes principales. Permiten generar contenidos de correo electrónico de forma sencilla y flexible, arrastrando y soltando, que luego pueden entregarse a la audiencia gracias a la potencia de Adobe Campaign.

## Ventajas {#benefits}

Los correos electrónicos forman parte de la experiencia de marca y del recorrido del cliente. Con los componentes principales de correo electrónico, los autores pueden crear contenido de correo electrónico desde AEM, lo que ofrece una experiencia de marca uniforme y, por lo tanto, aumenta la velocidad de contenido.

* Al igual que las páginas de creación con los componentes principales, los componentes principales de correo electrónico permiten a los autores montar correos electrónicos sin conocimientos técnicos, siempre que sigan las directrices de promoción de la marca.
* La capacidad de reutilizar activos y contenido también anima a los autores a seguir las directrices de promoción de la marca y optimizar el proceso de creación de contenido.

## Características {#features}

* Los componentes principales de correo electrónico se basan en los [componentes principales](/help/introduction.md) y, por tanto, también admiten las [plantillas editables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y el [sistema de estilos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=es)
* Hay [diez componentes listos para la producción y optimizados para correo electrónico](#components) que permiten crear contenido de correo electrónico.
* Los componentes principales de correo electrónico proporcionan una personalización avanzada gracias a la inserción de [Variables de Adobe Campaign](campaign-variables.md) en la mayoría de los campos de diálogo.
* El [Componente de segmentación](/help/email/components/segmentation.md) permite una segmentación avanzada del contenido.
* Los componentes principales de correo electrónico proporcionan un resultado HTML ideal para el correo electrónico gracias al [inliner de estilos CSS,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Documentación técnica) [el inliner de atributos HTML](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) y [el saneador de HTML.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Puede crear contenido de correo electrónico en cualquier parte bajo `/content`.
* Los componentes principales de correo electrónico son de [código abierto.](https://github.com/adobe/aem-core-email-components)

## Requisitos  {#requirements}

Los componentes principales de correo electrónico tienen los siguientes requisitos:

| AEM | Adobe Campaign | Componentes principales  |
|---|---|---|
| AEM 6.5.14.0+<br>On-Premise o AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versión 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Como las integraciones de Adobe Campaign no son compatibles con AEM as a Cloud Service, los componentes principales de correo electrónico tampoco son compatibles con AEM as a Cloud Service.

## Los componentes de correo electrónico {#components}

La versión actual de los componentes principales de correo electrónico contiene los siguientes componentes.

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

Consulte el documento [Uso de los componentes principales de correo electrónico](using.md) para obtener más información sobre la instalación de los componentes principales de correo electrónico.
