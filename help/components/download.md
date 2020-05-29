---
title: Descargar componente
description: El componente de descarga de componentes principales permite la creación de una opción de descarga en una página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 2%

---


# Descargar componente{#download-component}

El componente de descarga de componentes principales permite la creación de una opción de descarga en una página.

## Uso {#usage}

El componente Descarga de componentes principales permite incluir una opción de descarga y su recurso asociado en una página.

* Las propiedades de la opción de descarga se pueden seleccionar en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los valores predeterminados del componente de descarga se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de descarga es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para obtener información sobre el componente de descarga y ver ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_download)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de descarga [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de descarga y cómo se comportará y aparecerá para un visitante de la página.

![Ficha Recurso del cuadro de diálogo de edición del componente de descarga](/help/assets/download-edit-asset.png)

### Ficha Recurso {#asset-tab}

La selección de un recurso de descarga es muy similar a la funcionalidad del componente [de](image.md) imagen y, del mismo modo, aprovecha el DAM de AEM.

* **Recurso de descarga**
   * Suelte un recurso del navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) recursos o toque la opción de **exploración** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición Descargar componente](/help/assets/download-edit-properties.png)

* **Título** : se muestra como titular para el elemento de descarga
   * **Obtener título del recurso** DAM: cuando se selecciona, el título se rellena automáticamente con el título del recurso DAM.
* **Descripción** : se muestra como un subtítulo descriptivo del elemento de descarga
   * **Obtener descripción del recurso** DAM: cuando se selecciona, la descripción se rellena automáticamente con la descripción del recurso DAM.
* **Texto** de acción: se muestra como texto de acción para el elemento de descarga
   * Este campo es obligatorio cuando se carga un recurso desde el sistema de archivos.
   * **Mostrar en línea** : cuando se selecciona, el Texto **de** acción proporcionado se muestra en línea.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Descargar.

### Ficha Propiedades {#properties-tab-design}

![Cuadro de diálogo Diseño del componente de descarga](/help/assets/download-design.png)

* **Permitir la carga desde el sistema** de archivos: permite al autor del contenido cargar un recurso desde su sistema de archivos local como recurso de descarga.
   * El valor predeterminado no está seleccionado.
* **Tipo** de título: elemento HTML utilizado para el título del componente de descarga.
   * Si no hay ningún valor seleccionado, el valor predeterminado es H3.
* **Mostrar tamaño** de archivo: cuando se selecciona, el tamaño de archivo del recurso se muestra en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Formato** de archivo de visualización: cuando se selecciona, el formato de archivo del recurso se muestra en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Mostrar nombre de archivo** : cuando se selecciona, el nombre de archivo del recurso se mostrará en el componente de descarga.
   * Se selecciona el valor predeterminado.

### Ficha Estilos {#styles-tab}

El componente Imagen admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
