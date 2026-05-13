---
title: Introducción a los componentes principales de correo electrónico
description: Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.
role: Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
index: false
TQID: https://experienceleague.adobe.com/PLDfeItW57FUgvSUO7kHgeNP8KogBwVA2AeEd-srbwg
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: ae478996-b206-4712-9b0c-dc78a2644453
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
subfeature_v2:
  - id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 439
ht-degree: 100%

---

# Introducción a los componentes principales de correo electrónico {#email-core-components-introduction}

Cree contenido de correo electrónico atractivo con la flexibilidad de los componentes principales de correo electrónico y envíelo con la potencia de Adobe Campaign.

## Información general {#overview}

Los componentes principales de correo electrónico se crean sobre la misma base sólida de los componentes principales. Permiten generar contenidos de correo electrónico de forma sencilla y flexible, arrastrando y soltando, que luego pueden entregarse al público gracias a la potencia de Adobe Campaign.

## Ventajas {#benefits}

Los correos electrónicos forman parte de la experiencia de marca y del recorrido del cliente. Con los componentes principales de correo electrónico, los autores pueden crear contenido de correo electrónico desde AEM, lo que ofrece una experiencia de marca uniforme y, por lo tanto, aumenta la velocidad de contenido.

* Al igual que las páginas de creación con los componentes principales, los componentes principales de correo electrónico permiten a los autores montar correos electrónicos sin conocimientos técnicos, siempre que sigan las directrices de promoción de la marca.
* La capacidad de reutilizar activos y contenido también anima a los autores a seguir las directrices de promoción de la marca y optimizar el proceso de creación de contenido.

## Características {#features}

* Los componentes principales de correo electrónico se basan en los [componentes principales](/help/introduction.md) y, por tanto, también admiten las [plantillas editables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y el [sistema de estilos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=es)
* Hay [diez componentes listos para la producción y optimizados para correo electrónico](#components) que permiten crear contenido de correo electrónico.
* Los componentes principales del correo electrónico proporcionan una personalización avanzada gracias a la inserción de las [variables de Adobe Campaign](campaign-variables.md) en la mayoría de los campos de diálogo.
* El componente flexible [Segmentación](/help/email/components/segmentation.md) permite una segmentación avanzada de sus contenidos.
* Los componentes principales de correo electrónico proporcionan un resultado HTML ideal para el correo electrónico gracias al [inliner de estilos CSS,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [el inliner de atributos HTML](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) y [el saneador de HTML.](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)
* Puede crear contenido de correo electrónico en cualquier parte bajo `/content`.
* Los componentes principales de correo electrónico son de [código abierto.](https://github.com/adobe/aem-core-email-components)

## Requisitos {#requirements}

Los componentes principales de correo electrónico tienen los siguientes requisitos:

| AEM | Adobe Campaign | Componentes principales |
|---|---|---|
| AEM 6.5.14.0+<br>Local o AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [Versión 2.21.2](/help/versions.md)+ |

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
