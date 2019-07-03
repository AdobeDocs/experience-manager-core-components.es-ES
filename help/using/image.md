---
title: Componente de imagen
seo-title: Componente de imagen
description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
seo-description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
uuid: 1 a 229 d 42-2428-43 aa -895 a -9 b 7 c 1 bf 02834
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 4684 f 33-2 fb 5-4 f 32-866 f -7136 cf 1800 d 7
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Componente de imagen{#image-component}

El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.

## Uso {#usage}

El componente Imagen permite una fácil colocación de recursos de imagen y la edición in situ. Presenta la selección de imágenes adaptables con carga diferida, además de recortar para el autor del contenido.

The image widths as well as cropping and additional settings can be defined by the template author in the [design dialog](#design-dialog). The content editor can upload or select assets in the [configure dialog](#configure-dialog) and crop the image in the [edit dialog](#edit-dialog). Para mayor comodidad, también hay disponible una modificación in-situ sencilla de la imagen.

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente de imagen es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](image-v1.md) | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## SVG Support {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente de imagen.

* Ambos son compatibles con arrastrar y soltar un recurso SVG desde DAM y cargar una carga de archivo SVG desde un sistema de archivos local.
* El servlet de imagen adaptable se transmite en flujo continuo (se omiten las transformaciones).
* Para una imagen SVG, las «imágenes inteligentes» y los «tamaños inteligentes» se definen en una matriz vacía del modelo de imagen.

### Seguridad {#security}

Por razones de seguridad, el Editor de imágenes nunca llama directamente al SVG original. It is called through `<img src=“path-to-component”>`. Como tal, el navegador evita que se ejecuten las secuencias de comandos incrustadas en el archivo SVG.

>[!CAUTION]
>
>SVG support requires release 2.1.0 of the Core Components or higher along with [service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) for AEM 6.4 or [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) for AEM 6.3 or higher to support [new image editor features](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) within AEM.

## Sample Component Output {#sample-component-output}

To experience the Image Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/image.html).

### Technical Details {#technical-details}

