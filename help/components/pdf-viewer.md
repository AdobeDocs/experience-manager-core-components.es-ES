---
title: Componente Visualizador de PDF
description: El componente Visualizador de PDF permite ver un documento PDF.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '705'
ht-degree: 100%

---

# Componente Visualizador de PDF {#pdf-viewer-component}

El componente principal Visualizador de PDF permite incluir un documento PDF en una página.

## Uso {#usage}

El componente principal Visualizador de PDF inserta un visualizador para mostrar los archivos PDF almacenados como recursos en la página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Visualizador de PDF es la versión 1, que se introdujo con la versión 2.10.0 de los componentes principales en junio de 2020 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| Versión 1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Visualizador de PDF, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_pdfviewer_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Visualizador de PDF [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

>[!NOTE]
>
>El componente Visualizador de PDF aprovecha las API de servicios de documentos de [Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html) y requiere que el administrador establezca una [configuración contextual](/help/developing/context-aware-configs.md) para utilizar estos servicios. Consulte la documentación técnica del componente para obtener [información sobre esta configuración.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el visor y cómo se comportará y aparecerá para un visitante de la página.

### Pestaña Configuración {#configuration-tab}

La pestaña Configuración permite al autor definir qué PDF se debe mostrar. La ruta puede definirse como un recurso en AEM o como una ruta absoluta a otro recurso.

![Pestaña Configuración del cuadro de diálogo de edición del componente Visualizador de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Pestaña Personalizar {#customize-tab}

La pestaña Personalizar permite al autor definir las opciones disponibles en el visualizador para el lector y cómo se debe presentar.

![Pestaña Personalizar del cuadro de diálogo de edición del componente Visualizador de PDF](/help/assets/pdf-viewer-edit-customize.png)

El número de opciones disponibles depende del **tipo** seleccionado.

* [Ventana completa](#full-window): el área de visualización corresponde a la pantalla del explorador completa. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [Contenedor de tamaño](#sized-container): el área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [En línea](#in-line): todas las páginas PDF se procesan en línea dentro de una página web. Esto es más adecuado para aplicaciones de lectura.

#### Ventana completa {#full-window}

El área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![La opción Ventana completa de Personalizar pestaña del cuadro de diálogo de edición del componente Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo de vista predeterminado**: aspecto del visualizador en la página cuando se abra
   * Ajustar página
   * Ajustar anchura
* **Pantalla completa**: cuando se habilita, el visualizador ocupará toda la altura y anchura de la ventana.
* **Herramientas de anotación**: cuando está activada, las herramientas de anotación están disponibles.
* **Panel izquierdo**: cuando está activada, se muestra el panel izquierdo.
* **Descargar PDF**: cuando está activada, se muestra el botón de descarga.
* **Imprimir PDF**: cuando está activada, se muestra el botón de impresión.
* **Controles de página**: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### Contenedor de tamaño reducido {#sized-container}

El área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![La opción Personalizar contenedor de tamaño de pestaña del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Pantalla completa**: cuando se habilita, el visualizador ocupará toda la altura y anchura de la ventana.
* **Descargar PDF**: cuando está activada, se muestra el botón de descarga.
* **Imprimir PDF**: cuando está activada, se muestra el botón de impresión.
* **Controles de página**: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### En línea {#in-line}

Todas las páginas PDF procesadas en línea dentro de una página web. Esto es más adecuado para aplicaciones de lectura.

![La opción Personalizar contenedor de tamaño de pestaña del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Descargar PDF**: cuando está activada, se muestra el botón de descarga.
* **Imprimir PDF**: cuando está activada, se muestra el botón de impresión.

## Cuadro de diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Visualizador de PDF.
