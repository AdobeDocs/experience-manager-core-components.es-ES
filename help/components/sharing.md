---
title: Componente Compartir en redes sociales
description: El componente principal Compartir en redes sociales es una utilidad de uso compartido de Facebook y Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 100%

---

# Componente Compartir en redes sociales {#social-sharing-component}

El componente principal Compartir en redes sociales es una utilidad de uso compartido de Facebook y Pinterest.

>[!NOTE]
>
>El componente Uso compartido en redes sociales ha quedado obsoleto con la [versión 2.18.0](/help/versions.md) de los componentes principales.

## Uso {#usage}

El componente Compartir en redes sociales agrega vínculos de uso compartido de Facebook y Pinterest a la página. A menudo se incluye en encabezados o pies de página.

A diferencia de otros componentes, la configuración del componente Compartir en redes sociales la realiza el autor de la plantilla a través de [Propiedades de la página inicial](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y el autor del contenido a través de [Propiedades de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=es).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Compartir en redes sociales es la versión 1, que se introdujo con la versión 1.0.0 de los componentes principales y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente y las versiones AEM con las que son compatibles las versiones del componente.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| Versión 1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible, obsoleto | Compatible, obsoleto |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Compartir en redes sociales [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

![Cuadro de diálogo de edición del componente Compartir en redes sociales](/help/assets/sharing-edit.png)

* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe estar habilitado en el nivel de página. Por lo tanto, para el autor del contenido, hay opciones de edición adicionales disponibles para el componente Compartir en redes sociales a través de la pestaña de uso compartido [propiedades de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=es).

## Cuadro de diálogo de diseño {#design-dialog}

Dado que el uso compartido requiere encabezados de página especiales, cualquier uso compartido debe estar habilitado en el nivel de página. Por lo tanto, para el autor de la plantilla, las opciones de diseño para el componente Compartir en redes sociales están disponibles a través de las [propiedades de página inicial](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).
