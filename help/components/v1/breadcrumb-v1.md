---
title: Componente de ruta de navegación (v1)
description: El componente de ruta de exploración del componente principal es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.
index: n
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 1%

---


# Componente de ruta de navegación (v1) {#breadcrumb-component-v}

El componente de ruta de exploración del componente principal es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente Ruta de navegación muestra la posición de la página actual dentro de la jerarquía del sitio, lo que permite a los visitantes navegar por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad de mostrar la página actual o las páginas ocultas, pueden ser definidas por el autor de la plantilla en el [cuadro de diálogo de diseño](#design-dialog). A continuación, el editor de contenido puede elegir si se deben mostrar o no páginas ocultas y el nivel de navegación real del componente en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de ruta de exploración, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de v1 del componente de ruta de exploración.

| Versión de AEM | Componente de ruta de navegación v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de ruta de exploración.
>Para obtener más información sobre la versión actual del componente de ruta de exploración, consulte el documento [Componente de ruta de exploración](/help/components/breadcrumb.md).

## Salida de componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales v1](/help/versions.md) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido suprimir las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![](/help/assets/chlimage_1-34.png)

* **Navigation-Level to start** : donde en la jerarquía el componente de ruta de exploración debe comenzar a caminar hacia abajo hasta la página actual. Por ejemplo, en We.Retail:

   * 1 empieza en `/content/we-retail`
   * 2 empieza en `/content/we-retail/<country>`

* **Mostrar oculto** : muestra las páginas marcadas como ocultas en la ruta de exploración (de forma predeterminada, no se mostrarán)
* **Ocultar actual**: elimine la página actual en la ruta de exploración (de forma predeterminada se mostrará)

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir cuáles son los valores predeterminados para que las opciones supriman las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debería mostrar.

![](/help/assets/chlimage_1-35.png)

* **Navigation-Level to start** : define el valor predeterminado para el lugar en la jerarquía en el que el componente de ruta de exploración debe comenzar a caminar hacia abajo hasta la página actual cuando se agrega el componente de ruta de exploración a una página.
* **Mostrar oculto** : define el valor predeterminado de la opción  **Mostrar** oculto cuando se agrega el componente de la ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar actual** : define el valor predeterminado de la opción  **Ocultar** actual cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de ruta de exploración [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
