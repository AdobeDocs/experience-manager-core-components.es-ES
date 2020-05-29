---
title: Componente de búsqueda rápida
description: El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio Web y presenta resultados de búsqueda para que los visitantes puedan buscar en el sitio y filtrar los resultados.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 2%

---


# Componente de búsqueda rápida {#quick-search-component}

El componente Búsqueda rápida proporciona funciones de búsqueda a un sitio web y presenta resultados de búsqueda para que los visitantes puedan encontrar fácilmente contenido y resultados de vista coincidentes.

## Uso {#usage}

El componente Búsqueda rápida oferta el sitio visitante la capacidad de buscar contenido, vista de los resultados in situ y navegar fácilmente a las páginas coincidentes. Los nuevos resultados se obtienen de forma dinámica a medida que el usuario se desplaza por los resultados de la búsqueda.

El cuadro de diálogo [de](#edit-dialog) edición permite al autor del contenido definir en qué parte del árbol de contenido debe inicio la búsqueda. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que debería comenzar la búsqueda en el árbol de contenido, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de búsqueda rápida es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

### Detalles técnicos {#technical-details}

>[!NOTE]
>
>La protección del componente de búsqueda o de cualquier aplicación basada en AEM contra los ataques DOS debe implementarse en un nivel superior, por ejemplo, mediante el uso `mod_security` en el despachante.

La documentación técnica más reciente sobre el componente de búsqueda rápida [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_search_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir dónde debería inicio la búsqueda en el árbol de contenido.

![Cuadro de diálogo de edición del componente de búsqueda rápida](/help/assets/quick-search-edit.png)

**Raíz** de búsqueda: la página raíz desde donde se inicio la búsqueda. La raíz de búsqueda puede ser un maestro de modelo, un maestro de idioma o una página normal.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

Mediante el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que debería comenzar la búsqueda en el árbol de contenido, así como un tamaño máximo del conjunto de resultados y una longitud mínima del término de búsqueda.El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Ficha Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente de búsqueda rápida](/help/assets/quick-search-design.png)

* **Raíz** de búsqueda El valor predeterminado de la raíz de búsqueda cuando un autor de contenido coloca el componente de búsqueda rápida en una página de contenido
* **Tamaño** de los resultados El número máximo de resultados obtenidos por una solicitud de búsqueda
* **Longitud** mínima del término de búsqueda Longitud mínima del término de búsqueda para inicio de la búsqueda

>[!NOTE]
>
>**El tamaño** de los resultados y la longitud **mínima del término de** búsqueda solo se pueden establecer en modo de diseño y, por lo tanto, solo en el nivel de plantilla, lo que significa que los autores de contenido no pueden modificar estos valores.

>[!CAUTION]
>
>**El tamaño** de los resultados y la longitud **mínima de los términos de** búsqueda pueden tener un impacto en el rendimiento si se establecen demasiado altos o demasiado bajos, respectivamente.

### Ficha Estilos {#styles-tab}

El componente Búsqueda rápida es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
