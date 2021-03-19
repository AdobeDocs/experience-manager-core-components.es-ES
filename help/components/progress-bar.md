---
title: Componente de barra de progreso
description: El componente de barra de progreso representa visualmente el progreso hacia un objetivo
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 3%

---


# Componente de barra de progreso {#progress-bar-component}

El componente de barra de progreso del componente principal representa visualmente el progreso hacia un objetivo.

## Uso {#usage}

El componente de barra de progreso permite al autor del contenido crear fácilmente una barra de progreso definiendo un porcentaje de finalización, lo que permite una visualización visual intuitiva del progreso hacia un objetivo.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de barra de progreso es v1, que se introdujo con la versión 2.9.0 de los componentes principales en mayo de 2020 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de barra de progreso, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_progressbar).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de barra de progreso [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

![Cuadro de diálogo de edición del componente de barra de progreso](/help/assets/progress-bar-edit.png)

* **Finalización** : el progreso representado por un porcentaje
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente de barra de progreso.

### Pestaña Estilos {#styles-tab}

El componente de barra de progreso es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente de barra de progreso es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
