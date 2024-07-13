---
title: Componente teaser (v1)
description: El componente Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.
role: Architect, Developer, Admin, User
exl-id: 48e56938-660a-43e7-9e62-8069283ae73f
source-git-commit: 84e09fa64b3a7ae40ff3ff1a04ea1c7504db29d2
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 100%

---

# Componente teaser (v1) {#teaser-component}

El componente principal Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, un vínculo a más contenido.

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a más contenido u otras acciones.

El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como para desactivar las distintas opciones de visualización. El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro de diálogo de edición](image-v1.md#edit-dialog) del [Componente Imagen](image-v1.md) para modificar la imagen del teaser.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Teaser, que se introdujo con la versión 2.1.0 de los componentes principales en julio de 2018.

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Teaser.
>
>Para obtener más información sobre la versión actual del componente Teaser, consulte el documento [Componente Teaser](/help/components/teaser.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Teaser, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_teaser_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También existe un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona una.

### Imagen {#image}

![Pestaña de imagen del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-image.png)

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el editor de recursos.

>[!NOTE]
>
>Actualmente, las [funciones de Dynamic Media](image-v1.md#dynamic-media) no están disponibles en el componente Teaser.

### Texto {#text}

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

### Vínculos y acciones {#links-actions}

![Pestaña vincular del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-link.png)

* **Vínculo**: vínculo aplicado al teaser. Utilice el navegador de rutas para seleccionar el destino del vínculo.
* **Habilitar las llamadas a acción**: cuando está marcada esta opción, habilita la definición de la llamada a acción. El primer vínculo de llamada a la acción de la lista se utiliza como vínculo para otros elementos de teaser.

## Cuadro de diálogo de edición {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el [Componente de imagen](image-v1.md). Por lo tanto, el [cuadro de diálogo de edición](image-v1.md#edit-dialog) del componente de imagen está disponible para que el autor del contenido manipule la imagen de Teaser.

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
* **Tipo de título**: define la etiqueta H que se utilizará en el título del teaser.
* **Vínculos**
   * **No vincular la imagen**: cuando se selecciona, la imagen de teaser no se vincula
   * **No vincular el título**: cuando se selecciona, el título del teaser no se vincula
* **Delegado de imágenes**: visualización informativa que indica a qué componente delega el teaser la administración de las imágenes.

### Pestaña Estilos {#styles-tab}

El componente Teaser es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Teaser es compatible con la [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md).
