---
title: Componente teaser
description: El componente teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 2%

---


# Componente teaser {#teaser-component}

El componente teaser de componentes principales puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, un vínculo a más contenido.

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a más contenido u otras acciones.

El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como para desactivar las distintas opciones de visualización. El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro de diálogo de edición](image.md#edit-dialog) del [Componente de imagen](image.md) para modificar la imagen del teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es v1, que se introdujo con la versión 2.1.0 de los componentes principales en julio de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente Teaser, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_teaser).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También existe un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona una.

### Imagen {#image}

![Ficha de imagen del cuadro de diálogo de edición del componente teaser](/help/assets/teaser-edit-image.png)

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

>[!NOTE]
>
>[Actualmente, las ](image.md#dynamic-media) funciones de Dynamic Media no están disponibles en el componente teaser.

### Texto {#text}

![Ficha de texto del cuadro de diálogo de edición del componente teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo** : el pretítulo se mostrará antes del título del teaser.
* **Título** : define un título que se mostrará como el titular del teaser.
   * **Obtener título de la página vinculada** : cuando se activa, el título se rellena con el título de la página vinculada.
* **Descripción** : Define una descripción para mostrarla como el subencabezado del teaser.
   * **Obtener descripción de la página vinculada** : cuando está marcada, la descripción se rellena con la descripción de la página vinculada.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### Vínculos y acciones {#links-actions}

![Ficha de vínculo del cuadro de diálogo de edición del componente teaser](/help/assets/teaser-edit-link.png)

* **Vínculo** : vínculo aplicado al teaser. Utilice el navegador de rutas para seleccionar el destino del vínculo.
* **Habilitar la llamada a acción** : cuando está marcada esta opción, habilita la definición de la llamada a acción. El primer vínculo de llamada a acción de la lista se utiliza como vínculo para otros elementos de teaser.

## Editar cuadro de diálogo {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el [Componente de imagen](image.md). Por lo tanto, el [cuadro de diálogo de edición](image.md#edit-dialog del componente de imagen está disponible para que el autor del contenido manipule la imagen de teaser.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor de contenido al utilizar este componente.

### Ficha Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser](/help/assets/teaser-design.png)

* **Llamadas a la acción**
   * **Deshabilitar llamadas a acciones** : oculte la opción  **Llamada a** acción para autores de contenido
* **Elementos**
   * **Ocultar pretítulo** : oculta la opción  **** Pretítulo para autores de contenido
   * **Ocultar título** : oculta la opción  **** Título para autores de contenido
      * Cuando se selecciona, el **Tipo de título** está oculto
   * **Ocultar descripción** : oculte la opción  **** Descripción para autores de contenido
* **Tipo de título** : define la etiqueta H que se utilizará en el título del teaser.
* **Vínculos**
   * **No vincular la imagen** : cuando se selecciona, la imagen de teaser no está vinculada
   * **No vincular el título** : cuando se selecciona, el título del teaser no está vinculado
* **Delegado de imágenes** : visualización informativa que indica a qué componente delega el teaser la gestión de imágenes.

### Pestaña Estilos {#styles-tab}

El componente Teaser es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Teaser es compatible con la capa de datos del cliente de Adobe [.](/help/developing/data-layer/overview.md)
