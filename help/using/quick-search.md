---
title: Componente de búsqueda rápida
seo-title: Componente de búsqueda rápida
description: nulo
seo-description: El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio Web y presenta resultados de búsqueda para que los visitantes puedan explorar el sitio y filtrar los resultados.
uuid: 1 ba 69 be 3-537 e -4 f 20-9 f 17-b 4 b 7174 a 8 e 88
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 906 a 684 d -5663-4497-bef 3-37 f 13 d 5 b 46 c 7
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de búsqueda rápida{#quick-search-component}

El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio Web y presenta resultados de búsqueda para que los visitantes puedan encontrar fácilmente el contenido coincidente y ver los resultados.

## Uso {#usage}

El componente Búsqueda rápida ofrece a los visitantes del sitio la capacidad de buscar contenido, ver los resultados en contexto y navegar fácilmente a las páginas coincidentes. Los resultados nuevos se recuperan de forma dinámica cuando el usuario se desplaza por los resultados de la búsqueda.

El cuadro [de diálogo de edición](#edit-dialog) permite que el autor de contenido defina en qué parte del árbol de contenido debería comenzar la búsqueda. Con el cuadro de diálogo [de diseño](#design-dialog), el autor de la plantilla puede establecer el valor predeterminado para donde en el árbol de contenido debería comenzar la búsqueda, así como un tamaño máximo de conjunto de resultados y longitud mínima de término de búsqueda.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Búsqueda rápida es v 1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### Detalles técnicos {#technical-details}

>[!NOTE]
>
>La protección del componente de búsqueda o de cualquier aplicación basada en AEM frente a los ataques DOS se debe implementar en un nivel superior, por ejemplo utilizando `mod_security` en el despachante.

La documentación técnica más reciente sobre el componente de búsqueda rápida [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite que el autor de contenido defina en qué parte del árbol de contenido debería comenzar la búsqueda.

![](assets/screen_shot_2018-04-03at120132.png)

**Raíz** de búsqueda: la página raíz desde la que se inicia la búsqueda. La raíz de búsqueda puede ser una página maestra, maestra de idioma o página normal de modelo.

## Cuadro de diálogo de diseño {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado donde en el árbol de contenido debe comenzar la búsqueda, como así también un tamaño máximo de conjunto de resultados y una longitud mínima del término de búsqueda. El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de formato de texto disponibles para los autores de contenido.

### Ficha Propiedades {#properties-tab}

![](assets/screen_shot_2018-04-03at120028.png)

* **Raíz
de búsqueda** El valor predeterminado de raíz de búsqueda cuando un autor de contenido coloca el componente de búsqueda rápida en una página de contenido
* **Tamaño
de los resultados** El número máximo de resultados obtenidos por una solicitud de búsqueda
* **Longitud mínima de la longitud**
mínima de la búsqueda del término de búsqueda para iniciar la búsqueda

>[!NOTE]
>
>**El tamaño** de los resultados y **la longitud** mínima de término de búsqueda solo se pueden establecer en modo de diseño y, por lo tanto, solo en el nivel de plantilla, lo que significa que los autores de contenido no pueden modificar estos valores.

>[!CAUTION]
>
>**El tamaño** de los resultados y **la longitud mínima de la búsqueda** pueden tener impacto en el rendimiento si se definen demasiado altos o demasiado bajos respectivamente.

### Ficha Estilos {#styles-tab}

El componente de búsqueda rápida admite el sistema [de estilos AEM](authoring.md#component-styling).