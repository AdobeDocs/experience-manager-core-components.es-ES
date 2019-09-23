---
title: Componente de contenedor de formularios
seo-title: Componente de contenedor de formularios
description: nulo
seo-description: El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.
uuid: 9d556daf-3fe7-4b2a-b5ae-6926acb267a9
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: 3d33fe60-a0ac-4ff2-a865-d600b5448aeb
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Componente de contenedor de formularios{#form-container-component}

El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.

## Uso {#usage}

El componente Contenedor del formulario permite crear formularios y funciones de envío de información simples mediante la compatibilidad con formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Mediante el cuadro de diálogo [de](#configure-dialog) configuración, el editor de contenido puede definir la acción desencadenada por el envío del formulario, dónde se debe almacenar el contenido enviado y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de](#design-dialog) diseño para definir los componentes permitidos y sus asignaciones de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)de plantillas.

>[!NOTE]
>
>Los componentes principales Componente Contenedor de formulario solo admiten el uso de componentes principales de los componentes de formulario (botón, texto, oculto, etc.). Using foundation components form components within the core components form container (and vice versa) is not supported.[](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html)

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de formularios es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

| Component Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-container-v1.md) | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document Core Components Versions.[](versions.md)

## Technical Details {#technical-details}

The latest technical documentation about the Form Container Component can be found on GitHub.[](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container)

Further details about developing Core Components can be found in the Core Components developer documentation.[](developing.md)

## Configure Dialog {#configure-dialog}

The configure dialog allows the content author to define what actions are taken when the component is submitted.

![](assets/screen_shot_2018-01-12at122046.png)

Depending on the selected Action Type, the available options within the container will change. **** The available action types are:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar orden](#update-order)

Independientemente del tipo, hay una configuración [](#general-settings) general que se aplica a cada acción.

### Correo {#mail}

When the form is submitted, the mail action type will send an email to designated recipients.

![](assets/screen_shot_2018-01-12at122554.png)

* **Subject
The subject of the email that will be sent on form submission**
* **From
The from email address of the email that will be send on form submission**
* **A** Las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario

   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico
* **CC** Las direcciones de los destinatarios que recibirán una copia de carbono del correo electrónico enviado al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacena en una ubicación de repositorio designada.

![](assets/screen_shot_2018-01-12at122538.png)

* **Ruta** del contenido Ruta del repositorio del contenido donde se almacena el contenido enviado
* **Ver datos** Toque o haga clic para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo** Configure para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

### Enviar pedido {#submit-order}

Cuando se envía el formulario, se envía el pedido.

![](assets/chlimage_1-3.png)

### Actualizar orden {#update-order}

Cuando se envía el formulario, se actualiza el pedido.

![](assets/chlimage_1-4.png)

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![](assets/chlimage_1-5.png)

El usuario será redireccionado a la página especificada después de completar el envío del formulario.

* Utilice el cuadro de diálogo Selección para seleccionar un recurso en AEM.
* Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
* Deje en blanco para volver a mostrar el formulario después del envío.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)de plantillas.