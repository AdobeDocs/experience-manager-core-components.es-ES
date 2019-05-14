---
title: Componente Contenedor de formulario
seo-title: Componente Contenedor de formulario
description: nulo
seo-description: El componente Contenedor de formulario de componente principal permite crear formularios de envío sencillos.
uuid: 9 d 556 daf -3 fe 7-4 b 2 a-b 5 ae -6926 acb 267 a 9
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 d 33 fe 60-a 0 ac -4 ff 2-a 865-d 600 b 5448 aeb
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


# Componente Contenedor de formulario{#form-container-component}

El componente Contenedor de formulario de componente principal permite crear formularios de envío sencillos.

## Uso {#usage}

El componente Contenedor de formulario permite la creación de formularios y funciones de envío sencillos de información, ya que admite formularios WCM sencillos y una estructura anidada para permitir componentes adicionales de formulario.

Mediante el uso del [cuadro de diálogo](#configure-dialog) de configuración, el editor de contenido puede definir la acción desencadenada por el envío de formulario, donde el contenido enviado debe guardarse y si debería activarse un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de diseño](#design-dialog) para definir los componentes permitidos y sus asignaciones de forma similar al cuadro de diálogo de diseño del contenedor [de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!NOTE]
>
>Los componentes principales Componente Contenedor de formulario solo admiten el uso de componentes de formulario de componentes principales (botón, texto, oculto, etc.). El uso [de componentes de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) componentes de base dentro del contenedor de formulario de componentes principales (y viceversa) no es compatible.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de formulario es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-container-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir qué acciones se toman cuando se envía el componente.

![](assets/screen_shot_2018-01-12at122046.png)

Según el tipo **de acción seleccionado**, las opciones disponibles dentro del contenedor cambiarán. Los tipos de acción disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)
* [Enviar pedido](#submit-order)
* [Actualizar orden](#update-order)

Independientemente del tipo, existen ajustes [generales](#general-settings) que se aplican a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción enviará un correo electrónico a los destinatarios designados.

![](assets/screen_shot_2018-01-12at122554.png)

* **Asunto**
El asunto del correo electrónico que se enviará al envío del formulario
* **Desde**
la dirección de correo electrónico del correo electrónico que se enviará al envío del formulario
* **A**
las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario

   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el **botón Eliminar** para eliminar una dirección de correo electrónico
* **CC**
Las direcciones de los destinatarios que recibirán una copia en blanco el correo electrónico enviado al enviar el formulario
   * Toque o haga clic en el botón **Agregar** para agregar direcciones adicionales
   * Toque o haga clic en el **botón Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacenará en una ubicación del repositorio designada.

![](assets/screen_shot_2018-01-12at122538.png)

* **Ruta del repositorio**de contenido Ruta
del contenido donde se almacena el contenido enviado
* **Ver el toque de datos**
o hacer clic para ver los datos enviados enviados como JSON
* **Iniciar**Configuración de flujo de trabajo
para iniciar un flujo de trabajo con el contenido almacenado como carga útil al enviar el formulario

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

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor similar al cuadro de diálogo de diseño del contenedor [de diseño estándar en el editor de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).