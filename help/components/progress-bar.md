---
title: Componente de barra de progreso
description: El componente de barra de progreso representa visualmente el progreso hacia un objetivo
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---


# Componente de barra de progreso {#progress-bar-component}

El componente de la barra de progreso del componente principal representa visualmente el progreso hacia un objetivo.

## Uso {#usage}

El componente de barra de progreso permite al autor del contenido crear fácilmente una barra de progreso mediante la definición de un porcentaje de finalización, lo que permite una visualización visual intuitiva del progreso hacia un objetivo.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de barra de progreso es v1, que se introdujo con la versión 2.9.0 de los componentes principales en mayo de 2020, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de la barra de progreso y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_progressbar).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de barra de progreso [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

![Cuadro de diálogo de edición del componente de barra de progreso](/help/assets/progress-bar-edit.png)

* **Finalización** : el progreso representado por un porcentaje
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente de barra de progreso.

### Ficha Estilos {#styles-tab}

El componente de barra de progreso admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente de barra de progreso admite la capa de datos del cliente de Adobe [](/help/developing/data-layer/overview.md).
