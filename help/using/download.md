---
title: Descargar componente
seo-title: Descargar componente
description: nulo
seo-description: El componente Descarga de componentes principales permite crear una opción de descarga en una página.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 88bc68b60e5de247fe800ac041ffefdf9238cce1

---


# Download Component{#download-component}

El componente Descarga de componentes principales permite crear una opción de descarga en una página.

## Uso {#usage}

El componente Descarga de componentes principales permite incluir una opción de descarga y su recurso asociado en una página.

* The download option&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the download component can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente Descargar es v 1, introducida con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Download Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/download.html).

## Technical Details {#technical-details}

The latest technical documentation about the Download Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el elemento de descarga y cómo se comportará y aparecerá para un visitante de la página.

![](assets/screen-shot-2019-06-17-09.49.14.png)

### Asset Tab {#asset-tab}

The selection of a download asset is very similar to the functionality of the [Image Component](image.md) and likewise leverages AEM&#39;s DAM.

* **Recurso de descarga**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Properties Tab {#properties-tab}

![](assets/screen-shot-2019-06-17-09.49.51.png)

* **Título** : se muestra como un titular para el elemento de descarga
   * **Obtener título del recurso** DAM: cuando se selecciona, el título se rellena automáticamente con el título del recurso DAM.
* **Descripción** : Muestra como subtitular descriptivo del elemento de descarga
   * **Obtener descripción del recurso** DAM: cuando se selecciona, la descripción se rellena automáticamente con la descripción de los recursos DAM.
* **Texto** de acción: muestra como texto de acción para el elemento de descarga
   * Este campo es necesario al cargar un recurso desde el sistema de archivos.
   * **Mostrar línea** : Cuando se selecciona el texto **de acción proporcionado** se mostrará en línea.

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Descargar.

### Properties Tab {#properties-tab-design}

![](assets/screen-shot-2019-06-17-10.04.31.png)

* **Texto** de acción predeterminado: define el texto **de acción predeterminado** que se proporciona cuando un autor agrega el componente Descargar a una página.
* **Permitir la carga desde el sistema** de archivos: Permite al autor del contenido cargar un recurso desde su sistema de archivos local como recurso de descarga.
   * El valor predeterminado no está seleccionado.
* **Tipo** de título: elemento HTML utilizado para el título de Descargar componente.
   * Si no se selecciona ningún valor, el valor predeterminado es H 3.
* **Mostrar tamaño** de archivo: cuando se selecciona el tamaño de archivo del recurso, se mostrará en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Mostrar formato** de archivo: cuando se selecciona el formato de archivo del recurso se mostrará en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Mostrar nombre de archivo** : cuando se selecciona el nombre de archivo del recurso se mostrará en el componente de descarga.
   * Se selecciona el valor predeterminado.

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](authoring.md#component-styling).
