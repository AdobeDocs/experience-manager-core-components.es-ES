---
title: Componente Teaser
seo-title: Componente Teaser
description: El componente teaser puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, vincular a otro contenido.
seo-description: El componente teaser puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, vincular a otro contenido.
uuid: 46989314-df 37-448 b -8562-c 707043 f 2160
contentOwner: bohnert
content-type: referencia
topic-tags: componentes principales
discoiquuid: e 597 c 18 e -3643-41 be -9878-4 a 7872 f 1 ab 90
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Teaser Component{#teaser-component}

El componente Teaser del componente principal puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, un vínculo a otro contenido.

## Uso {#usage}

El componente Teaser permite que el autor de contenido cree fácilmente un teaser para más contenido utilizando una imagen, un título o un texto enriquecido y vinculando a contenido u otras acciones.

The template author can use the [design dialog](#design-dialog) to define if the options to create call-to-actions and add links are available as well as disabling various display options. The content author can use the [configure dialog](#configure-dialog) to set an image, define CTAs, set titles and descriptions, and configure links to the individual teaser. The [edit dialog](image.md#edit-dialog) of the [Image Component](image.md) can be accessed to modify the teaser image.

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente Teaser es v 1, introducida con la versión 2.1.0 de los componentes principales en julio de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Sample Component Output {#sample-component-output}

To experience the Teaser Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Technical Details {#technical-details}

The latest technical documentation about the Teaser Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

El autor de contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. There is also an [edit dialog](#edit-dialog) to modify the teaser image if one is selected.

### Imagen {#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Recurso de imagen**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Texto {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Title**
Define un título para mostrarlo como el titular del teaser.
* **Obtener título de página
vinculada** Cuando se marque, el título se rellenará con el título de la página vinculada.
* **Descripcióndefine**
una descripción para mostrar como subtítulo del teaser.
* **Obtener descripción de la página**
vinculada Cuando se marque, la descripción se rellenará con la descripción de la página vinculada.

### Links &amp; Actions {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Vínculo de vínculo**
aplicado al teaser. Utilice el navegador de rutas para seleccionar el destino del vínculo.
* **Activar llamadas a acción**
Cuando se selecciona, habilita la definición de llamadas a acción. El primer vínculo de llamada a acción de la lista se usa como vínculo para otros elementos teaser.

## Edit Dialog {#edit-dialog}

The Teaser Component delegates image rendering to the [Image Component](image.md). Therefore the [edit dialog](image.md#edit-dialog of the Image Component is available to the content author to manipulate the teaser image.

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de teaser que tiene el autor del contenido al utilizar este componente.

### Teaser Tab {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Llamadas a la acción**
   * **Deshabilitar la opción Llamada a acción**
Oculta la **opción Llamada a acciones** para los autores de contenido
* **Elementos**
   * **Ocultar título**
      * Hides the **Title** option for content authors
      * When selected the **Title Type** is hidden
   * **Ocultar descripción**
Oculta la **opción Descripción** para los autores de contenido
* **Tipo
de título** Define la etiqueta H que utilizará el título del teaser.
* **Vínculos**
   * **No vincular la imagen**
cuando se selecciona, la imagen de teaser no está vinculada
   * **No vincular el título**
cuando se selecciona, el título del teaser no está vinculado

### Styles Tab {#styles-tab}

The Teaser Component supports the AEM [Style System](authoring.md#component-styling).
