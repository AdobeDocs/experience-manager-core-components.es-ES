---
title: Componente de uso compartido en redes sociales
description: El componente principal de uso compartido en medios sociales es un widget de uso compartido de Pinterest y Facebook.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 7%

---


# Componente de uso compartido en medios sociales{#social-sharing-component}

El componente principal de uso compartido en medios sociales es un widget de uso compartido de Pinterest y Facebook.

## Uso {#usage}

El componente Uso compartido en medios sociales agrega vínculos de uso compartido de Facebook y Pinterest a la página. A menudo se incluye en encabezados o pies de página.

A diferencia de otros componentes, la configuración del componente de uso compartido en medios sociales la realiza el autor de la plantilla a través de [Propiedades de la página inicial](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) y el autor del contenido a través de [Propiedades de página](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de uso compartido en medios sociales es v1, que se introdujo con la versión 1.0.0 de los componentes principales y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente y las versiones AEM con las que son compatibles las versiones del componente.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de uso compartido en medios sociales, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_sharing).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de uso compartido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

![Cuadro de diálogo de edición del componente de uso compartido](/help/assets/sharing-edit.png)

* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe estar habilitado en el nivel de página. Por lo tanto, para el autor del contenido, hay opciones de edición adicionales disponibles para el componente de uso compartido a través de la pestaña de uso compartido [propiedades de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Diálogo de diseño {#design-dialog}

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe estar habilitado en el nivel de página. Por lo tanto, para el autor de la plantilla, las opciones de diseño para el componente de uso compartido están disponibles a través de las [propiedades de página inicial](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
