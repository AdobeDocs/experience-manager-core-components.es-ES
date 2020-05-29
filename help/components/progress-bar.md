---
title: Componente de barra de progreso
description: El componente de barra de progreso representa visualmente el progreso hacia un objetivo
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 3%

---


# Componente de barra de progreso {#progress-bar-component}

El componente de la barra de progreso del componente principal representa visualmente el progreso hacia un objetivo.

## Uso {#usage}

El componente de barra de progreso permite al autor del contenido crear fácilmente una barra de progreso mediante la definición de un porcentaje de finalización, lo que permite una visualización visual intuitiva del progreso hacia un objetivo.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de barra de progreso es v1, que se introdujo con la versión 2.9.0 de los componentes principales en mayo de 2020, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de barra de progreso, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_progress)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de barra de progreso [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

![Cuadro de diálogo de edición del componente de barra de progreso](/help/assets/progress-bar-edit.png)

* **Finalización** : el progreso representado por un porcentaje
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente de barra de progreso.

### Ficha Estilos {#styles-tab}

El componente de barra de progreso es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
