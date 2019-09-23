---
title: Componente de lista
seo-title: Componente de lista
description: nulo
seo-description: El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
uuid: 50a572e8-b444-4f7d-82bc-5a93ebb4be95
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: 89053323-6221-46ed-896a-31a42c55282e
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

El componente Lista se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente. El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el cuadro de diálogo [](#design-dialog)de diseño. El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el cuadro de diálogo [de](#edit-dialog)edición.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Lista es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](list-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Lista, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [](http://opensource.adobe.com/aem-core-wcm-components/library/list.html)de componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y los elementos de la lista.

### Ficha Configuración de lista {#list-settings-tab}

La lista se puede crear de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Buscar](#search-options)
* [Etiquetas](#tags)

Independientemente de cómo se cree la lista, hay opciones [de](#sort-options) ordenación que siempre se pueden configurar.

![](assets/chlimage_1-38.png)

Según el modo en que el autor elija crear la lista, cambiarán las opciones de configuración adicionales.

#### Páginas secundarias {#child-pages}

La lista se puede crear con las páginas secundarias de la página actual u otra página.

![](assets/chlimage_1-39.png)

* **Página principal**
   * La página cuyas páginas secundarias deben crear la lista
   * Deje en blanco para utilizar la página actual

* **Profundidad** secundaria Cuántos niveles inferiores de la jerarquía se deben utilizar

#### Fixed List {#fixed-list}

La lista se puede crear con una lista fija de elementos.

![](assets/chlimage_1-40.png)

Toque o haga clic en el botón **Agregar** para insertar un nuevo elemento en la lista.

* Introduzca texto para el elemento en la lista o utilice el cuadro de diálogo **** Selección para elegir un elemento de AEM.
* Utilice el controlador de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search-options}

La lista se puede crear con los resultados de una búsqueda de contenido de AEM.

![](assets/chlimage_1-41.png)

* **Consulta** de búsqueda La cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de lista
* **Buscar** donde se debe ejecutar la búsqueda
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear con páginas que coincidan con determinadas etiquetas en una ubicación determinada.

![](assets/chlimage_1-42.png)

* **Página** principalDónde debe comenzar la coincidencia de etiquetas
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco
* **Etiquetas** Qué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Examinar** para seleccionar las etiquetas
* **Coincidencia** Defina qué tipo de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija crear la lista, hay ciertas opciones de ordenación que siempre se pueden definir.

![](assets/chlimage_1-43.png)

* **Ordenar por** cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden** El orden en el que se deben ordenar los elementos
   * **ascendente**
   * **descendente**
* **Número máximo de elementos** Número máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.

### Ficha Configuración de elemento {#item-settings-tab}

Mediante la ficha Configuración de elemento, se puede configurar el formato de los elementos de lista.

![](assets/chlimage_1-44.png)

* **Vincular elementos** Vincular elementos a la página correspondiente
* **Mostrar descripción** Mostrar descripciones del elemento de vínculo
* **Mostrar fecha** Mostrar fecha de modificación del elemento de vínculo

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los tipos de listas que deben permitirse a los autores de contenido, así como la configuración del elemento disponible.

### Ajustes de la lista {#list-settings}

En la ficha Configuración **de** lista, se puede definir el formato de fecha, así como el tipo de listas que deben estar disponibles en el componente para los autores de contenido.

![](assets/chlimage_1-45.png)

* **Formato** de fecha que se usará para mostrar la fecha de la última modificación
* **Deshabilitar elementos secundarios** Desactive el tipo de lista de elementos secundarios del componente
* **Deshabilitar estático** Deshabilitar el tipo de lista estática en el componente
* **Deshabilitar la búsqueda** Deshabilite el tipo de lista de búsqueda en el componente
* **Deshabilitar etiquetas** Deshabilitar tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings}

En la ficha Configuración **de** elemento, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![](assets/chlimage_1-46.png)

* **Vincular elementos** Habilitar elementos de vínculo en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar descripciones** Habilitar la opción Mostrar descripciones en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar fecha** Activar la opción Mostrar fecha en el cuadro de diálogo [Editar](#edit-dialog)

### Ficha Estilos {#styles-tab}

El componente Imagen admite el sistema [de](authoring.md#component-styling)estilo AEM.