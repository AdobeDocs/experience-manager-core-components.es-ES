---
title: Componente de título (v1)
description: El componente Título del componente principal es un componente de encabezado de sección que incluye la edición in-situ.
index: n
translation-type: tm+mt
source-git-commit: 945381996db443c227aa31f0aacb963071165681

---


# Title Component (v1){#title-component-v}

El componente Título del componente principal es un componente de encabezado de sección que incluye la edición in-situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido.

El autor de la plantilla puede definir los niveles de encabezado disponibles en el cuadro de diálogo [de](title-v1.md#main-pars_title_1995166862)diseño. El editor de contenido puede seleccionar los niveles de encabezados disponibles en el cuadro de diálogo [de](title-v1.md#main-pars_title)edición. Para mayor comodidad, también está disponible la edición in situ del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Título, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Título.

| Versión de AEM | Componente de título v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Título.
>
>Para obtener más información sobre la versión actual del componente Título, consulte el documento Componente [](title.md) Título.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](versions.md#main-pars_title_236368006) para obtener más información.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título y seleccionar el nivel del encabezado.

>[!NOTE]
>
>Un valor vacío para el título hará que se muestre el título de la página.

![](assets/chlimage_1-91.png)

El editor in-situ también puede utilizarse para editar el texto del componente de título.

![](assets/chlimage_1-37.png)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

![](assets/chlimage_1-92.png)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.
