---
title: Componente Lista (versión 1)
description: El componente principal Lista permite crear fácilmente listas dinámicas y estáticas.
index: n
role: Architect, Developer, Admin, User
exl-id: 510d059c-e60a-40aa-9032-66a901109f6e
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '854'
ht-degree: 100%

---

# Componente Lista (versión 1) {#list-component-v}

El componente principal Lista permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una estática de elementos definidos arbitrariamente.

El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Lista, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de la versión 1 del componente Lista.

| Versión de AEM | Versión 1 del componente Lista |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Lista.
>
>Para obtener más información sobre la versión actual del componente Lista, consulte el documento [Componente Lista](/help/components/list.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y sus elementos.

### Ajustes de la lista {#list-settings}

La lista se puede generar de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Búsqueda](#search-list)
* [Etiquetas](#tags)

Independientemente de cómo se genere la lista, hay [Opciones de clasificación](#sort-options) que siempre se pueden configurar.

![](/help/assets/chlimage_1-38.png)

Según la forma en la que el autor del contenido elija crear la lista, las opciones de configuración adicionales cambiarán.

#### Páginas secundarias {#child-pages}

La lista se puede crear a partir de las páginas secundarias de la página actual o de otra página.

![](/help/assets/chlimage_1-39.png)

* **Página principal**
   * La página cuyas páginas secundarias deben aparecer en la lista
   * Déjelo en blanco para utilizar la página actual
* **Profundidad-secundaria**: cuántos niveles inferiores de la jerarquía se deben usar

#### Lista fija {#fixed-list}

La lista se puede crear mediante una lista fija de elementos.

![](/help/assets/chlimage_1-40.png)

Pulse o haga clic en el botón **Añadir** para insertar un nuevo elemento en la lista.

* Escriba texto para el elemento de la lista o utilice el **Cuadro de diálogo de selección** para elegir un elemento de AEM.
* Utilice el controlador de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search-list}

La lista se puede crear utilizando los resultados de una búsqueda de contenido de AEM.

![](/help/assets/chlimage_1-41.png)

* **Consulta de búsqueda**: cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de la lista.
* **Buscar en**: donde se debe ejecutar la búsqueda
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Si se deja en blanco se usará la página actual

#### Etiquetas {#tags}

La lista se puede crear utilizando páginas que coincidan con determinadas etiquetas en una ubicación concreta.

![](/help/assets/chlimage_1-42.png)

* **Página principal**: donde se debería iniciar la coincidencia de etiquetas
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Si se deja en blanco se usará la página actual
* **Etiquetas**: qué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Examinar** para seleccionar las etiquetas
* **Coincidencia**: definir qué tipo de coincidencia debe condicionar a una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija generar la lista, hay ciertas opciones de clasificación que siempre se pueden definir.

![](/help/assets/chlimage_1-43.png)

* **Ordenar por**: cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden**: orden en el que se deben ordenar los elementos.
   * **ascendente**
   * **descendente**
* **Artículos máximos**: número máximo de elementos mostrados en la lista.
   * Déjelo vacío para ver todos los elementos.

### Configuración del elemento {#item-settings}

Con la pestaña **Configuración de elementos**, se puede configurar el formato de los elementos de la lista.

![](/help/assets/chlimage_1-44.png)

* **Vincular elementos**
Vincular elementos a la página correspondiente
* **Mostrar descripción**
Mostrar descripciones del elemento de vínculo
* **Mostrar fecha**
Mostrar fecha de modificación del elemento vinculado

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué tipos de listas se deben permitir a los autores de contenido, así como la configuración de elementos disponible.

### Ajustes de la lista {#list-settings-1}

En la pestaña **Configuración de la lista**, se puede definir el formato de fecha y qué tipo de listas deben estar disponibles en el componente para los autores de contenido.

![](/help/assets/chlimage_1-45.png)

* **Formato de fecha**: formato que se usará para visualizar la fecha de la última modificación
* **Deshabilitar elementos secundarios**: deshabilitar la lista de elementos secundarios en el componente
* **Deshabilitar estático**: deshabilitar la lista estática en el componente
* **Deshanilitar búsqueda**: deshabilitar la lista de búsqueda en el componente
* **Deshabilitar etiquetas**: deshabilitar la lista de etiquetas en el componente

### Configuración del elemento {#item-settings-1}

En la pestaña **Configuración de elementos**, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![](/help/assets/chlimage_1-46.png)

* **Elementos de vínculo**: habilitar la opción de elementos de vínculo en el [cuadro de diálogo de edición](#edit-dialog)
* **Mostrar descripciones**: activar la opción de mostrar descripciones en el [cuadro de diálogo de edición](#edit-dialog)
* **Mostrar fecha**: habilitar la opción de fecha en el [cuadro de diálogo de edición](#edit-dialog)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
