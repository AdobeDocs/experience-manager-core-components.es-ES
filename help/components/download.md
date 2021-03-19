---
title: Descargar componente
description: El componente de descarga de componentes principales permite crear una opción de descarga en una página.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 2%

---


# Descargar componente{#download-component}

El componente de descarga de componentes principales permite crear una opción de descarga en una página.

## Uso {#usage}

El componente de descarga de componentes principales permite incluir una opción de descarga y su recurso asociado en una página.

* Las propiedades de la opción de descarga se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente de descarga se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de descarga es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de descarga, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_download).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de descarga [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de descarga y cómo se comportará y aparecerá para un visitante de la página.

![Pestaña Recurso del cuadro de diálogo de edición del componente de descarga](/help/assets/download-edit-asset.png)

### Pestaña Activo {#asset-tab}

La selección de un recurso de descarga es muy similar a la funcionalidad del [Componente de imagen](image.md) y, del mismo modo, aprovecha AEM DAM.

* **Recurso de descarga**
   * Coloque un recurso desde el [navegador de recursos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente de descarga](/help/assets/download-edit-properties.png)

* **Título** : se muestra como un titular para el elemento de descarga
   * **Obtener título del recurso DAM** : cuando se selecciona, el título se rellena automáticamente con el título del recurso DAM.
* **Descripción** : se muestra como un subtitular descriptivo del elemento de descarga
   * **Obtener descripción del recurso DAM** : cuando se selecciona, la descripción se rellena automáticamente con la descripción del recurso DAM.
* **Texto de acción** : se muestra como texto de acción para el elemento de descarga
   * Este campo es necesario al cargar un recurso desde el sistema de archivos.
   * **Mostrar en línea** : al seleccionarlo, el texto de  **acción** proporcionado se mostrará en línea.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente de descarga.

### Ficha Propiedades {#properties-tab-design}

![Cuadro de diálogo Diseño del componente de descarga](/help/assets/download-design.png)

* **Permitir carga desde el sistema de archivos** : permite al autor del contenido cargar un recurso desde su sistema de archivos local como recurso de descarga.
   * El valor predeterminado no está seleccionado.
* **Tipo de título** : el elemento HTML utilizado para el título del componente de descarga.
   * Si no se selecciona ningún valor, el valor predeterminado es H3.
* **Mostrar tamaño de archivo** : cuando se selecciona, el tamaño de archivo del recurso se muestra en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Formato del archivo de visualización** : cuando se selecciona, el formato de archivo del recurso se muestra en el componente de descarga.
   * Se selecciona el valor predeterminado.
* **Mostrar nombre de archivo** : al seleccionarlo, el nombre de archivo del recurso se mostrará en el componente de descarga.
   * Se selecciona el valor predeterminado.

### Pestaña Estilos {#styles-tab}

El componente Imagen es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
