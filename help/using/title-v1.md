---
title: Componente de título (v 1)
seo-title: Componente de título (v 1)
description: El componente Título de componente principal es un componente de encabezado de sección que incluye edición in-situ.
seo-description: El componente Título de componente principal es un componente de encabezado de sección que incluye edición in-situ.
uuid: 5 c 4 d 276 c-f 0 be -4122-a 15 e -3 f 7443 d 8 b 209
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 028 ebef -2957-410 c -9 bab-a 7040 c 350 f 2 f
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente de título (v 1){#title-component-v}

El componente Título de componente principal es un componente de encabezado de sección que incluye edición in-situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido.

El autor de la plantilla puede definir los niveles de encabezados disponibles en el cuadro de diálogo [de diseño](title-v1.md#main-pars_title_1995166862). El editor de contenido puede seleccionar los niveles de encabezados disponibles en el cuadro de diálogo [de edición](title-v1.md#main-pars_title). Para mayor comodidad, también hay disponible una edición in-situ sencilla del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe v 1 del componente Título, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v 1 del componente Título.

| Versión de AEM | Componente de título v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Título.
>
>Para obtener más información sobre la versión actual del componente Título, consulte [el documento Componente](title.md) de título.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título y seleccionar el nivel de encabezado.

>[!NOTE]
>
>Un valor vacío para el título hará que se muestre el título de la página.

![](assets/chlimage_1-91.png)

El editor in-situ también se puede utilizar para editar el texto del componente de título.

![](assets/chlimage_1-37.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

![](assets/chlimage_1-92.png)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
