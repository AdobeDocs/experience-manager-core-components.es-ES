---
title: Componente de sendero de exploración (v 1)
seo-title: Componente de sendero de exploración (v 1)
description: El componente de ruta de componente principal es un componente de navegación que crea una ruta de vínculos basada en la ubicación de la página en la jerarquía de contenido.
seo-description: El componente de ruta de componente de AEM Core es un componente de navegación que crea una ruta de vínculos basada en la ubicación de la página en la jerarquía de contenido.
uuid: c 1 f 20 a 82-b 6 ff -4 a 3 c -920 a -6710084 a 69 f 2
content-type: referencia
topic-tags: componentes principales
discoiquuid: 0 b 3 a 7 d 8 f-d 110-424 f-b 531-ff 88 c 9 a 09128
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de sendero de exploración (v 1){#breadcrumb-component-v}

El componente de ruta de componente principal es un componente de navegación que crea una ruta de vínculos basada en la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente de sendero de exploración muestra la posición de la página actual dentro de la jerarquía del sitio, permitiendo que los visitantes de la página naveguen por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad para mostrar la página actual u páginas ocultas, pueden ser definidas por el autor de la plantilla en el cuadro de diálogo [de diseño](breadcrumb-v1.md#main-pars_title_1995166862). El editor de contenido puede elegir si las páginas ocultas deben mostrarse o no y el nivel de navegación real del componente en el cuadro de diálogo [de edición](breadcrumb-v1.md#main-pars_title).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Breadcrumb, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de la versión 1 del componente de Sendero de exploración.

| Versión de AEM | Componente de sendero de exploración v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de sendero de exploración.
>Para obtener más información sobre la versión actual del componente de ruta de exploración, consulte [el documento Componente](breadcrumb.md) de sendero de exploración.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite que el autor del contenido suprima las páginas ocultas y activas en las rutas, así como la profundidad en la jerarquía que debería mostrar.

![](assets/chlimage_1-34.png)

* **Nivel de navegación para empezar** : en la jerarquía, el componente de sendero de navegación debería comenzar a desplazarse hacia la página actual. Por ejemplo, en We. Retail:

   * 1 comienza en `/content/we-retail`
   * 2 comienza en `/content/we-retail/<country>`

* **Mostrar oculto** : Mostrar las páginas marcadas como ocultas en la ruta (de forma predeterminada, no se mostrarán)
* **Ocultar actual**: Eliminar la página actual en la ruta (de forma predeterminada se mostrará)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los valores predeterminados para las opciones para eliminar las páginas ocultas y activas en las rutas, así como la profundidad en la jerarquía que debería mostrar.

![](assets/chlimage_1-35.png)

* **Nivel de navegación para empezar** : define el valor predeterminado de donde en la jerarquía el componente de sendero de exploración debería comenzar a bajar a la página actual cuando se agrega el componente de sendero de migas a una página.
* **Mostrar oculto** : define el valor predeterminado de la opción **Mostrar oculto** cuando se agrega el componente de sendero de migas a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar actual** : define el valor predeterminado de la opción **Ocultar actual** cuando se agrega el componente de sendero de migas a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de sendero de exploración [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
