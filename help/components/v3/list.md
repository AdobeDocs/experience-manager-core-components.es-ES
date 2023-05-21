---
title: Componente Lista (versión 3)
description: El componente principal de lista (versión 3) permite crear fácilmente listas dinámicas y estáticas.
role: Architect, Developer, Admin, User
exl-id: 4aefce2e-9c22-4c6d-869e-aaa8c246b073
source-git-commit: d86cb826922330f9877a725b84eb1844e1d5c0b7
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 100%

---

# Componente Lista (versión 3) {#list-component}

El componente principal de lista (versión 3) permite crear fácilmente listas dinámicas y estáticas.

## Uso {#usage}

El componente de lista (versión 3) se puede utilizar para crear, por ejemplo, una lista dinámica de páginas secundarias o una estática de elementos definidos arbitrariamente. El autor de la plantilla puede definir el tipo de listas disponibles y las opciones de formato en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los tipos de lista disponibles y cómo dar formato a los elementos de la lista en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 3 del componente de lista, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022.

>[!CAUTION]
>
>Este documento describe la versión 3 del componente Lista.
>
>Para obtener más información sobre la versión actual del componente Lista, consulte el documento [Componente Lista](/help/components/list.md).

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| [Versión 4](/help/components/list.md) | - | Compatible | Compatible |
| Versión 3 | - | Compatible | Compatible |
| [Versión 2](/help/components/v2/list.md) | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/list-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Redirecciones en listas {#redirects}

Cuando una página tiene un objetivo de redirección (independientemente de si apunta a una dirección URL externa o a otra página de AEM), cualquier lista que contenga vínculos hacia ahí apunta directamente a la dirección URL del destino de redirección.

### Ejemplo {#redirect-example}

* Cree una página A que redirija a la página B.
* Cree una página C que redirija a `https://aemcomponents.dev`
* En una página D, inserte un componente de lista que contenga las páginas A y C
* Los vínculos respectivos que se generan apuntan directamente a la página B y `https://aemcomponents.dev`

## Salida del componente de ejemplo {#sample-component-output}

Para visualizar el componente Lista, ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_list_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_list_v3_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido configurar la lista y los elementos de la lista.

### Pestaña de configuración de la lista {#list-settings-tab}

La lista se puede generar de diferentes maneras.

* [Páginas secundarias](#child-pages)
* [Lista fija](#fixed-list)
* [Búsqueda](#search-options)
* [Etiquetas](#tags)

Independientemente de cómo se genere la lista, hay [Opciones de ordenación e ID](#sort-options) que siempre se pueden configurar.

![Cuadro de diálogo de edición del componente Lista](/help/assets/v3/list-edit.png)

Según la forma en la que el autor del contenido elija crear la lista, las opciones de configuración adicionales cambiarán.

#### Páginas secundarias {#child-pages}

La lista se puede crear a partir de las páginas secundarias de la página actual o de otra página.

![Opciones de página secundarias](/help/assets/v3/list-edit-child-pages.png)

* **Página principal**
   * La página cuyas páginas secundarias deben aparecer en la lista
   * Déjelo en blanco para utilizar la página actual

* **Profundidad secundaria**
Cuántos niveles inferiores en la jerarquía deben usarse

#### Lista fija {#fixed-list}

La lista se puede crear mediante una lista fija de elementos.

![Opciones de listas fijas](/help/assets/v3/list-edit-fixed.png)

Pulse o haga clic en el botón **Añadir** para insertar un nuevo elemento en la lista.

* Escriba texto para el elemento de la lista o utilice el **Cuadro de diálogo de selección** para elegir un elemento de AEM.
* Utilice el controlador de arrastre para reorganizar los elementos de la lista.
* Utilice el icono de la papelera para eliminar elementos de la lista.

#### Búsqueda {#search-options}

La lista se puede crear utilizando los resultados de una búsqueda de contenido de AEM.

![Opciones de la lista de búsqueda](/help/assets/v3/list-edit-search.png)

* **Consulta de búsqueda**
La cadena para la que se ejecutará una búsqueda de texto completo para generar los elementos de la lista
* **Buscar en**
Dónde se debe ejecutar la búsqueda
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Si se deja en blanco se usará la página actual

#### Etiquetas {#tags}

La lista se puede crear utilizando páginas que coincidan con determinadas etiquetas en una ubicación concreta.

![Opciones de la lista de etiquetas](/help/assets/v3/list-edit-tags.png)

* **Página principal**
Donde debería comenzar la coincidencia de etiquetas
   * Utilice el **Cuadro de diálogo de selección** para elegir la ubicación en AEM
   * Si se deja en blanco se usará la página actual
* **Etiquetas**
Qué etiquetas deben coincidir
   * Utilice el cuadro de diálogo **Examinar** para seleccionar las etiquetas
* **Coincidencias**
Define qué tipo de coincidencias debe presentar una página para incluirla en la lista
   * **cualquier etiqueta**
   * **todas las etiquetas**

#### Opciones de ordenación {#sort-options}

Independientemente de cómo elija generar la lista, hay ciertas opciones de clasificación que siempre se pueden definir.

![Opciones de ordenación](/help/assets/v3/list-edit-sort-options.png)

* **Ordenar por**
Cómo se deben ordenar los elementos
   * **Título**
   * **Fecha de la última modificación**
* **Orden de clasificación**
El orden en el que se deben ordenar los elementos
   * **ascendente**
   * **descendente**
* **Artículos máximos**
Número máximo de elementos mostrados en la lista.
   * Déjelo vacío para ver todos los elementos.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña de configuración de elementos {#item-settings-tab}

Con la pestaña Configuración de elementos, se puede configurar el formato de los elementos de la lista.

![Configuración del elemento](/help/assets/v3/list-edit-items.png)

* **Vincular elementos**: vincular elementos a la página correspondiente
* **Mostrar descripción**: mostrar descripciones del elemento de vínculo
* **Mostrar fecha**: mostrar fecha de modificación del elemento vinculado
* **Mostrar como teaser**: cuando está marcado, el elemento se muestra como teaser

### Pestaña Estilos {#styles-tab-edit}

El componente Lista es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

![Pestaña Propiedades del cuadro de diálogo de edición del componente Lista](/help/assets/v3/list-edit-styles.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué tipos de listas se deben permitir a los autores de contenido, así como la configuración de elementos disponible.

### Ajustes de la lista {#list-settings}

En la pestaña **Configuración de la lista**, se puede definir el formato de fecha y qué tipo de listas deben estar disponibles en el componente para los autores de contenido.

![Configuración de la lista de cuadros de diálogo de diseño del componente Lista](/help/assets/v3/list-design-list-settings.png)

* **Formato de fecha**:
Formato que se usará para visualizar la fecha de la última modificación
* **Deshabilitar elementos secundarios**
Deshabilitar el tipo de lista secundaria en el componente
* **Deshabilitar estáticas**
Deshabilitar el tipo de lista estática en el componente
* **Deshabilitar búsqueda**
Deshabilitar el tipo de lista de búsqueda en el componente
* **Deshabilitar etiquetas**
Deshabilitar tipo de lista de etiquetas en el componente

### Configuración del elemento {#item-settings}

En la pestaña **Configuración de elementos**, se pueden definir las opciones de formato para los elementos de lista individuales que deben estar disponibles en el componente para los autores de contenido.

![Configuración del elemento de diálogo de diseño del componente Lista](/help/assets/v3/list-design-item-settings.png)

* **Vincular elementos**
Habilitar vincular elementos en el [cuadro de diálogo de edición](#edit-dialog)
* **Mostrar descripciones**
Habilitar la opción Mostrar descripciones en el [cuadro de diálogo de edición](#edit-dialog)
* **Mostrar fecha**
Habilitar la opción Mostrar fecha en el [cuadro de diálogo de edición](#edit-dialog)

### Pestaña Estilos {#styles-tab}

El componente Imagen es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Lista es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
