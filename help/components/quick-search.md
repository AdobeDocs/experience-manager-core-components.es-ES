---
title: Componente Búsqueda rápida
description: El componente Búsqueda rápida proporciona funciones de búsqueda en un sitio web y presenta resultados de búsqueda para que los visitantes puedan buscar en el sitio y filtrar los resultados.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Búsqueda rápida {#quick-search-component}

El componente Búsqueda rápida proporciona funciones de búsqueda en un sitio web y presenta resultados de búsqueda para que los visitantes puedan encontrar fácilmente contenido coincidente y ver resultados.

{{traditional-aem}}

## Uso {#usage}

El componente Búsqueda rápida permite a los visitantes del sitio buscar contenido, ver los resultados in situ y navegar fácilmente a las páginas coincidentes. Los nuevos resultados se obtienen de forma dinámica a medida que el usuario se desplaza por los resultados de la búsqueda.

El [cuadro de diálogo de edición](#edit-dialog) permite que el autor del contenido defina dónde debería comenzar la búsqueda en el árbol de contenido. Utilizando el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede establecer el valor predeterminado de dónde en el árbol de contenido debe comenzar la búsqueda, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Búsqueda rápida es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/quick-search.md) | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

### Detalles técnicos {#technical-details}

>[!NOTE]
>
>La protección del componente de búsqueda o de cualquier aplicación basada en AEM contra ataques DOS debe implementarse en un nivel superior, por ejemplo utilizando `mod_security` en Dispatcher.

La documentación técnica más reciente sobre el componente Búsqueda rápida [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_search_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite que el autor del contenido defina dónde debería comenzar la búsqueda en el árbol de contenido.

![Cuadro de diálogo de edición del componente Búsqueda rápida](/help/assets/quick-search-edit.png)

**Raíz de búsqueda**: página raíz desde la que se inicia la búsqueda. La raíz de búsqueda puede ser un modelo maestro, un idioma maestro o una página normal.
* **ID**: esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos.](/help/developing/data-layer/overview.md)
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

>[!NOTE]
>
>Si la **Raíz de búsqueda** no está configurada o no se puede resolver, la Búsqueda rápida toma como valor predeterminado la búsqueda debajo de la página actual.

## Cuadro de diálogo de diseño {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que en el árbol de contenido debe comenzar la búsqueda, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda. El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente Búsqueda rápida](/help/assets/quick-search-design.png)

* **Raíz de búsqueda**
El valor predeterminado de la raíz de búsqueda cuando un autor de contenido coloca el componente Búsqueda rápida en una página de contenido
* **Tamaño de los resultados**
El número máximo de resultados recuperados por una solicitud de búsqueda.
* **Longitud mínima del término de búsqueda**
Longitud mínima del término de búsqueda para iniciar la búsqueda

>[!NOTE]
>
>**El tamaño de los resultados** y **la longitud mínima del término de búsqueda** solo se pueden establecer en el modo de diseño y, por lo tanto, solo en el nivel de plantilla, lo que significa que los autores de contenido no pueden modificar estos valores.

>[!CAUTION]
>
>**El tamaño de los resultados** y **la longitud mínima del término de búsqueda** pueden tener un impacto en el rendimiento si se establecen demasiado altos o demasiado bajos, respectivamente.

### Pestaña Estilos {#styles-tab}

El componente Búsqueda rápida es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
