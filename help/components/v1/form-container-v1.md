---
title: Componente contenedor de formularios (v1)
description: El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.
index: n
translation-type: tm+mt
source-git-commit: 68472ab548fb6ebb443a06c12e7b37797a0c1302

---


# Form Container Component (v1) {#form-container-component-v1}

El componente Contenedor de formularios de componentes principales permite la creación de formularios de envío simples.

## Uso {#usage}

El componente Contenedor de formularios permite crear formularios y funciones de envío de información simples mediante la compatibilidad con formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Mediante el cuadro de [diálogo](#settings-dialog) de configuración, el editor de contenido puede definir qué tipo de acción desencadena el envío de formularios, dónde se debe almacenar el contenido enviado y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de](#design-dialog) diseño para definir los componentes permitidos y sus asignaciones de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html)de plantillas.

## Versión y compatibilidad {#version-and-compatibility}

En este documento se describe la versión 1 del componente Contenedor de formularios, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Contenedor de formularios.

| Versión de AEM | Contenedor de formularios v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Contenedor de formulario.
>
>Para obtener más información sobre la versión actual del componente Contenedor de formularios, consulte el documento Componente [Contenedor de](/help/components/forms/form-container.md) formularios.

## Cuadro de diálogo Configuración {#settings-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan al enviar el componente.

![](/help/assets/chlimage_1.png)

Según el tipo **de** acción seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acciones disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar orden](#update-order)

Independientemente del tipo, hay una configuración [](#general-settings) general que se aplica a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo enviará un correo electrónico a los destinatarios designados.

![](/help/assets/chlimage_1-1.png)

* **Asunto** : el asunto del correo electrónico que se enviará al enviar el formulario
* **Desde** : la dirección de correo electrónico de origen del correo electrónico que se enviará al enviar el formulario
* **Para** : las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico
* **CC** : las direcciones de los destinatarios que recibirán una copia del correo electrónico enviado al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacena en una ubicación de repositorio designada.

![](/help/assets/chlimage_1-2.png)

* **Ruta** de contenido: Ruta del repositorio de contenido donde se almacena el contenido enviado
* **Ver datos** : toque o haga clic para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo** : configurar para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

### Enviar pedido {#submit-order}

Cuando se envía el formulario, se envía el pedido.

![](/help/assets/chlimage_1-3.png)

### Actualizar orden {#update-order}

Cuando se envía el formulario, se actualiza el pedido.

![](/help/assets/chlimage_1-4.png)

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![](/help/assets/chlimage_1-5.png)

El usuario será redireccionado a la página especificada después de completar el envío del formulario.

* Utilice el cuadro de diálogo Selección para seleccionar un recurso en AEM.
* Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
* Deje en blanco para volver a mostrar el formulario después del envío.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843)de plantillas.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor de formularios [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.
