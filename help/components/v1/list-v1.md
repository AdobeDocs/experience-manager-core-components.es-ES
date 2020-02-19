---
title: Componente de lista (v1)
description: El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# List Component (v1) {#list-component-v}

El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente.

El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el cuadro de diálogo [](#design-dialog)de diseño. El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el cuadro de diálogo [de](#edit-dialog)edición.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Lista, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v1 del componente Lista.

| Versión de AEM | Componente de lista v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Lista.
>
>Para obtener más información sobre la versión actual del componente de lista, consulte el documento Componente [de](/help/components/list.md) lista.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-47.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](/help/versions.md) para obtener más información.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y los elementos de la lista.

### Ajustes de la lista {#list-settings}

La lista se puede crear de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Buscar](#search-list)
* [Etiquetas](#tags)

Independientemente de cómo se cree la lista, hay opciones [de](#sort-options) ordenación que siempre se pueden configurar.

![](/help/assets/chlimage_1-38.png)

Según el modo en que el autor elija crear la lista, cambiarán las opciones de configuración adicionales.

#### Páginas secundarias {#child-pages}

La lista se puede crear con las páginas secundarias de la página actual u otra página.

![](/help/assets/chlimage_1-39.png)

* **Página principal**
   * La página cuyas páginas secundarias deben incluirse en la lista
   * Deje en blanco para utilizar la página actual
* **Profundidad** secundaria: cuántos niveles inferiores de la jerarquía se deben utilizar

#### Fixed List {#fixed-list}

La lista se puede crear con una lista fija de elementos.

![](/help/assets/chlimage_1-40.png)

Toque o haga clic en el botón **Agregar** para insertar un nuevo elemento en la lista.

* Introduzca texto para el elemento en la lista o utilice el cuadro de diálogo **** Selección para elegir un elemento de AEM.
* Utilice el controlador de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Buscar {#search-list}

La lista se puede crear con los resultados de una búsqueda de contenido de AEM.

![](/help/assets/chlimage_1-41.png)

* **Consulta** de búsqueda: la cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de lista
* **Buscar en** : donde se debe ejecutar la búsqueda
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear con páginas que coincidan con determinadas etiquetas en una ubicación determinada.

![](/help/assets/chlimage_1-42.png)

* **Página** principal: donde debe comenzar la coincidencia de etiquetas
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco
* **Etiquetas** : qué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Examinar** para seleccionar las etiquetas
* **Coincidencia** : defina qué tipo de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija crear la lista, hay ciertas opciones de ordenación que siempre se pueden definir.

![](/help/assets/chlimage_1-43.png)

* **Orden por** : cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden** : orden en el que se deben ordenar los artículos
   * **ascendente**
   * **descendente**
* **Máximo de elementos** : número máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.

### Ajustes del elemento {#item-settings}

Mediante la ficha Configuración **de** elemento, se puede configurar el formato de los elementos de la lista.

![](/help/assets/chlimage_1-44.png)

* **Vincular elementos** Vincular elementos a la página correspondiente
* **Mostrar descripción** Mostrar descripciones del elemento de vínculo
* **Mostrar fecha** Mostrar fecha de modificación del elemento de vínculo

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los tipos de listas que deben permitirse a los autores de contenido, así como la configuración del elemento disponible.

### Ajustes de la lista {#list-settings-1}

En la ficha Configuración **de** lista, se puede definir el formato de fecha, así como el tipo de listas que deben estar disponibles en el componente para los autores de contenido.

![](/help/assets/chlimage_1-45.png)

* **Formato** de fecha: formato que se usará para mostrar la fecha de la última modificación
* **Deshabilitar elementos secundarios** : desactive el tipo de lista de elementos secundarios en el componente
* **Deshabilitar estático** : Deshabilitar el tipo de lista estática en el componente
* **Deshabilitar la búsqueda** : Deshabilitar el tipo de lista de búsqueda en el componente
* **Deshabilitar etiquetas** : deshabilitar el tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings-1}

En la ficha Configuración **de** elemento, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![](/help/assets/chlimage_1-46.png)

* **Elementos** de vínculo: opción Activar elementos de vínculo en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar descripciones** : activar la opción Mostrar descripciones en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar fecha** : opción Activar la opción Mostrar fecha en el cuadro de diálogo [Editar](#edit-dialog)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.
