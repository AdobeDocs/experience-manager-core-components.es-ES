---
title: Componente del contenedor de formularios
description: El componente principal Contenedor de formularios permite crear formularios de envío simples.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '914'
ht-degree: 100%

---

# Componente del contenedor de formularios {#form-container-component}

El componente principal Contenedor de formularios permite crear formularios de envío simples.

## Uso {#usage}

El Componente del contenedor de formularios permite crear formularios y funciones de envío de información sencillos mediante la compatibilidad de formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Al utilizar el [cuadro de diálogo de configuración](#configure-dialog) el editor de contenido puede definir la acción desencadenada por el envío del formulario, la URL que debe administrar el envío y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los componentes permitidos y las asignaciones similares a él para el [contenedor de diseño estándar en el editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

>[!NOTE]
>
>Los componentes principales del componente del contenedor de formularios solo admite el uso de otros componentes principales de componentes de formularios (botón, texto, oculto, etc.). No se admite el uso de componentes de formularios de [componentes de fundación](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=es) dentro del contenedor de formularios de componentes principales (y viceversa).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente del contenedor de formularios es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 2 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/form-container-v1.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para obtener más información sobre el componente del contenedor de formularios, así como ejemplos de sus opciones de configuración, y sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_container_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [Contenedor de formularios se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

Según el **Tipo de acción** seleccionado, cambiarán las opciones disponibles dentro del contenedor. Los tipos de acción disponibles son:

* [Publicar datos de formulario](#post-data)
* [Correo](#mail)
* [Almacenar contenido](#store-content)

Independientemente del tipo, existen [configuraciones generales](#general-settings) que se aplican a cada acción.

### Publicar datos de formulario {#post-data}

Cuando se envía el formulario, el tipo de acción de publicación de datos de formulario pasa los datos enviados a un tercero como JSON para su procesamiento.

![Opciones de publicar datos de formulario en el cuadro de diálogo de edición del componente del contenedor de formularios](/help/assets/form-container-edit-post.png)

* **Punto de conexión**: el servicio HTTPS completo que procesará los datos
* **Mensaje de error**: mensaje que se muestra si el envío no se ha realizado correctamente

>[!TIP]
>Hay opciones de tiempo de espera adicionales que un administrador del sistema puede ajustar para administrar el procesamiento de los datos de formulario reenviados. [Consulte la documentación técnica de GitHub para obtener más información.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo envía un correo electrónico a los destinatarios designados.

![Opciones de correo en el cuadro de diálogo de edición del componente del contenedor de formularios](/help/assets/form-container-edit-mail.png)

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

![Almacenar opciones de contenido en el cuadro de diálogo de edición del contenedor de formularios](/help/assets/form-container-edit-store.png)

* **Ruta de contenido**: ruta del repositorio de contenido donde se almacena el contenido enviado
* **Ver datos**: pulse o haga clic en esta opción para ver los datos enviados almacenados como JSON
* **Iniciar flujo de trabajo**: configúrelo para iniciar un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

>[!NOTE]
>
>Para simplificar la administración de los datos del usuario y hacer cumplir la separación de preocupaciones, generalmente no se recomienda almacenar el contenido generado por el usuario dentro del repositorio.
>
>En lugar de eso, utilice el tipo de acción [Publicar datos del formulario](#post-data) para pasar el contenido del usuario a un proveedor de servicios dedicado.

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![Opciones generales en el cuadro de diálogo de edición del componente del contenedor de formularios](/help/assets/form-container-edit-general.png)

* **Página de agradecimiento**: se redirigirá al usuario a la página especificada tras completar el envío del formulario.
   * Utilice el cuadro de diálogo de selección para seleccionar un recurso dentro de AEM.
   * Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
   * Déjela vacía para volver a visualizar el formulario tras el envío.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el [contenedor de diseño estándar en el editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

### Pestaña Estilos {#styles-tab}

El componente del contenedor de formularios es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
