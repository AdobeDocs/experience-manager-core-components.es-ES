---
title: Componente Teaser
description: El componente Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 100%

---


# Componente Teaser {#teaser-component}

El componente principal Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, un vínculo a más contenido.

{{traditional-aem}}

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a más contenido u otras acciones.

El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como para desactivar las distintas opciones de visualización. El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro de diálogo de edición](image.md#edit-dialog) del [Componente Imagen](image.md) para modificar la imagen del teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](v1/teaser.md) | Compatible | Compatible | - | Compatible |

## Soporte de recursos remotos {#remote-assets}

El componente de teaser (a partir de la [versión 2.23.2](/help/versions.md)) admite recursos remotos. [Una vez configurado,](/help/developing/remote-assets.md) puede seleccionar recursos desde un servicio remoto para su componente teaser.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Teaser, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_teaser_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También existe un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona una.

### Pestaña Vínculos {#links-tab}

![Pestaña de vínculos del cuadro de diálogo Editar del componente Teaser](/help/assets/teaser-edit-links.png)

El título, la descripción y la imagen del teaser se pueden heredar de la página vinculada o de la página vinculada en la primera llamada a la acción. Si no se especifica ni un vínculo ni una llamada a la acción, el título, la descripción y la imagen se heredarán de la página actual.

* **Vínculo**: este archivo establece un vínculo a una página de contenido, a una URL externa o a un anclaje de página.
* **Abrir en ficha nueva**: si está activado, el vínculo se abre en una nueva pestaña del explorador.
* **Llamada a acción**: esta opción permite la vinculación a varios destinos.
   * La página vinculada en la primera llamada a la acción se utiliza al heredar el título, la descripción o la imagen del teaser.

### Pestaña Texto {#text-tab}

![Pestaña de texto del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo**: el pretítulo se mostrará antes del título del teaser.
* **Título**: texto que se mostrará como el titular del teaser.
   * **Obtener el título de la página vinculada**: cuando se activa, el título se rellena con el título de la página vinculada.
* **Descripción**: define una descripción para mostrarla como el subencabezado del teaser.
   * **Obtener la descripción de la página vinculada**: cuando está marcada, la descripción se rellena con la descripción de la página vinculada.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Recurso {#asset-tab}

![Pestaña de imagen del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-image.png)

* **Heredar imagen destacada de la página**: utilice la imagen definida en las propiedades de página de la página vinculada o la página actual si no encuentra ninguna.
* **Recurso de imagen**: coloque un recurso desde el [explorador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **Examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Haga clic o pulse **Seleccionar** para abrir el [explorador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) para seleccionar una imagen.
      * Si [Soporte de recursos remotos](#remote-assets) está habilitado, tiene múltiples opciones para seleccionar un recurso:
         * **Local** selecciona de la biblioteca de recursos de AEM local.
         * **Remoto** selecciona desde una biblioteca de Dynamic Media fuera de su instancia de AEM.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el editor de recursos.
* **Texto alternativo para fines de accesibilidad**: este campo le permite definir una descripción de la imagen para los usuarios con discapacidades visuales.
   * **Heredar texto alternativo de la página**: esta opción utiliza la descripción alternativa del valor de recurso vinculado de los `dc:description` metadatos en DAM o de la página actual si no hay ningún recurso vinculado.
* **No proporcionar texto alternativo**: esta opción marca la imagen para que sea ignorada por las tecnologías de asistencia, como lectores de pantalla, en casos en los que la imagen es puramente decorativa o no transmite información adicional a la página.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Lista de teaser](/help/assets/teaser-edit-styles.png)

El componente Teaser es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de edición {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el [Componente de imagen](image.md). Por lo tanto, el [cuadro de diálogo de edición]&#x200B;(image.md#edit-dialog) del componente de imagen está disponible para que el autor del contenido manipule la imagen de teaser.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor de contenido al utilizar este componente.

### Pestaña Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser](/help/assets/teaser-design.png)

* **Llamadas a la acción**
   * **Deshabilitar las llamadas a la acción**: oculta la opción **Llamadas a la acción** para autores de contenido
* **Elementos**
   * **Ocultar pretítulo**: oculta la opción **Pretítulo** para autores de contenido
   * **Ocultar título**: oculta la opción **Título** para autores de contenido
      * Cuando se selecciona, el **Tipo de título** está oculto
   * **Ocultar descripción**: oculta la opción **Descripción** para autores de contenido
* **Tipo de título predeterminado**: define la etiqueta H que se utilizará en el título del teaser.
* **Delegado de imágenes**: visualización informativa que indica a qué componente delega el teaser la administración de las imágenes.

### Pestaña Estilos {#styles-tab}

El componente Teaser es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Teaser es compatible con la [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md).
