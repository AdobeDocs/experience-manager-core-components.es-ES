---
title: Uso de los componentes principales de correo electrónico
description: Obtenga información sobre la instalación, configuración y uso básicos de los componentes principales de correo electrónico.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 4%

---


# Uso de los componentes principales de correo electrónico {#using}

Obtenga información sobre la instalación, configuración y uso básicos de los componentes principales de correo electrónico.

## Instalación de los componentes principales de correo electrónico {#installation}

Los componentes principales de correo electrónico se pueden usar con AEM 6.5. Consulte la [Sección Requisitos del documento de introducción a los componentes principales de correo electrónico](introduction.md#requirements) para obtener más información.

### Instalar componentes principales {#core-components}

Los componentes principales de correo electrónico se crean en los componentes principales de AEM. Como los componentes principales no se envían con AEM, primero debe instalar los componentes principales de AEM antes de instalar los componentes principales de correo electrónico.

Consulte la sección [Descargar e instalar](/help/get-started/using.md#download-and-install) del documento Uso de componentes principales para obtener más información sobre cómo instalar los componentes principales.

### Instalación de los componentes principales de correo electrónico {#email-core-components}

Una vez instalados los componentes principales en la instancia, también debe instalar los componentes principales de correo electrónico. Los componentes principales de correo electrónico aún no forman parte del tipo de archivo del proyecto AEM, por lo que deberá añadirlos manualmente al proyecto. Siga la documentación de [la wiki de componentes principales de correo electrónico de GitHub que se va a instalar.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

Puede seguir las mismas instrucciones si desea adaptar un proyecto existente para utilizar los componentes principales de correo electrónico.

## Configuración {#configuration}

Después de instalar los componentes principales, debe completar dos pasos de configuración importantes.

### Configuración de Campaign {#configure-campaign}

Debe configurar la integración AEM-Adobe Campaign para que las dos soluciones se comuniquen.

* Configurar la integración con Adobe Campaign
   * Adobe Campaign Classic: [Integración con Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard: [Integración con Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Vincular la configuración de integración de Adobe Campaign](/help/email/components/page.md#cloud-services-tab) a la página de contenido donde utilizará los componentes principales de correo electrónico

### Añadir AEM filtro de tipo de recurso para los componentes de correo electrónico {#aem-resource-filter}

Para que Adobe Campaign pueda procesar correos electrónicos basados en los componentes principales de correo electrónico, se debe ajustar un filtro en Campaign.

1. Inicie sesión en Adobe Campaign como administrador mediante la consola del cliente.

1. Select **Herramientas** -> **Explorer** en la barra de menús.

1. En el explorador, vaya a la **Administración** -> **Plataforma** -> **Opciones** nodo .

1. Seleccione el `AEMResourceTypeFilter` de la lista.

1. En el **Valor** campo, anexar `core/email/components/page/<v1>/page` si no está presente.

   * Reemplazar `<v1>` con la versión actual de los componentes principales de correo electrónico [Componente de página](/help/email/components/page.md) como `v1`.
   * Tenga en cuenta que los valores de la variable **Valores** El campo debe estar delimitado por comas.

1. Haga clic en **Guardar**.

## Uso de los componentes principales de correo electrónico {#using-components}

Una vez instalados los componentes de correo electrónico y configurada la integración con Adobe Campaign, puede utilizar los componentes de correo electrónico para crear contenido de correo electrónico en AEM y, a continuación, enviar ese contenido a los destinatarios mediante Adobe Campaign. A continuación se ofrece una descripción general del flujo de trabajo.

| Etapa | Descripción | Solución |
|---|---|---|
| 1 | Los autores crean una estructura jerárquica libre de carpetas y contenido de correo electrónico como páginas. | AEM |
| 2 | Al usar la variable [editor de plantillas,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) los autores configuran un encabezado y/o pie de página de correo electrónico que se compartiría entre todas las páginas de correo electrónico resultantes de esta plantilla de página. | AEM |
| 3 | Los autores utilizan la variable [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) para crear contenido de correo electrónico con el editor de texto, donde pueden elegir variables de Adobe Campaign y utilizar el componente Segmentación para mostrar información condicional si el destinatario cumple determinados criterios. | AEM |
| 4 | Cuando se complete el contenido del correo electrónico, [se ejecuta un flujo de trabajo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) para aprobar el contenido y enviarlo a Campaign. | AEM |
| 5 | Se crea una entrega que define una lista de destinatarios. | Campaign |
| 6 | El contenido creado en AEM se selecciona como contenido de la entrega. | Campaign |
| 7 | El contenido se envía a los destinatarios y reemplaza las variables de Adobe Campaign por la información personalizada de los destinatarios. | Campaign |

Para ver un ejemplo de la creación de contenido de correo electrónico en AEM y la entrega en Adobe Campaign, consulte los siguientes recursos.

* AEM as a Cloud Service: [Creación de boletines de campaña con AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/campaign/creating-newsletters.html)
* AEM 6.5: [Uso de Adobe Campaign Classic y Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)

