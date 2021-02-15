---
title: Componente teaser
description: El componente teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a otro contenido.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 2%

---


# Componente teaser {#teaser-component}

El componente de teaser de componentes principales puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a otro contenido.

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a contenido u otras acciones.

El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como deshabilitar varias opciones de visualización. El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro de diálogo de edición](image.md#edit-dialog) del [Componente de imagen](image.md) para modificar la imagen de teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es v1, que se introdujo con la versión 2.1.0 de los componentes principales en julio de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Teaser y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_teaser).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También hay un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona uno.

### Imagen {#image}

![Ficha de imagen del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-image.png)

* **Recurso de imagen**
   * Suelte un recurso del [navegador de recursos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) o toque la opción **examinar** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para deseleccionar la imagen seleccionada actualmente.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

>[!NOTE]
>
>[Actualmente, ](image.md#dynamic-media) las funciones de Dynamic Media no están disponibles en el componente Teaser.

### Texto {#text}

![Ficha de texto del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo** : el pretítulo se mostrará antes del título del teaser.
* **Título** : define un título para que se muestre como titular para el teaser.
   * **Obtener título de una página**  vinculada: al activarlo, el título se rellenará con el título de la página vinculada.
* **Descripción** : define una descripción para que se muestre como el subtítulo del teaser.
   * **Obtener descripción de la página**  vinculada: cuando se selecciona, la descripción se rellena con la descripción de la página vinculada.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Vínculos y acciones {#links-actions}

![Ficha de vínculo del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-link.png)

* **Vínculo** : vínculo aplicado al teaser. Utilice el navegador de rutas para seleccionar el destinatario del vínculo.
* **Habilitar llamada a acción** : cuando está activada, habilita la definición de llamada a acción. El primer vínculo de llamada a acción de la lista se utiliza como vínculo para otros elementos de teaser.

## Editar cuadro de diálogo {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el [componente de imagen](image.md). Por lo tanto, el [cuadro de diálogo de edición](image.md#edit-dialog del componente de imagen está disponible para que el autor del contenido manipule la imagen de teaser.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor del contenido al utilizar este componente.

### Ficha Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser](/help/assets/teaser-design.png)

* **Llamadas a la acción**
   * **Deshabilitar Llamada a acción** : ocultar la opción  **Llamada a** acción para autores de contenido
* **Elementos**
   * **Ocultar pretítulo** : oculta la opción  **** Pretítulo para autores de contenido
   * **Ocultar título** : oculta la opción  **** Título para autores de contenido
      * Cuando se selecciona, el **tipo de título** está oculto
   * **Ocultar descripción** - Ocultar la opción  **** Descripción para autores de contenido
* **Tipo**  de título: define la etiqueta H que utilizará el título del teaser.
* **Vínculos**
   * **No vincular la imagen** : cuando se selecciona, la imagen de teaser no está vinculada
   * **No vincular el título** : cuando se selecciona, el título del teaser no está vinculado
* **Delegado**  de imagen: visualización informativa que indica a qué componente delega el teaser la gestión de imágenes.

### Ficha Estilos {#styles-tab}

El componente Teaser admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Teaser admite la capa de datos del cliente de Adobe [](/help/developing/data-layer/overview.md).
