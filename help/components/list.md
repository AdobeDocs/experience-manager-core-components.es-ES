---
title: Componente de lista
description: El componente de Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de lista{#list-component}

El componente de Lista de componentes principales permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente Lista se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una lista estática de elementos definidos arbitrariamente. El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el cuadro de diálogo [](#design-dialog)de diseño. El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de lista en el cuadro de diálogo [de](#edit-dialog)edición.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de Lista es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/list-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de Lista, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_list)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de Lista [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_list_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y los elementos de lista.

### Ficha Configuración de lista {#list-settings-tab}

La lista se puede construir de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Buscar](#search-options)
* [Etiquetas](#tags)

Independientemente de cómo se cree la lista, hay opciones [de](#sort-options) ordenación e ID que siempre se pueden configurar.

![Cuadro de diálogo de edición del componente de lista](/help/assets/list-edit.png)

Según el modo en que el autor elija crear la lista, cambiarán las opciones de configuración adicionales.

#### Páginas secundarias {#child-pages}

La lista se puede crear a partir de las páginas secundarias de la página actual u otra página.

![Opciones de página secundarias](/help/assets/list-edit-child-pages.png)

* **Página principal**
   * La página cuyas páginas secundarias deben realizar la lista
   * Deje en blanco para utilizar la página actual

* **Profundidad** secundaria Cuántos niveles inferiores de la jerarquía se deben utilizar

#### Fixed List {#fixed-list}

La lista se puede crear mediante una lista fija de elementos.

![Opciones de lista fijas](/help/assets/list-edit-fixed.png)

Toque o haga clic en el botón **Añadir** para insertar un nuevo elemento en la lista.

* Escriba el texto del elemento en la lista o utilice el cuadro de diálogo **** Selección para elegir un elemento de AEM.
* Utilice el controlador de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de papelera para eliminar elementos de la lista.

#### Búsqueda {#search-options}

La lista se puede crear utilizando los resultados de una búsqueda de contenido AEM.

![Opciones de lista de búsqueda](/help/assets/list-edit-search.png)

* **Consulta** de búsqueda La cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de lista
* **Buscar** donde se debe ejecutar la búsqueda
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco

#### Etiquetas {#tags}

La lista se puede crear con páginas que coincidan con determinadas etiquetas en una ubicación determinada.

![Opciones de lista de etiquetas](/help/assets/list-edit-tags.png)

* **Página** principalDónde debe inicio la coincidencia de etiquetas
   * Utilice el cuadro de diálogo **** Selección para elegir la ubicación en AEM
   * Usar la página actual si se deja en blanco
* **Etiquetas** Qué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Examinar** para seleccionar las etiquetas
* **Coincidencia** Defina qué tipo de coincidencia debe calificar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija crear la lista, hay ciertas opciones de ordenación que siempre se pueden definir.

![Opciones de ordenación](/help/assets/list-edit-sort-options.png)

* **Ordenar por** cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden** El orden en el que se deben ordenar los elementos
   * **ascendente**
   * **descendente**
* **Número máximo de elementos** Número máximo de elementos mostrados en la lista.
   * Deje vacío para devolver todos los elementos.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Ficha Configuración de elemento {#item-settings-tab}

Mediante la ficha Configuración de elemento, se puede configurar el formato de los elementos de lista.

![Configuración del elemento](/help/assets/list-edit-items.png)

* **Vincular elementos** Vincular elementos a la página correspondiente
* **Mostrar descripción** Mostrar descripciones del elemento de vínculo
* **Mostrar fecha** Mostrar fecha de modificación del elemento de vínculo

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los tipos de listas que deben permitirse a los autores de contenido, así como la configuración del elemento disponible.

### Ajustes de la lista {#list-settings}

En la ficha Configuración **de** Lista, se puede definir el formato de fecha, así como el tipo de listas que deben estar disponibles en el componente para los autores de contenido.

![Configuración de la lista del cuadro de diálogo de diseño del componente de lista](/help/assets/list-design-list-settings.png)

* **Formato** de fecha que se usará para mostrar la fecha de la última modificación
* **Deshabilitar elementos secundarios** Deshabilitar el tipo de lista secundarios en el componente
* **Deshabilitar estático** Deshabilitar el tipo de lista estática en el componente
* **Deshabilitar la búsqueda** Deshabilitar el tipo de lista de búsqueda en el componente
* **Deshabilitar etiquetas** Deshabilitar el tipo de lista de etiquetas en el componente

### Ajustes del elemento {#item-settings}

En la ficha Configuración **de** elemento, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![Configuración del elemento del cuadro de diálogo de diseño del componente de lista](/help/assets/list-design-item-settings.png)

* **Elementos** de vínculoOpción Activar elementos de vínculo en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar descripciones** Activar la opción Mostrar descripciones en el cuadro de diálogo [Editar](#edit-dialog)
* **Mostrar fecha** Habilitar la opción Mostrar fecha en el cuadro de diálogo [Editar](#edit-dialog)

### Ficha Estilos {#styles-tab}

El componente Imagen admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
