---
title: Componente de uso compartido en redes sociales
description: El componente principal de uso compartido en redes sociales es una utilidad de uso compartido de Facebook y Pinterest.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 2%

---


# Componente de uso compartido en redes sociales{#social-sharing-component}

El componente principal de uso compartido en redes sociales es una utilidad de uso compartido de Facebook y Pinterest.

## Uso {#usage}

El componente Compartir en redes sociales agrega vínculos de uso compartido de Facebook y Pinterest a la página. A menudo se incluye en los encabezados o pies de página.

A diferencia de otros componentes, la configuración del componente de uso compartido en redes sociales la realiza el autor de la plantilla mediante [propiedades de página inicial](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) y el autor del contenido mediante [Propiedades de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de uso compartido en redes sociales es v1, que se introdujo con la versión 1.0.0 de los componentes principales y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente y las versiones AEM con las que las versiones del componente son compatibles.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Compartir en redes sociales, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_sharing).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de uso compartido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

![Cuadro de diálogo de edición del componente Compartir](/help/assets/sharing-edit.png)

* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe habilitarse en el nivel de página. Por lo tanto, para el autor del contenido, hay disponibles opciones de edición adicionales para el componente de uso compartido a través de la ficha de uso compartido las [propiedades de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Diálogo de diseño {#design-dialog}

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe habilitarse en el nivel de página. Por lo tanto, para el autor de la plantilla, las opciones de diseño para el componente de uso compartido están disponibles a través de las [propiedades de página iniciales](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
