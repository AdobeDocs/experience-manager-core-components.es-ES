---
title: Componente teaser
description: El componente teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a otro contenido.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 2%

---


# Componente teaser {#teaser-component}

El componente de teaser de componentes principales puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a otro contenido.

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a contenido u otras acciones.

El autor de la plantilla puede utilizar el cuadro de diálogo [de](#design-dialog) diseño para definir si están disponibles las opciones para crear llamadas a acción y agregar vínculos, así como desactivar las distintas opciones de visualización. El autor del contenido puede utilizar el cuadro de diálogo [de](#configure-dialog) configuración para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al cuadro de diálogo [de](image.md#edit-dialog) edición del componente [de](image.md) imagen para modificar la imagen de teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es v1, que se introdujo con la versión 2.1.0 de los componentes principales en julio de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Teaser y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_teaser)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También hay un cuadro de diálogo [de](#edit-dialog) edición para modificar la imagen de teaser si se selecciona una.

### Imagen {#image}

![Ficha de imagen del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-image.png)

* **Recurso de imagen**
   * Suelte un recurso del navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) recursos o toque la opción de **exploración** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Texto {#text}

![Ficha de texto del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo** : el pretítulo se mostrará antes del título del teaser.
* **Título** : define un título para que se muestre como titular para el teaser.
   * **Obtener título de una página** vinculada: cuando se selecciona, el título se rellena con el título de la página vinculada.
* **Descripción** : define una descripción para que se muestre como el subtítulo del teaser.
   * **Obtener descripción de la página** vinculada: cuando se selecciona, la descripción se rellena con la descripción de la página vinculada.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Vínculos y acciones {#links-actions}

![Ficha de vínculo del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-link.png)

* **Vínculo** : vínculo aplicado al teaser. Utilice el navegador de rutas para seleccionar el destinatario del vínculo.
* **Habilitar llamada a acción** : cuando está activada, habilita la definición de llamada a acción. El primer vínculo de llamada a acción de la lista se utiliza como vínculo para otros elementos de teaser.

## Edit Dialog {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el componente [](image.md)de imagen. Por lo tanto, el cuadro de diálogo [de]edición (image.md#edit-dialog) del componente de imagen está disponible para que el autor del contenido manipule la imagen de teaser.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor del contenido al utilizar este componente.

### Ficha Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser](/help/assets/teaser-design.png)

* **Llamadas a la acción**
   * **Deshabilitar llamada a acción** : ocultar la opción de **llamada a acción** para autores de contenido
* **Elementos**
   * **Ocultar pretítulo** : oculta la opción **Pretítulo** para autores de contenido
   * **Ocultar título** : oculta la opción **Título** para autores de contenido
      * Cuando se selecciona, el tipo **de** título está oculto
   * **Ocultar descripción** - Ocultar la opción **Descripción** para autores de contenido
* **Tipo** de título: define la etiqueta H que se utilizará en el título del teaser.
* **Vínculos**
   * **No vincular la imagen** : cuando se selecciona, la imagen de teaser no está vinculada
   * **No vincular el título** : cuando se selecciona, el título del teaser no está vinculado
* **Delegado** de imagen: visualización informativa que indica a qué componente delega el teaser la gestión de imágenes.

### Ficha Estilos {#styles-tab}

El componente Teaser es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
