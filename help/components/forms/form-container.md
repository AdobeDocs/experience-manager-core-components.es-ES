---
title: Componente Contenedor de formulario
description: El componente Contenedor de formulario de componente principal permite la creación de formularios de envío simples.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---

# Componente Contenedor de formulario {#form-container-component}

El componente Contenedor de formulario de componente principal permite la creación de formularios de envío simples.

## Uso {#usage}

El componente Contenedor de formulario permite crear formularios y funciones de envío de información sencillos mediante la compatibilidad de formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Al utilizar el [configure dialog](#configure-dialog) el editor de contenido puede definir la acción desencadenada por el envío del formulario, la URL que debe gestionar el envío y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los componentes permitidos y sus asignaciones similares al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Los componentes principales Contenedor de formulario solo admiten el uso de componentes de formulario principales (botón, texto, oculto, etc.). No se admite el uso de componentes de formulario [foundation components](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) dentro del contenedor de formularios de componentes principales (y viceversa).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-container-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Contenedor de formulario, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_container).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [del contenedor de formularios se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

Según el **Tipo de acción** seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acción disponibles son:

* [Datos de formulario de anuncio](#post-data)
* [Correo](#mail)
* [Almacenar contenido](#store-content)

Independientemente del tipo, existen [configuraciones generales](#general-settings) que se aplican a cada acción.

### Datos de formulario de anuncio {#post-data}

Cuando se envía el formulario, el tipo de acción de datos del formulario de anuncio pasa los datos enviados a un tercero como JSON para su procesamiento.

![Opciones de posponer datos de formulario en el cuadro de diálogo de edición del componente Contenedor de formulario](/help/assets/form-container-edit-post.png)

* **Punto final** : el servicio HTTPS completo que procesará los datos.
* **Mensaje de error** : Mensaje que se muestra si el envío no se ha realizado correctamente

>[!TIP]
>Hay opciones de tiempo de espera adicionales que un administrador del sistema puede ajustar para gestionar el procesamiento de los datos de formulario reenviados. [Consulte la documentación técnica de GitHub para obtener más información.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo envía un correo electrónico a los destinatarios designados.

![Opciones de correo en el cuadro de diálogo de edición del componente del contenedor de formularios](/help/assets/form-container-edit-mail.png)

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

![Almacenar opciones de contenido en el cuadro de diálogo de edición del contenedor de formularios](/help/assets/form-container-edit-store.png)

* **Ruta de contenido** : ruta del repositorio de contenido en la que se almacena el contenido enviado
* **Ver datos** : toque o haga clic para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo** : configure para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

>[!NOTE]
>
>Para simplificar la administración de los datos del usuario y hacer cumplir la separación de preocupaciones, generalmente no se recomienda almacenar el contenido generado por el usuario dentro del repositorio.
>
>En su lugar, utilice el tipo de acción [Publicar datos del formulario](#post-data) para pasar el contenido del usuario a un proveedor de servicios dedicado.

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![Opciones generales en el cuadro de diálogo de edición del componente del contenedor de formularios](/help/assets/form-container-edit-general.png)

* **Página de agradecimiento** : se redirigirá al usuario a la página especificada tras completar el envío del formulario.
   * Utilice el cuadro de diálogo Selección para seleccionar un recurso dentro de AEM.
   * Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
   * Deje en blanco para volver a mostrar el formulario después del envío.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Pestaña Estilos {#styles-tab}

El componente Contenedor de formulario es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
