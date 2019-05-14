---
title: Componente Contenedor de formulario (v 1)
seo-title: Componente Contenedor de formulario (v 1)
description: El componente Contenedor de formulario de componente principal permite crear formularios de envío sencillos.
seo-description: El componente Contenedor de formulario de componente principal permite crear formularios de envío sencillos.
uuid: 075 d 83 ed-de 40-414 e-a 18 f -46 b 3 a 857 acba
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 800 c 064 e -2 ad 5-41 f 3-9 cef-b 025 a 555 efd 9
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente Contenedor de formulario (v 1){#form-container-component-v}

El componente Contenedor de formulario de componente principal permite crear formularios de envío sencillos.

## Uso {#usage}

El componente Contenedor de formulario habilitaba la creación de formularios y funciones de envío sencillos de información, ya que admitía formularios sencillos de WCM y utilizaba una estructura anidada para permitir componentes adicionales de formulario.

Mediante el uso del [cuadro de diálogo](form-container-v1.md#main-pars_title) de configuración, el editor de contenido puede definir el tipo de activador de envío de formularios de acción, donde se debe almacenar el contenido enviado y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de diseño](form-container-v1.md#main-pars_title_1995166862) para definir los componentes y sus asignaciones de forma similar al cuadro de diálogo de diseño del contenedor [de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Contenedor de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de la versión 1 del componente Contenedor de formulario.

| Versión de AEM | Componente Contenedor de formulario v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Contenedor de formulario.
>
>Para obtener más información sobre la versión actual del componente Contenedor de formulario, consulte [el documento Componente](form-container.md) Contenedor de formulario.

## Cuadro de diálogo de configuración {#settings-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir qué acciones se toman cuando se envía el componente.

![](assets/chlimage_1.png)

Según el tipo **de acción seleccionado**, las opciones disponibles dentro del contenedor cambiarán. Los tipos de acción disponibles son:

* [Correo](form-container-v1.md#main-pars_title_966511656)
* [Almacenar contenido](form-container-v1.md#main-pars_title_2065985840)
* [Enviar pedido](form-container-v1.md#main-pars_title_686874527)
* [Actualizar orden](form-container-v1.md#main-pars_title_410109286)

Independientemente del tipo, existen ajustes [generales](form-container-v1.md#main-pars_title_375403046) que se aplican a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción enviará un correo electrónico a los destinatarios designados.

![](assets/chlimage_1-1.png)

* **Asunto** : Asunto del correo electrónico que se enviará al envío del formulario
* **Desde** - La dirección de correo electrónico del correo electrónico que se enviará al envío del formulario
* **A** - Las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el **botón Eliminar** para eliminar una dirección de correo electrónico
* **CC** - Las direcciones de destinatarios que recibirán una copia en carbono el correo electrónico enviado al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el **botón Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacenará en una ubicación del repositorio designada.

![](assets/chlimage_1-2.png)

* **Ruta** de contenido: Ruta del repositorio de contenido donde se almacena el contenido enviado
* **Ver datos** : toque o haga clic para ver los datos enviados enviados como JSON
* **Iniciar flujo de trabajo** : Configurar para iniciar un flujo de trabajo con el contenido almacenado como carga útil al enviar el formulario

### Enviar pedido {#submit-order}

Cuando se envía el formulario, se enviará el pedido.

![](assets/chlimage_1-3.png)

### Actualizar orden {#update-order}

Cuando se envía el formulario, se actualizará el pedido.

![](assets/chlimage_1-4.png)

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![](assets/chlimage_1-5.png)

Tras la finalización del envío del formulario, se redirigirá al usuario a la página especificada.

* Utilice el cuadro de diálogo Selección para seleccionar un recurso dentro de AEM.
* Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las URL no absolutas se interpretarán en relación con AEM.
* Deje en blanco para volver a mostrar el formulario después del envío.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor similar al cuadro de diálogo de diseño del contenedor [de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
