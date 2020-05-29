---
title: Componente de título
description: El componente Título del componente principal es un componente de encabezado de sección que incluye la edición in-situ.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 3%

---


# Componente de título{#title-component}

El componente Título del componente principal es un componente de encabezado de sección que incluye la edición in-situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido. El autor de la plantilla puede definir los niveles de encabezado disponibles en el cuadro de diálogo [de](#design-dialog)diseño. El editor de contenido puede seleccionar los niveles de encabezados disponibles en el cuadro de diálogo [de](#edit-dialog)edición. Para mayor comodidad, también está disponible la edición in situ del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Título es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | - | Compatible | Compatible | Compatible |
| [v1](v1/title-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Título, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [](https://adobe.com/go/aem_cmp_library_title)de componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_title_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título y seleccionar el nivel del encabezado.

* **Título** : si está vacío, se utilizará el título de la página
* **Tipo/Tamaño** : define el nivel de encabezado del título
* **Vínculo** : define el contenido al que se vinculará el título. Puede ser una ruta a una página de contenido, una dirección URL externa o un anclaje de página.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente Título](/help/assets/title-edit.png)

>[!NOTE]
>
>La capacidad de definir un vínculo para el título se introdujo con la versión 2.2.0 de los componentes principales.

El editor in-situ también puede utilizarse para editar el texto del componente de título.

![Edición in situ del componente Título](/help/assets/title-edit-inline.png)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

### Ficha Tamaños {#sizes-tab}

![Cuadro de diálogo de diseño del componente Título](/help/assets/title-design.png)

* **Tipos permitidos / Tamaños para autores** : habilite o deshabilite los tipos de encabezados que estarán disponibles para los autores de contenido cuando usen el componente Título.
* **Tipo/Tamaño** predeterminado: defina el tipo de encabezado que se asignará automáticamente cuando un autor de contenido agregue el componente Título a una página.
* **Deshabilitar vínculo**: deshabilite la compatibilidad con vínculos en el componente de título para impedir que los autores de contenido se vinculen desde títulos.

>[!NOTE]
>
>La capacidad de definir un vínculo para el título se introdujo con la versión 2.2.0 de los componentes principales.

### Ficha Estilos {#styles-tab}

El componente Título admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
