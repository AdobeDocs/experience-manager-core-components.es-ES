---
title: Componente de visualizador de PDF
description: El componente visualizador de PDF permite la visualización de un documento PDF.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 3%

---


# Componente de visor de PDF {#pdf-viewer-component}

El componente Core Component PDF Viewer permite la inclusión de un documento PDF en una página.

## Uso {#usage}

El componente visualizador de PDF de componente principal incrusta un visualizador para mostrar los archivos PDF almacenados como recursos en la página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente visualizador de PDF es v1, que se introdujo con la versión 2.10.0 de los componentes principales en junio de 2020 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente visualizador de PDF, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente visualizador de PDF [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

>[!NOTE]
>
>El componente visualizador de PDF aprovecha las API de servicios de documentos del [Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html) y requiere que el administrador configure una [configuración según el contexto](/help/developing/context-aware-configs.md) para utilizar estos servicios. Consulte la documentación técnica del componente para obtener [detalles sobre esta configuración.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el visor y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Configuración {#configuration-tab}

La ficha Configuración permite al autor definir qué PDF se debe mostrar. La ruta puede definirse como un recurso en AEM o como una ruta absoluta a otro recurso.

![Ficha Configuración del cuadro de diálogo de edición del componente Visor de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Pestaña Personalizar {#customize-tab}

La pestaña Personalizar permite al autor definir las opciones disponibles en el visor para el lector y cómo se debe presentar el visor.

![Ficha Personalizar del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize.png)

El número de opciones disponibles depende del **Type** seleccionado.

* [Ventana completa](#full-window) : el área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [Contenedor de tamaño](#sized-container) : el área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [En línea](#in-line) : todas las páginas PDF procesadas en línea dentro de una página web. Esto es más adecuado para leer aplicaciones.

#### Ventana completa {#full-window}

El área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Opción Personalizar ficha ventana completa del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo de vista predeterminado** : cómo se ajustará el visor a la página en la que se muestra
   * Ajustar página
   * Ajustar anchura
* **Pantalla completa** : cuando se habilita, el visor ocupará toda la altura y anchura de la ventanilla.
* **Herramientas de anotación** : cuando está activada, las herramientas de anotación están disponibles.
* **Panel izquierdo** : cuando está activado, se muestra el panel izquierdo.
* **Descargar PDF** : Cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles de página** : cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### Contenedor de tamaño reducido {#sized-container}

El área de visualización se procesa en el explorador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Opción Personalizar contenedor de tamaño de ficha del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Pantalla completa** : cuando se habilita, el visor ocupará toda la altura y anchura de la ventanilla.
* **Descargar PDF** : Cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles de página** : cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### En línea {#in-line}

Todas las páginas PDF procesadas en línea dentro de una página web. Esto es más adecuado para leer aplicaciones.

![Opción Personalizar contenedor de tamaño de ficha del cuadro de diálogo de edición del componente visualizador de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Descargar PDF** : Cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.

## Diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente visualizador de PDF.
