---
title: Componente de lista
description: El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 4%

---


# Componente de lista{#list-component}

El componente Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente. El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de lista es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/list-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de lista, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_list).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de lista [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y los elementos de la lista.

### Pestaña Configuración de lista {#list-settings-tab}

La lista se puede crear de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Buscar](#search-options)
* [Etiquetas](#tags)

Independientemente de cómo se cree la lista, hay [Opciones de ordenación e ID](#sort-options) que siempre se pueden configurar.

![Cuadro de diálogo Editar componente de lista](/help/assets/list-edit.png)

Según la forma en que el autor del contenido elija crear la lista, cambiarán las opciones de configuración adicionales.

#### Páginas secundarias {#child-pages}

La lista se puede crear a partir de las páginas secundarias de la página actual u otra página.

![Opciones de página secundarias](/help/assets/list-edit-child-pages.png)

* **Página principal**
   * La página cuyas páginas secundarias deben aparecer en la lista
   * Dejar en blanco para usar la página actual

* **Profundidad-**
secundariaCuántos niveles inferiores en la jerarquía deben usarse

#### Lista fija {#fixed-list}

La lista se puede crear con una lista fija de elementos.

![Opciones de lista fijas](/help/assets/list-edit-fixed.png)

Toque o haga clic en el botón **Add** para insertar un nuevo elemento en la lista.

* Escriba texto para el elemento en la lista o utilice el **Cuadro de diálogo de selección** para elegir un elemento de AEM.
* Utilice el control de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search-options}

La lista se puede crear utilizando los resultados de una búsqueda de contenido AEM.

![Opciones de la lista de búsqueda](/help/assets/list-edit-search.png)

* **Consulta de**
búsquedaLa cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de la lista
* **Buscar**
enDonde se debe ejecutar la búsqueda
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear utilizando páginas que coincidan con determinadas etiquetas en una ubicación concreta.

![Opciones de la lista de etiquetas](/help/assets/list-edit-tags.png)

* **Página principal**
Donde debería comenzar la coincidencia de etiquetas
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco
* ****
EtiquetasQué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Browse** para seleccionar las etiquetas
* ****
MatchDefine qué tipo de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija crear la lista, hay ciertas opciones de clasificación que siempre se pueden definir.

![Opciones de ordenación](/help/assets/list-edit-sort-options.png)

* **Ordenar**
porCómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden**
de clasificaciónEl orden en el que se deben ordenar los elementos
   * **ascendente**
   * **descendente**
* **Máximo de**
elementosNúmero máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### Pestaña Configuración de elementos {#item-settings-tab}

Con la ficha Configuración de elementos , se puede configurar el formato de los elementos de la lista.

![Configuración de elementos](/help/assets/list-edit-items.png)

* **Vincular**
elementosVincular elementos a la página correspondiente
* **Mostrar**
descripciónMostrar descripciones del elemento de vínculo
* **Mostrar**
fechaMostrar fecha de modificación del elemento de vínculo

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué tipos de listas se deben permitir a los autores de contenido, así como la configuración de elementos disponible.

### Ajustes de la lista {#list-settings}

En la pestaña **Configuración de lista**, se puede definir el formato de fecha y qué tipo de listas deben estar disponibles en el componente para los autores de contenido.

![Configuración de la lista de cuadros de diálogo de diseño del componente de lista](/help/assets/list-design-list-settings.png)

* **Date**
FormatFormat que se utilizará para mostrar la fecha de la última modificación
* **Desactivar**
elementos secundariosDesactivar el tipo de lista secundaria en el componente
* **Desactivar**
staticDesactivar el tipo de lista estática en el componente
* **Desactivar**
búsquedaDesactivar el tipo de lista de búsqueda en el componente
* **Deshabilitar**
etiquetasDeshabilitar tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings}

En la pestaña **Configuración de elementos**, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![Configuración del elemento de diálogo de diseño del componente de lista](/help/assets/list-design-item-settings.png)

* **Vincular**
elementosHabilitar elementos de vínculo en el cuadro de diálogo de  [edición](#edit-dialog)
* **Mostrar**
descripcionesActive la opción Mostrar descripciones en el cuadro de diálogo de  [edición](#edit-dialog)
* **Mostrar**
fechaActive la opción Mostrar fecha en el cuadro de diálogo de  [edición](#edit-dialog)

### Pestaña Estilos {#styles-tab}

El componente Imagen es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Lista es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
