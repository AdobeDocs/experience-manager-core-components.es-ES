---
title: Componente Teaser de correo electrónico
description: El componente Teaser de correo electrónico puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 99%

---


# Componente Teaser de correo electrónico {#email-teaser-component}

El componente Teaser de correo electrónico puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.

## Uso {#usage}

El componente Teaser de correo electrónico permite al autor del contenido crear fácilmente un teaser mediante una imagen, un título o texto enriquecido y vincularlo a más contenido u otras acciones.

* El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como para desactivar las distintas opciones de visualización.
* El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual.
* Se puede acceder al [cuadro de diálogo de edición](image.md#edit-dialog) del [Componente imagen del correo electrónico](image.md) para modificar la imagen del teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser de correo electrónico es la v1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | Compatible | - |

### Detalles técnicos {#technical-details}

La documentación técnica más reciente acerca del componente Teaser de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También existe un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona una.

### Pestaña Vínculos {#links-tab}

![Pestaña de vínculos del cuadro de diálogo editar del componente Teaser de correo electrónico](/help/email/assets/email-teaser-edit-links.png)

El título, la descripción y la imagen del teaser se pueden heredar del contenido vinculado o del contenido vinculado en la primera llamada a acción. Si no se especifica ningún vínculo ni una llamada a la acción, el título, la descripción y la imagen se heredarán del contenido actual.

* **Vínculo**: este archivo establece un vínculo a un contenido, a una URL externa o a un anclaje.
   * Haga clic en el icono de la campaña para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **Llamadas a la acción**: esta opción permite la vinculación a varios destinos.
   * La página vinculada en la primera llamada a la acción se utiliza al heredar el título, la descripción o la imagen del teaser.
   * Haga clic en el icono de la campaña para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.

### Pestaña Texto {#text-tab}

![Pestaña de texto del cuadro de diálogo de edición del componente teaser de correo electrónico](/help/email/assets/email-teaser-edit-text.png)

* **Pretítulo**: el pretítulo se mostrará antes del título del teaser.
* **Título**: texto que se mostrará como el titular del teaser.
   * Haga clic en el icono de la campaña para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
   * **Obtener el título de la página vinculada**: cuando se activa, el título se rellena con el título de la página vinculada.
* **Descripción**: define una descripción para mostrarla como el subencabezado del teaser.
   * Haga clic en el icono **Seleccione la variable Adobe Campaign** para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
   * **Obtener la descripción de la página vinculada**: cuando está marcada, la descripción se rellena con la descripción de la página vinculada.
* **ID**: esta opción permite controlar el identificador único del componente en HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.

### Pestaña Recurso {#asset-tab}

![Pestaña de imagen del cuadro de diálogo de edición del componente teaser de correo electrónico](/help/email/assets/email-teaser-edit-image.png)

* **Heredar imagen destacada de la página**: utilice la imagen definida en las propiedades de página de la página vinculada o la página actual si no encuentra ninguna.
* **Recurso de imagen**: coloque un recurso desde el [explorador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **Examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el Editor de recursos.
* **Texto alternativo para fines de accesibilidad**: este campo le permite definir una descripción de la imagen para los usuarios con discapacidades visuales.
   * **Heredar texto alternativo de la página**: esta opción utiliza la descripción alternativa del valor de recurso vinculado de los `dc:description` metadatos en DAM o de la página actual si no hay ningún recurso vinculado.
* **No proporcionar texto alternativo**: esta opción marca la imagen para que sea ignorada por las tecnologías de asistencia, como lectores de pantalla, en casos en los que la imagen es puramente decorativa o no transmite información adicional a la página.

>[!NOTE]
>
>Actualmente, las [funciones de Dynamic Media](image.md#dynamic-media) no están disponibles en el componente Teaser.

### Pestaña Estilos {#styles-tab-edit}

El componente Teaser de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de edición {#edit-dialog}

El componente Teaser de correo electrónico delega el procesamiento de imágenes en el [componente Imagen](image.md). Por lo tanto, el [cuadro de diálogo de edición](image.md#edit-dialog) del componente de imagen está disponible para que el autor del contenido manipule la imagen de Teaser.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor de contenido al utilizar este componente.

### Pestaña Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser de correo electrónico](/help/email/assets/email-teaser-design.png)

* **Elementos de encabezado permitidos**: utilice la lista desplegable para definir qué elementos HTML de encabezado puede seleccionar un autor para el tipo de título del teaser.
* **Elemento de encabezado predeterminado del título**: el elemento HTML de encabezado predeterminado que se utiliza para el tipo de título del teaser
* **Llamadas a la acción**
   * **Deshabilitar las llamadas a la acción**: oculta la opción **Llamadas a la acción** para autores de contenido
* **Elementos**
   * **Ocultar pretítulo**: oculta la opción **Pretítulo** para autores de contenido
   * **Ocultar título**: oculta la opción **Título** para autores de contenido
      * Cuando se selecciona, el **Tipo de título** está oculto
   * **Mostrar tipo de título**
   * **Ocultar descripción**: oculta la opción **Descripción** para autores de contenido
* **Delegado de imágen**: visualización informativa que indica a qué componente delega el Teaser de correo electrónico la administración de las imágenes.

### Pestaña Estilos {#styles-tab}

El componente Teaser de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
