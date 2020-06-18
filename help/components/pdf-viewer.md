---
title: Componente de visor PDF
description: El componente de visor de PDF permite la visualización de un documento PDF.
translation-type: tm+mt
source-git-commit: 0df759a020020c21d776eb8f45d40cb7aff45cea
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 2%

---


# Componente de visor PDF {#pdf-viewer-component}


El componente Core Component PDF Viewer permite la inclusión de un documento PDF en una página.

## Uso {#usage}

El componente Core Component PDF Viewer incorpora un visor para mostrar los archivos PDF almacenados como recursos en la página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de visor de PDF es v1, que se introdujo con la versión 2.10.0 de los componentes principales en junio de 2020 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para ver el componente de visor de PDF, así como ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_pdf_viewer)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de visor de PDF [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_pdf-viewer_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el visor y cómo se comportará y aparecerá para un visitante de la página.

### Configuration Tab {#configuration-tab}

La ficha Configuración permite al autor definir qué PDF se debe mostrar. La ruta se puede definir como un recurso en AEM o como una ruta absoluta a otro recurso.

![Ficha Configuración del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Ficha Personalizar {#customize-tab}

La ficha Personalizar permite al autor definir las opciones disponibles en el visor para el lector y cómo se debe presentar el visor.

![Ficha Personalizar del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize.png)

El número de opciones disponibles depende del **tipo** seleccionado.

* [Ventana](#full-window) completa: el área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [Contenedor](#sized-container) de tamaño: el área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.
* [En línea](#in-line) : todas las páginas PDF representadas en línea dentro de una página web. Esto es más adecuado para la lectura de aplicaciones.

#### Ventana completa {#full-window}

El área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Opción Personalizar ficha en ventana completa del cuadro de diálogo de edición del componente del visor de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo** de Vista predeterminado: cómo se adaptará el visor a la página en la que se muestra
   * Ajustar página
   * Ajustar anchura
* **Pantalla** completa: cuando está activada, el visor ocupa toda la altura y anchura de la ventanilla.
* **Herramientas** de anotación: cuando está activada, las herramientas de anotación están disponibles.
* **Panel** izquierdo: cuando está activado, se muestra el panel izquierdo.
* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles** de página: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### Contenedor de tamaño {#sized-container}

El área de visualización se procesa en el navegador completo. Esto es más adecuado para aplicaciones de almacenamiento y productividad.

![Personalización de la opción de contenedor de tamaño de ficha del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Pantalla** completa: cuando está activada, el visor ocupa toda la altura y anchura de la ventanilla.
* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.
* **Controles** de página: cambia el comportamiento de los controles de página.
   * Acoplar
   * Desacoplar

#### En línea {#in-line}

Todas las páginas PDF representadas en línea dentro de una página web. Esto es más adecuado para la lectura de aplicaciones.

![Personalización de la opción de contenedor de tamaño de ficha del cuadro de diálogo de edición del componente de visor de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Descargar PDF** : cuando está activado, se muestra el botón de descarga.
* **Imprimir PDF** : cuando está activado, se muestra el botón de impresión.

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente de visor de PDF.
