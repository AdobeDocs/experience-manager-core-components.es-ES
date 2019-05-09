---
title: Componente de lista (v 1)
seo-title: Componente de lista (v 1)
description: nulo
seo-description: El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
uuid: 06658 c 9 d-cbf 2-4 bfe-b 425-d 980 d 1181908
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 7 c 130 ccc -83 ff -464 d-b 58 f-d 581 f 4365 dbd
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
noindex: verdadero
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de lista (v 1){#list-component-v}

El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista puede utilizarse para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente.

El autor de plantillas puede definir el tipo de listas disponibles y las opciones de formato en el cuadro de diálogo [de diseño](list-v1.md#main-pars_title_1995166862). El editor de contenido puede seleccionar los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el cuadro de diálogo [de edición](list-v1.md#main-pars_title).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe v 1 del componente de lista, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v 1 del componente de lista.

| Versión de AEM | Componente de lista v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de lista.
>
>Para obtener más información sobre la versión actual del componente Lista, consulte [el documento Componente](list.md) de lista.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor de contenido configurar la lista y los elementos de lista.

### Ajustes de la lista {#list-settings}

La lista puede generarse de diferentes maneras.

* [Páginas secundarias](list-v1.md#main-pars_title_1861279796)
* [Lista fija](list-v1.md#main-pars_title_1227896889)
* [Buscar](list-v1.md#main-pars_title_1224003560)
* [Etiquetas](list-v1.md#main-pars_title_700759533)

Independientemente de cómo se genere la lista, hay Opciones [de orden](list-v1.md#main-pars_title_1568376452) que siempre pueden configurarse.

![](assets/chlimage_1-38.png)

Según cómo elija el autor de contenido crear la lista, las opciones de configuración adicionales cambiarán.

#### Páginas secundarias {#child-pages}

La lista puede generarse de las páginas secundarias de la página actual u otra página.

![](assets/chlimage_1-39.png)

* **Página principal**
   * Página cuyas páginas secundarias deben hacer la lista
   * Deje en blanco para utilizar la página actual
* **Profundidad secundaria** : la cantidad de niveles hacia abajo en la jerarquía debería usarse

#### Lista fija {#fixed-list}

La lista se puede crear con una lista fija de elementos.

![](assets/chlimage_1-40.png)

Toque o haga clic en el **botón Agregar** para insertar un nuevo elemento en la lista.

* Introduzca el texto del elemento en la lista o utilice el cuadro de diálogo **Selección** para elegir un elemento de AEM.
* Utilice el control de arrastrar para reorganizar los elementos en la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search}

La lista se puede crear con los resultados de una búsqueda del contenido de AEM.

![](assets/chlimage_1-41.png)

* **Consulta** de búsqueda: la cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de la lista
* **Buscar en** : donde se debe ejecutar la búsqueda
   * Utilizar el cuadro de diálogo **Selección** para elegir la ubicación en AEM
   * Utilizar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear utilizando páginas que coincidan con determinadas etiquetas en una ubicación determinada.

![](assets/chlimage_1-42.png)

* **Página** principal: donde la coincidencia de etiquetas debería comenzar
   * Utilizar el cuadro de diálogo **Selección** para elegir la ubicación en AEM
   * Utilizar la página actual si se deja en blanco
* **Etiquetas** : las etiquetas que deben coincidir
   * Uso del cuadro **de** diálogo Examinar para seleccionar las etiquetas
* **Coincidencia** : defina qué tipo de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija crear la lista, hay determinadas opciones de clasificación que siempre se pueden definir.

![](assets/chlimage_1-43.png)

* **Ordenar por** - Cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden** : el orden en el que deben ordenarse los elementos
   * **ascendente**
   * **descendente**
* **Elementos máximos** : número máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.

### Ajustes del elemento {#item-settings}

Con la ficha **Ajustes** del elemento, se puede configurar el formato de los elementos de lista.

![](assets/chlimage_1-44.png)

* **Vincular elementos**
Vínculo Elementos a la página correspondiente
* **Mostrar descripción**
Mostrar descripción del elemento del vínculo
* **Mostrar fecha**de modificación Mostrar fecha
del elemento del vínculo

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los tipos de listas que deben permitirse los autores de contenido, así como los ajustes de elementos disponibles.

### Ajustes de la lista {#list-settings-1}

En la ficha **Configuración** de lista, se puede definir el formato de fecha, así como el tipo de listas que debe estar disponible en el componente a los autores de contenido.

![](assets/chlimage_1-45.png)

* **Formato** de fecha: formato que se utilizará para la visualización de la última fecha de modificación
* **Deshabilitar elementos secundarios** : deshabilitar el tipo de lista secundaria en el componente
* **Deshabilitar estático** : deshabilitar el tipo de lista estática en el componente
* **Deshabilitar búsqueda** : Deshabilitar el tipo de lista de búsqueda en el componente
* **Deshabilitar etiquetas** : deshabilitar el tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings-1}

En la ficha **Ajustes** del elemento, se pueden definir las opciones de formato de los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![](assets/chlimage_1-46.png)

* **Vincular elementos** : habilitar la opción Elementos de vínculo en el cuadro [de diálogo de edición](list-v1.md#main-pars_title_550499279)
* **Mostrar descripciones** : Activar la opción Mostrar descripciones en el cuadro de diálogo [de edición](list-v1.md#main-pars_title_550499279)
* **Mostrar fecha** : habilitar la opción Mostrar fecha en el cuadro [de diálogo de edición](list-v1.md#main-pars_title_550499279)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [Lista se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
