---
title: Componente de visor PDF
description: El componente de visor de PDF permite la visualización de un documento PDF.
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---


# Componente de visor de PDF {#pdf-viewer-component}

El componente Core Component PDF Viewer permite la inclusión de un documento PDF en una página.

## Uso {#usage}

El componente Core Component PDF Viewer incorpora un visor para mostrar los archivos PDF almacenados como recursos en la página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de visor de PDF es v1, que se introdujo con la versión 2.10.0 de los componentes principales en junio de 2020 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de visor de PDF y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de visor de PDF [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

>[!NOTE]
>
>El componente de visor de PDF aprovecha las [API de servicios de Documento](https://www.adobe.io/apis/documentcloud/dcsdk.html) de Adobe y requiere que el administrador configure una [configuración contextual](/help/developing/context-aware-configs.md) para poder utilizar estos servicios. Consulte la documentación técnica del componente para obtener [detalles sobre esta configuración.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el visor y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Configuración {#configuration-tab}

La ficha Configuración permite al autor definir qué PDF se debe mostrar. La ruta se puede definir como un recurso en AEM o una ruta absoluta a otro recurso.

![Ficha Configuración del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Personalizar ficha {#customize-tab}

La ficha Personalizar permite al autor definir las opciones disponibles en el visor para el lector y cómo se debe presentar el visor.

![Ficha Personalizar del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize.png)

El número de opciones disponibles depende del **Tipo** que se seleccione.

* [Ventana](#full-window)  completa: el área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [Contenedor](#sized-container)  de tamaño: el área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [En línea](#in-line) : todas las páginas PDF representadas en línea dentro de una página web. Esto es más adecuado para la lectura de aplicaciones.

#### Ventana completa {#full-window}

El área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Opción Personalizar ficha en ventana completa del cuadro de diálogo de edición del componente del visor de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo**  de Vista predeterminado: cómo se adaptará el visor a la página en la que se muestra
   * Ajustar página
   * Ajustar anchura
* **Pantalla**  completa: cuando está activada, el visor ocupa toda la altura y anchura de la ventanilla.
* **Herramientas**  de anotación: cuando está activada, las herramientas de anotación están disponibles.
* **Panel**  izquierdo: cuando está activado, se muestra el panel izquierdo.
* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles**  de página: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### Contenedor de tamaño reducido {#sized-container}

El área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Personalización de la opción de contenedor de tamaño de ficha del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Pantalla**  completa: cuando está activada, el visor ocupa toda la altura y anchura de la ventanilla.
* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles**  de página: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### En línea {#in-line}

Todas las páginas PDF representadas en línea dentro de una página web. Esto es más adecuado para la lectura de aplicaciones.

![Personalización de la opción de contenedor de tamaño de ficha del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.

## Diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente de visor de PDF.
