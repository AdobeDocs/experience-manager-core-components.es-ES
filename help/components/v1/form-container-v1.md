---
title: Componente Contenedor de formularios (versión 1)
description: El componente principal Contenedor de formularios permite crear formularios de envío simples.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Contenedor de formularios (versión 1) {#form-container-component-v1}

El componente principal Contenedor de formularios permite crear formularios de envío simples.

## Uso {#usage}

El componente Contenedor de formularios permite crear formularios y funciones de envío de información sencilla mediante la compatibilidad de formularios WCM simples y el uso de una estructura anidada para admitir componentes de formulario adicionales.

Al utilizar el [cuadro de diálogo de configuración](#settings-dialog), el editor de contenido puede definir qué tipo de formulario de acción se debe enviar, dónde debe almacenarse el contenido enviado y si debe activarse un flujo de trabajo. El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los componentes permitidos y sus asignaciones similares al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/siteandpage/templates.html?lang=es).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Contenedor de formularios, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de la versión 1 del componente Contenedor de formularios.

| Versión de AEM | Componente Contenedor de formularios (versión 1) |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Contenedor de formularios.
>
>Para obtener más información sobre la versión actual del componente Contenedor de formularios, consulte el documento [Componente Contenedor de formularios](/help/components/forms/form-container.md).

## Cuadro de diálogo de configuración {#settings-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

![](/help/assets/chlimage_1.png)

Según el **Tipo de acción** seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acción disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar pedido](#update-order)

Independientemente del tipo, existen [configuraciones generales](#general-settings) que se aplican a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo envía un correo electrónico a los destinatarios designados.

![](/help/assets/chlimage_1-1.png)

* **Asunto**: el asunto del correo electrónico que se enviará junto con el formulario
* **Desde**: la dirección de correo electrónico de origen desde la que se enviará el formulario
* **Hasta**: las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario
   * Pulse o haga clic en el botón **Añadir** para añadir direcciones adicionales
   * Pulse o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico
* **CC**: las direcciones de los destinatarios que recibirán una copia del correo electrónico enviado al enviar el formulario.
   * Pulse o haga clic en el botón **Añadir** para añadir direcciones adicionales
   * Pulse o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envíe el formulario, su contenido se almacenará en una ubicación designada del repositorio.

![](/help/assets/chlimage_1-2.png)

* **Ruta de contenido**: ruta del repositorio de contenido donde se almacena el contenido enviado
* **Ver datos**: pulse o haga clic en esta opción para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo**: configúrelo para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

### Enviar pedido {#submit-order}

Cuando se envía el formulario, se envía la solicitud.

![](/help/assets/chlimage_1-3.png)

### Actualizar pedido {#update-order}

Cuando se envía el formulario, se actualiza la solicitud.

![](/help/assets/chlimage_1-4.png)

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![](/help/assets/chlimage_1-5.png)

Se redirigirá al usuario a la página especificada tras completar el envío del formulario.

* Utilice el cuadro de diálogo de selección para seleccionar un recurso dentro de AEM.
* Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
* Deje este espacio en blanco para volver a mostrar el formulario después del envío.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/siteandpage/templates.html?lang=es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [Contenedor de formularios se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
