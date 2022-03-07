---
title: 'Componente Descarga '
description: El componente principal Descarga permite crear una opción de descarga en una página.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: ht
source-wordcount: '758'
ht-degree: 100%

---

# Componente Descarga {#download-component}

El componente principal Descarga permite crear una opción de descarga en una página.

## Uso {#usage}

El componente Descarga de componentes principales permite incluir una opción de descarga y su recurso asociado en una página.

* Las propiedades de la opción de descarga se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente Descarga se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Descargar es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| Versión 2 | - | Compatible | Compatible |
| [Versión 1](v1/download.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Descarga, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_download).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Descarga [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_download_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de descarga y cómo se comportará y aparecerá para un visitante de la página.

![Pestaña Recurso del cuadro de diálogo de edición del componente Descarga](/help/assets/download-edit-asset.png)

### Pestaña Recurso {#asset-tab}

La selección de un recurso de descarga es muy similar a la funcionalidad del [Componente Imagen](image.md) y, del mismo modo, aprovecha AEM DAM.

* **Recurso de descarga**
   * Coloque un recurso desde el [navegador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el editor de recursos.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Descarga](/help/assets/download-edit-properties.png)

* **Título**: se muestra como un titular para el elemento de descarga
   * **Obtener el título del recurso DAM**: cuando se selecciona, el título se rellena automáticamente con el título del recurso DAM.
* **Descripción**: se muestra como un subtitular descriptivo del elemento de descarga
   * **Obtener la descripción del recurso DAM**: cuando se selecciona, la descripción se rellena automáticamente con la descripción del recurso DAM.
* **Texto de acción**: se muestra como texto de acción para el elemento de descarga
   * Este campo es necesario al cargar un recurso desde el sistema de archivos.
   * **Mostrar elementos incorporados**: al seleccionarlo, el **texto de acción** proporcionado se mostrará en línea.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Descargar](/help/assets/download-edit-styles.png)

El componente Descargar es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Descarga.

### Pestaña Propiedades {#properties-tab-design}

![Cuadro de diálogo Diseño del componente Descarga](/help/assets/download-design.png)

* **Permitir la carga desde el sistema de archivos**: permite al autor del contenido cargar un recurso desde su sistema de archivos local como recurso de descarga.
   * El valor predeterminado no está seleccionado.
* **Tipo de título**: el elemento HTML utilizado para el título del componente Descarga.
   * Si no se selecciona ningún valor, el valor predeterminado es H3.
* **Mostrar el tamaño de archivo**: cuando se selecciona, el tamaño de archivo del recurso se muestra en el componente Descarga.
   * El valor predeterminado está seleccionado.
* **Mostrar el formato de archivo**: cuando se selecciona, el formato de archivo del recurso se muestra en el componente Descarga.
   * El valor predeterminado está seleccionado.
* **Mostrar el nombre de archivo**: al seleccionarlo, el nombre de archivo del recurso se mostrará en el componente Descarga.
   * El valor predeterminado está seleccionado.

### Pestaña Estilos {#styles-tab}

El componente Imagen es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
