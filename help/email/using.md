---
title: Uso de los componentes principales de correo electrónico
description: Obtenga información acerca de la instalación, configuración y uso básicos de los componentes principales de correo electrónico.
role: Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
index: false
TQID: https://experienceleague.adobe.com/wNHEXDBErMNRfSs-N6vAhQl9jnzMJJnGTPBUFEMZHY8
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a642c50e-80eb-4fc1-a5d2-f3762d1f841did: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2: id: a6c0bfb4-91d0-4952-9c1d-c7f39e7705c4id: de0934a4-5275-4727-b871-497a72ae8500
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 683
ht-degree: 100%

---

# Uso de los componentes principales de correo electrónico {#using}

Obtenga información acerca de la instalación, configuración y uso básicos de los componentes principales de correo electrónico.

## Instalación de los componentes principales de correo electrónico {#installation}

Los componentes principales del correo electrónico se pueden utilizar con AEM 6.5. Consulte la [sección Requisitos del documento de introducción a los componentes principales de correo electrónico](introduction.md#requirements) para obtener más información.

### Instalación de componentes principales {#core-components}

Los componentes principales de correo electrónico se basan en los componentes principales de AEM. Como los componentes principales no se entregan con AEM 6.5, primero debe instalarlos, antes de instalar los componentes principales del correo electrónico.

Consulte la sección [Descarga e instalación](/help/get-started/using.md#download-and-install) del documento Uso de los componentes principales para obtener más información sobre cómo instalar los componentes principales.

### Instalación de los componentes principales de correo electrónico {#email-core-components}

Una vez instalados los componentes principales en la instancia, también debe instalar los componentes principales de correo electrónico. Los componentes principales de correo electrónico aún no forman parte del Arquetipo de proyecto de AEM, por lo que deberá añadirlos manualmente al proyecto. Siga la documentación de [la wiki de los componentes principales de correo electrónico de GitHub que se van a instalar.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Puede seguir las mismas instrucciones si desea adaptar un proyecto existente para utilizar los componentes principales de correo electrónico.

## Configuración {#configuration}

Después de instalar los componentes principales, debe completar dos pasos de configuración importantes.

### Configuración de Campaign {#configure-campaign}

Debe configurar la integración de AEM y Adobe Campaign para que las dos soluciones se comuniquen.

* Configuración de la integración con Adobe Campaign
   * Adobe Campaign Classic: [Integración con Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=es)
   * Adobe Campaign Standard: [Integración con Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=es)
* [Vincule la configuración de integración de Adobe Campaign](/help/email/components/page.md#cloud-services-tab) a la página de contenido donde utilizará los componentes principales de correo electrónico

### Adición de un filtro de tipo de recurso de AEM para los componentes de correo electrónico {#aem-resource-filter}

Para que Adobe Campaign pueda procesar correos electrónicos basados en los componentes principales de correo electrónico, se debe ajustar un filtro en Campaign.

1. Inicie sesión en Adobe Campaign como administrador mediante la consola del cliente.

1. Seleccione **Herramientas** -> **Explorador** en la barra de menús.

1. En el explorador, vaya al nodo **Administración** -> **Plataforma** -> **Opciones**.

1. Seleccione la opción `AEMResourceTypeFilter` en la lista.

1. En el campo **Valor**, anexe `core/email/components/page/<v1>/page` si no está presente.

   * Reemplace `<v1>` con la versión actual del [componente Página](/help/email/components/page.md) de los componentes principales de correo electrónico, como `v1`.
   * Tenga en cuenta que los valores del campo **Valores** deben estar delimitados por comas.

1. Haga clic en **Guardar**.

## Uso de los componentes principales de correo electrónico {#using-components}

Una vez instalados los componentes de correo electrónico y configurada la integración con Adobe Campaign, puede utilizar los componentes de correo electrónico para crear contenido de correo electrónico en AEM y, a continuación, enviar ese contenido a los destinatarios mediante Adobe Campaign. A continuación se ofrece una descripción general del flujo de trabajo.

| Paso | Descripción | Solución |
|---|---|---|
| 1 | Los autores crean una estructura jerárquica de carpetas y contenidos de correo electrónico de forma libre como páginas. | AEM |
| 2 | Con el [editor de plantillas,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) los autores configuran un encabezado o pie de página de correo electrónico que se compartiría entre todas las páginas de correo electrónico resultantes de esta plantilla de página. | AEM |
| 3 | Los autores utilizan el [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=es) para crear contenido de correo electrónico con el editor de texto, donde pueden elegir variables de Adobe Campaign y utilizar el componente Segmentación para mostrar información condicional si el destinatario cumple determinados criterios. | AEM |
| 4 | Cuando se complete el contenido del correo electrónico, [se ejecuta un flujo de trabajo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=es) para aprobarlo y enviarlo a Campaign. | AEM |
| 5 | Se crea un envío que define una lista de destinatarios. | Campaign |
| 6 | El contenido creado en AEM se selecciona como contenido del envío. | Campaign |
| 7 | El contenido se envía a los destinatarios y reemplaza las variables de Adobe Campaign por la información personalizada de los destinatarios. | Campaign |

Para ver un ejemplo de creación de contenido de correo electrónico en AEM y entrega en Adobe Campaign, consulte los siguientes recursos.

* AEM 6.5: [Trabajo con Adobe Campaign Classic y Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=es)
