---
title: Componente de ruta de navegación (v1)
seo-title: Componente de ruta de navegación (v1)
description: El componente de ruta de navegación del componente principal es un componente de navegación que crea una ruta de navegación de vínculos en función de la ubicación de la página en la jerarquía de contenido.
seo-description: El componente de ruta de navegación del componente principal de AEM es un componente de navegación que crea una ruta de navegación de vínculos en función de la ubicación de la página en la jerarquía de contenido.
uuid: c1f20a82-b6ff-4a3c-920a-6710084a69f2
content-type: referencia
topic-tags: componentes principales
discoiquuid: 0b3a7d8f-d110-424f-b531-ff88c9a09128
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Breadcrumb Component (v1){#breadcrumb-component-v}

El componente de ruta de navegación del componente principal es un componente de navegación que crea una ruta de navegación de vínculos en función de la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente de ruta de navegación muestra la posición de la página actual dentro de la jerarquía del sitio, lo que permite a los visitantes navegar por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad de mostrar la página actual o las páginas ocultas, pueden ser definidas por el autor de la plantilla en el cuadro de diálogo [](breadcrumb-v1.md#main-pars_title_1995166862)de diseño. A continuación, el editor de contenido puede elegir si se deben mostrar o no las páginas ocultas y el nivel de navegación real del componente en el cuadro de diálogo [de](breadcrumb-v1.md#main-pars_title)edición.

## Versión y compatibilidad {#version-and-compatibility}

En este documento se describe la versión 1 del componente de ruta de navegación, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de la versión 1 del componente de ruta de navegación.

| Versión de AEM | Componente de ruta de navegación v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de ruta de exploración.
>Para obtener más información sobre la versión actual del componente de ruta de navegación, consulte el documento [Componente](breadcrumb.md) de ruta de navegación.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-33.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](versions.md#main-pars_title_236368006) para obtener más información.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido suprimir las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![](assets/chlimage_1-34.png)

* **Nivel de navegación para comenzar** : donde en la jerarquía el componente de ruta de exploración debe empezar a desplazarse hacia la página actual. Por ejemplo en We.Retail:

   * 1 empieza en `/content/we-retail`
   * 2 empieza en `/content/we-retail/<country>`

* **Mostrar ocultos** : mostrar páginas marcadas como ocultas en la ruta de exploración (de forma predeterminada, no se mostrarán)
* **Ocultar actual**: suprimir la página actual en la ruta de exploración (de forma predeterminada se mostrará)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los valores predeterminados para las opciones de supresión de las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![](assets/chlimage_1-35.png)

* **Navigation-Level to start** : Define el valor predeterminado para dónde en la jerarquía el componente de ruta de exploración debe empezar a desplazarse hacia abajo hasta la página actual cuando se agrega el componente de ruta de exploración a una página.
* **Mostrar oculto** : define el valor predeterminado de la opción **Mostrar oculto** cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar actual** : define el valor predeterminado de la opción **Ocultar actual** cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de ruta de navegación [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.