The latest technical documentation about the Image Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Image Component supports [schema.org microdata](https://schema.org).

## Configure Dialog {#configure-dialog}

In addition to the standard [edit dialog](#edit-dialog) and [design dialog](#design-dialog), the image component offers a configure dialog where the image itself is defined along with its description and basic properties.

### Asset Tab {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Recurso de imagen**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Metadata Tab {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

* **Image es decorativa**
si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto se aplica únicamente a imágenes decorativas.
* **Alternativa**textual textual
del significado o función de la imagen para los lectores con deficiencias visuales.
   * Get alternative text from DAM - When checked the image&#39;s alternative text will be populated with the value of the `dc:description` metadata in DAM.

* **Información**adicional sobre
la imagen, que se muestra debajo de la imagen de forma predeterminada.
   * **Obtenga un rótulo de DAM**
cuando se active el texto de rótulos de la imagen con el valor de `dc:title` los metadatos en DAM.
   * **Mostrar rótulo como ventana emergente** Cuando se active, el rótulo no se mostrará debajo de la imagen, sino como una ventana emergente mostrada por algunos exploradores al situar el ratón sobre la imagen.

* **Vínculo**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las URL no flotantes se interpretarán como relativas a AEM.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite que el autor del contenido recorte, modifique el mapa de inicio y aplique zoom a la imagen.

![](assets/chlimage_1-8.png)

* Iniciar recorte

   ![](assets/chlimage_1-9.png)

   Al seleccionar esta opción se abre una lista desplegable para proporciones de recorte predefinidas.

   * Choose the option **Free Hand** to define your own crop.
   * Choose the option **Remove Crop** to display the original asset.
   Una vez seleccionada la opción de recorte, utilice los controles azules para ajustar el tamaño del recorte en la imagen.

   ![](assets/chlimage_1-10.png)

* Rotar a la derecha

   ![](assets/chlimage_1-11.png)

   Utilice esta opción para rotar la imagen 90 ° a la derecha (en sentido de las agujas del reloj).

* Voltear horizontalmente

   ![](assets/screen_shot_2018-04-16at091404.png)

   Utilice esta opción para voltear la imagen horizontalmente o girar la imagen 180 ° a lo largo del eje Y.

* Voltear verticalmente

   ![](assets/screen_shot_2018-04-16at091410.png)

   Utilice esta opción para voltear la imagen verticalmente o girar la imagen 180 ° a lo largo del eje x.

* Iniciar mapa

   >[!CAUTION]
   >
   >The Launch Map feature requires release 2.1.0 of the Core Components or higher along with [service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) for AEM 6.4 or [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) for AEM 6.3 or higher to support [new image editor features](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) within AEM.

   ![](assets/chlimage_1-12.png)

   Utilice esta opción para aplicar un mapa de inicio a la imagen. Al seleccionar esta opción, se abre una ventana nueva que permite al usuario seleccionar la forma del mapa:

   * **Agregar mapa rectangular**
   * **Agregar mapa circular**
   * **Agregar mapa poligonal**
      * De forma predeterminada, agrega un mapa triángulo. Haga doble clic en una línea de la forma para agregar un nuevo manipulador de cambio de tamaño azul en un nuevo lado.
   Cuando se selecciona una forma de mapa, se superpone en la imagen que permite el cambio de tamaño. Arrastre y suelte los controles de cambio de tamaño azul para ajustar la forma.

   ![](assets/chlimage_1-13.png)

   Después de cambiar el tamaño del mapa de inicio, haga clic en él para abrir una barra flotante para definir la ruta del vínculo.

   * **Ruta**
      * Utilice la opción Selector de rutas para seleccionar una ruta en AEM
      * Si la ruta no está en AEM, utilice la dirección URL absoluta. Las rutas no absolutas se interpretarán en relación con AEM.
   * **Texto**
alternativo Descripción alternativa del destino de ruta
   * **Destino**
      * **Misma ficha**
      * **Nueva ficha**
      * **Marco principal**
      * **Marco superior**
   Toque o haga clic en la marca de verificación azul para guardar, la x negra para cancelar y la papelera roja puede eliminar el mapa.

   ![](assets/chlimage_1-14.png)

* Restablecer zoom

   ![](assets/chlimage_1-15.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador de zoom

   ![](assets/chlimage_1-16.png)

   Utilice esta opción para mostrar un deslizador para controlar el nivel de zoom de la imagen.

   ![](assets/chlimage_1-17.png)

El editor in-situ también se puede utilizar para modificar la imagen. Debido a limitaciones de espacio, solo hay disponibles opciones básicas en línea. Para las opciones de edición completa, utilice el modo de pantalla completa.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, rotar) no son compatibles con las imágenes GIF. Los cambios realizados en el modo de edición a GIF no persistirán.

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de recorte, carga y giro y de carga que tiene el autor del contenido al utilizar este componente.

### Main Tab {#main-tab}

On the **Main** tab you can define a list of widths in pixels for the image to automatically load the most appropriate width from the list.

Además, puede definir qué opciones de componente general se encuentran automáticamente o desactivadas cuando el autor agrega el componente a una página.

![](assets/screenshot_2018-10-19at102756.png)

* **Habilite la carga
diferida** Definir si la opción de carga diferida se activa automáticamente al agregar el componente de imagen a una página.
* **La imagen es decorativa**
si la opción de imagen decorativa se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener texto alternativo de DAM**
Definir si la opción para recuperar el texto alternativo del DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Obtenga un rótulo de DAM**
Definir si la opción para recuperar el rótulo del DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Mostrar el rótulo como ventana emergente** Definir si la opción para mostrar el rótulo de imagen como ventana emergente se activa automáticamente al agregar el componente de imagen a una página.
* **Deshabilitar seguimiento de UUID**
Para deshabilitar el seguimiento del UUID del recurso de imagen.

* **Anchos**
Define una lista de anchos en píxeles para que la imagen cargue automáticamente el ancho más adecuado desde la lista.
   * Tap or click the **Add** button to add another size.
      * Utilice los controles de captura para reorganizar el orden de los tamaños.
      * Use the **Delete** icon to remove a width.
   * De forma predeterminada, las imágenes se cargan hasta que se vuelven visibles.
      * Select the option **Disable lazy loading** to load the images upon page load.
* **Calidad
JPEG** El factor de calidad (en porcentaje entre 0 y 100) para las imágenes JPEG transformadas (p. ej., escaladas o recortadas).

>[!CAUTION]
>
>La opción Calidad JPEG está disponible desde la versión 2.2.0 de los componentes principales.

>[!NOTE]
>
>As of release 2.2.0 of the Core Components, the Image Component adds the unique UUID attribute `data-asset-id` to the image asset to allow tracking and analysis of the number of views that individual assets receive.

### Features Tab {#features-tab}

On the **Features** tab you can define which options are available to the content authors when using the component including upload options, orientation, and cropping options.

* Origen

   ![](assets/chlimage_1-19.png)

   Select the option **Allow asset upload from file system** to allow content authors to upload images from his or her local computer. Para obligar a los autores de contenido a seleccionar únicamente recursos de AEM, anule la selección de esta opción.

* Orientación

   ![](assets/chlimage_1-20.png)

* **Rotarutilice**
esta opción para permitir que el autor del contenido utilice la **opción Rotar derecha** .
* **Voltear**
Utilice esta opción para permitir al autor del contenido utilizar **las opciones Voltear horizontalmente** y **Voltear verticalmente** .

   >[!CAUTION]
   >
   >**La** opción Voltear está deshabilitada de forma predeterminada. Enabling it will display the **Flip Vertically** and **Flip Horizontally** buttons in the edit dialog of the image component, however the feature is not currently supported by AEM and any changes made using these options will not be persisted.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
 -->

* Recortar

   ![](assets/chlimage_1-21.png)

   Select the option **Allow crop** to allow the content author to crop the image in the component in the edit dialog.
   * Click **Add** to add a pre-defined crop aspect ratio.
   * Enter a descriptive name, which will be shown in the **Start Crop** dropdown.
   * Introduzca la proporción numérica del aspecto.
   * Utilice los controles de arrastrar para reorganizar el orden de las proporciones de aspecto
   * Utilice el icono de la papelera para eliminar una proporción de aspecto.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Esto difiere de la definición convencional de anchura y altura y se realiza por motivos de compatibilidad heredados. Los autores de contenido no tendrán constancia de ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la misma proporción.

### Styles Tab {#styles-tab-1}

The Image Component supports the AEM [Style System](authoring.md#component-styling).