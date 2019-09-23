---
title: Componente de búsqueda rápida
seo-title: Componente de búsqueda rápida
description: nulo
seo-description: El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio Web y presenta resultados de búsqueda para que los visitantes puedan buscar en el sitio y filtrar los resultados.
uuid: 1ba69be3-537e-4f20-9f17-b4b7174a8e88
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: 906a684d-5663-4497-bef3-37f13d5b46c7
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
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente de búsqueda rápida{#quick-search-component}

El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio Web y presenta resultados de búsqueda para que los visitantes puedan encontrar fácilmente contenido coincidente y ver los resultados.

## Uso {#usage}

El componente Búsqueda rápida ofrece a los visitantes del sitio la posibilidad de buscar contenido, ver los resultados en el sitio y navegar fácilmente a las páginas coincidentes. Los nuevos resultados se obtienen de forma dinámica a medida que el usuario se desplaza por los resultados de la búsqueda.

El cuadro de diálogo [de](#edit-dialog) edición permite al autor del contenido definir dónde debe iniciarse la búsqueda en el árbol de contenido. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que debería comenzar la búsqueda en el árbol de contenido, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de búsqueda rápida es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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
>La protección del componente de búsqueda o de cualquier aplicación basada en AEM contra los ataques DOS debe implementarse en un nivel superior, por ejemplo, mediante el uso `mod_security` en el despachante.

La documentación técnica más reciente sobre el componente de búsqueda rápida [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir dónde debe iniciarse la búsqueda en el árbol de contenido.

![](assets/screen_shot_2018-04-03at120132.png)

**Raíz** de búsqueda: la página raíz desde donde se inicia la búsqueda. La raíz de búsqueda puede ser un maestro de modelo, un maestro de idioma o una página normal.

## Cuadro de diálogo Diseño {#design-dialog}

Mediante el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que debería comenzar la búsqueda, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda.El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Ficha Propiedades {#properties-tab}

![](assets/screen_shot_2018-04-03at120028.png)

* **Raíz** de búsqueda El valor predeterminado de la raíz de búsqueda cuando un autor de contenido coloca el componente de búsqueda rápida en una página de contenido
* **Tamaño** de los resultados El número máximo de resultados obtenidos por una solicitud de búsqueda
* **Longitud** mínima del término de búsqueda Longitud mínima del término de búsqueda para iniciar la búsqueda

>[!NOTE]
>
>**El tamaño** de los resultados y la longitud **mínima del término de** búsqueda solo se pueden establecer en modo de diseño y, por lo tanto, solo en el nivel de plantilla, lo que significa que los autores de contenido no pueden modificar estos valores.

>[!CAUTION]
>
>**El tamaño** de los resultados y la longitud **mínima de los términos de** búsqueda pueden tener un impacto en el rendimiento si se establecen demasiado altos o demasiado bajos, respectivamente.

### Ficha Estilos {#styles-tab}

El componente Búsqueda rápida es compatible con el sistema [de](authoring.md#component-styling)estilo de AEM.