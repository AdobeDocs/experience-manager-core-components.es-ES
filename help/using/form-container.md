---
title: Componente de contenedor de formularios
description: El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# Componente de contenedor de formularios{#form-container-component}

El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.

## Uso {#usage}

El componente Contenedor del formulario permite crear formularios y funciones de envío de información simples mediante la compatibilidad con formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Mediante el cuadro de diálogo [de](#configure-dialog) configuración, el editor de contenido puede definir la acción desencadenada por el envío del formulario, dónde se debe almacenar el contenido enviado y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de](#design-dialog) diseño para definir los componentes permitidos y sus asignaciones de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de plantillas.

>[!NOTE]
>
>Los componentes principales Componente Contenedor de formulario solo admiten el uso de componentes principales de los componentes de formulario (botón, texto, oculto, etc.). No se admite el uso de componentes [](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) de base de formularios dentro del contenedor de formularios de componentes principales (y viceversa).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de formularios es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como servicio de nube |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](form-container-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor de formularios [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

![](assets/screen_shot_2018-01-12at122046.png)

Según el tipo **de** acción seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acciones disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar orden](#update-order)

Independientemente del tipo, hay una configuración [](#general-settings) general que se aplica a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo enviará un correo electrónico a los destinatarios designados.

![](assets/screen_shot_2018-01-12at122554.png)

* **Asunto** Asunto del correo electrónico que se enviará al enviar el formulario
* **Desde** la dirección de correo electrónico de origen del mensaje que se enviará al enviar el formulario
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

El cuadro de diálogo de diseño permite al autor de la plantilla definir los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de plantillas.
