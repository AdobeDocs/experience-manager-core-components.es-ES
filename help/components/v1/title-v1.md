---
title: Componente Título (versión 1)
description: El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.
index: n
role: Architect, Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Título (versión 1) {#title-component-v}

El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido.

El autor de la plantilla puede definir los niveles de encabezado disponibles en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los niveles de encabezados disponibles en el [cuadro de diálogo de edición](#edit-dialog). Para ofrecer una mayor comodidad, también está disponible la edición in situ simple del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Título, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de la versión 1 del componente Título.

| Versión de AEM | Componente Título de (versión 1) |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Título.
>
>Para obtener más información sobre la versión actual del componente Título, consulte el documento [Componente Ttítulo](/help/components/title.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-36.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

>[!NOTE]
>
>Si el título está vacío, se mostrará el título de la página.

![](/help/assets/chlimage_1-91.png)

El editor in situ también se puede utilizar para editar el texto del componente de título.

![](/help/assets/chlimage_1-37.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

![](/help/assets/chlimage_1-92.png)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
