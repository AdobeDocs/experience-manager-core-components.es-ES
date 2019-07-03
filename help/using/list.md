---
title: Componente de lista
seo-title: Componente de lista
description: nulo
seo-description: El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
uuid: 50 a 572 e 8-b 444-4 f 7 d -82 bc -5 a 93 ebb 4 be 95
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 89053323-6221-46 ed -896 a -31 a 42 c 55282 e
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
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Componente de lista{#list-component}

El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista puede utilizarse para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente. The type of lists available and formatting options can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available list types and how to format the list elements in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente de lista es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](list-v1.md) | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the List Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### Technical Details {#technical-details}

The latest technical documentation about the List Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor de contenido configurar la lista y los elementos de lista.

### List Settings Tab {#list-settings-tab}

La lista puede generarse de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Buscar](#search-options)
* [Etiquetas](#tags)

Regardless of how the list is built, there are [Sort Options](#sort-options) that can always be configured.

![](assets/chlimage_1-38.png)

Según cómo elija el autor de contenido crear la lista, las opciones de configuración adicionales cambiarán.

#### Páginas secundarias {#child-pages}

La lista puede generarse de las páginas secundarias de la página actual u otra página.

![](assets/chlimage_1-39.png)

* **Página principal**
   * Página cuyas páginas secundarias deben hacer la lista
   * Deje en blanco para utilizar la página actual

* **Profundidad secundaria**
en la que se deben utilizar los niveles inferiores en la jerarquía

#### Fixed List {#fixed-list}

La lista se puede crear con una lista fija de elementos.

![](assets/chlimage_1-40.png)

Tap or click the **Add** button to inset a new item to the list.

* Enter text for the item in the list or use the **Selection Dialog** to choose an item from AEM.
* Utilice el control de arrastrar para reorganizar los elementos en la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search-options}

La lista se puede crear con los resultados de una búsqueda del contenido de AEM.

![](assets/chlimage_1-41.png)

* **Consulta
de búsqueda** La cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de la lista
* **Buscar en**
dónde se debe ejecutar la búsqueda
   * Use the **Selection Dialog** to choose the location in AEM
   * Utilizar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear utilizando páginas que coincidan con determinadas etiquetas en una ubicación determinada.

![](assets/chlimage_1-42.png)

* **Página
principal** donde la coincidencia de etiquetas debería comenzar
   * Use the **Selection Dialog** to choose the location in AEM
   * Utilizar la página actual si se deja en blanco
* **Etiquetas**
que deben coincidir con etiquetas
   * Use the **Browse** dialog to select the tags
* **Coincide**
Definir qué clase de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Sort Options {#sort-options}

Independientemente de cómo elija crear la lista, hay determinadas opciones de clasificación que siempre se pueden definir.

![](assets/chlimage_1-43.png)

* **Ordenar por**
cómo deben ordenarse los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Ordenar El**
orden en el que deben ordenarse los elementos
   * **ascendente**
   * **descendente**
* **Número máximo de elementos**
Número máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.

### Item Settings Tab {#item-settings-tab}

Con la ficha Ajustes del elemento, se puede configurar el formato de los elementos de lista.

![](assets/chlimage_1-44.png)

* **Vincular elementos**
Vínculo Elementos a la página correspondiente
* **Mostrar descripción**
Mostrar descripción del elemento del vínculo
* **Mostrar fecha**de modificación Mostrar fecha
del elemento del vínculo

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los tipos de listas que deben permitirse los autores de contenido, así como los ajustes de elementos disponibles.

### Ajustes de la lista {#list-settings}

On the **List Settings** tab, the date format can be defined as well as what type of lists should be available in the component to the content authors.

![](assets/chlimage_1-45.png)

* **Formato de formato**
de fecha que se utilizará para la visualización de la última fecha de modificación
* **Deshabilitar elementos secundarios**
Deshabilitar el tipo de lista secundarios en el componente
* **Deshabilitar deshabilitar estático**
el tipo de lista estática del componente
* **Deshabilitar búsqueda**
Deshabilitar el tipo de lista de búsqueda en el componente
* **Deshabilitación de etiquetas**
Deshabilitar el tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings}

On the **Item Settings** tab, the formatting options for the individual list elements that should be available in the component for the content authors can be defined.

![](assets/chlimage_1-46.png)

* **Activar elementos de vínculo** La opción Elementos de vínculo en el cuadro [de diálogo de edición](#edit-dialog)
* **Mostrar descripciones**
Habilitar la opción Mostrar descripciones en el cuadro de diálogo [de edición](#edit-dialog)
* **Mostrar fecha**
de habilitación de fecha Mostrar fecha en el cuadro [de diálogo de edición](#edit-dialog)

### Styles Tab {#styles-tab}

The Image Component supports the AEM [Style System](authoring.md#component-styling).