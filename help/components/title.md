---
title: Componente Título
description: El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Título{#title-component}

El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.

{{traditional-aem}}

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido. El autor de la plantilla puede definir los niveles de encabezado disponibles en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los niveles de encabezados disponibles en el [cuadro de diálogo de edición](#edit-dialog). Para ofrecer una mayor comodidad, también está disponible la edición in situ simple del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Título es la versión 3, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| Versión 3 | - | Compatible | Compatible | Compatible |
| [Versión 2](v2/title.md) | Compatible | Compatible | - | Compatible |
| [Versión 1](v1/title-v1.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Título, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_title_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_title_v3_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

* **Título**: si está vacío, se utilizará el título de la página
* **Tipo / Tamaño**: define el nivel de encabezado del título
* **Vínculo**: define el contenido al que se vinculará el título. Puede ser una ruta a una página de contenido, una URL externa o un anclaje de página.
* **Abrir en ficha nueva**: cuando está activado, el vínculo se abre en una nueva pestaña del explorador.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente Título](/help/assets/title-edit.png)

El editor in situ también se puede utilizar para editar el texto del componente de título.

![Edición in situ del componente Título](/help/assets/title-edit-inline.png)

### Pestaña Estilos {#styles-tab-edit}

El componente Título es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

![Pestaña Estilos del cuadro de diálogo de edición del componente Título](/help/assets/title-edit-styles.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

### Pestaña Tamaños {#sizes-tab}

![Cuadro de diálogo de diseño del componente Título](/help/assets/title-design.png)

* **Tipos permitidos/tamaños para autores**: habilite o deshabilite los tipos de encabezados que estarán disponibles para los autores de contenido cuando usen el componente Título.
* **Tipo/tamaño predeterminado**: defina el tipo de encabezado que se asignará automáticamente cuando un autor de contenido añada el componente Título a una página.
* **Deshabilitar el vínculo**: desactive la compatibilidad con vínculos en el componente de título para impedir que los autores de contenido se vinculen desde títulos.

### Pestaña Estilos {#styles-tab}

El componente Título es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Título es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
