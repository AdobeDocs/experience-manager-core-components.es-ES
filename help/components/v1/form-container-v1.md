---
title: Componente contenedor de formulario (v1)
description: El componente Contenedor de formulario de componente principal permite la creación de formularios de envío simples.
index: n
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 3%

---


# Componente contenedor de formularios (v1) {#form-container-component-v1}

El componente Contenedor de formulario de componente principal permite la creación de formularios de envío simples.

## Uso {#usage}

El componente Contenedor de formulario permitió crear formularios y funciones de envío de información sencilla mediante la compatibilidad de formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Al utilizar el [cuadro de diálogo de configuración](#settings-dialog), el editor de contenido puede definir qué tipo de acción deben utilizarse para enviar déclencheur, dónde debe almacenarse el contenido enviado y si debe activarse un flujo de trabajo. El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los componentes permitidos y sus asignaciones similares al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Contenedor de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Contenedor de formulario.

| Versión de AEM | Componente contenedor de formulario v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente contenedor de formularios.
>
>Para obtener más información sobre la versión actual del componente contenedor de formularios, consulte el documento [Componente contenedor de formularios](/help/components/forms/form-container.md).

## Diálogo de configuración {#settings-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

![](/help/assets/chlimage_1.png)

Según el **Tipo de acción** seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acción disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar orden](#update-order)

Independientemente del tipo, existen [configuraciones generales](#general-settings) que se aplican a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo envía un correo electrónico a los destinatarios designados.

![](/help/assets/chlimage_1-1.png)

* **Asunto** : el asunto del correo electrónico que se enviará en el envío del formulario
* **Desde** : la dirección de correo electrónico de origen del correo electrónico que se enviará en el envío del formulario.
* **To** : las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario
   * Toque o haga clic en el botón **Add** para añadir direcciones adicionales
   * Toque o haga clic en el botón **Delete** para eliminar una dirección de correo electrónico
* **CC** : las direcciones de los destinatarios que recibirán una copia del correo electrónico enviado al enviar el formulario.
   * Toque o haga clic en el botón **Add** para añadir direcciones adicionales
   * Toque o haga clic en el botón **Delete** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacena en una ubicación designada del repositorio.

![](/help/assets/chlimage_1-2.png)

* **Ruta de contenido** : ruta del repositorio de contenido en la que se almacena el contenido enviado
* **Ver datos** : toque o haga clic para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo** : configure para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

### Enviar pedido {#submit-order}

Cuando se envía el formulario, se envía la solicitud.

![](/help/assets/chlimage_1-3.png)

### Actualizar orden {#update-order}

Cuando se envía el formulario, se actualiza la solicitud.

![](/help/assets/chlimage_1-4.png)

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![](/help/assets/chlimage_1-5.png)

Se redirigirá al usuario a la página especificada tras completar el envío del formulario.

* Utilice el cuadro de diálogo Selección para seleccionar un recurso dentro de AEM.
* Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
* Deje en blanco para volver a mostrar el formulario después del envío.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [del contenedor de formularios se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
