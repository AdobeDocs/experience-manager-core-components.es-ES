---
title: Componente Título (Versión 2)
description: El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.
role: Architect, Developer, Admin, User
source-git-commit: e5251010ca41025eb2bb56b66164ecf4cc0145c8
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 94%

---


# Componente Título (versión 2) {#title-component}

El componente principal Título es un componente de encabezado de sección que incluye la edición in situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido. El autor de la plantilla puede definir los niveles de encabezado disponibles en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede seleccionar entre los niveles de encabezados disponibles en el [cuadro de diálogo de edición](#edit-dialog). Para ofrecer una mayor comodidad, también está disponible la edición in situ simple del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 2 del componente Título , que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018.

>[!CAUTION]
>
>Este documento describe la versión 2 del componente Título.
>
>Para obtener más información sobre la versión actual del componente Título, consulte el documento [Componente Ttítulo](/help/components/title.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Título, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_title_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_title_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

* **Título**: si está vacío, se utilizará el título de la página
* **Tipo / Tamaño**: define el nivel de encabezado del título
* **Vínculo**: define el contenido al que se vinculará el título. Puede ser una ruta a una página de contenido, una URL externa o un anclaje de página.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente Título](/help/assets/title-edit.png)

>[!NOTE]
>
>La capacidad para definir un vínculo para el título se introdujo en la versión 2.2.0 de los componentes principales.

El editor in situ también se puede utilizar para editar el texto del componente de título.

![Edición in situ del componente Título](/help/assets/title-edit-inline.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

### Pestaña Tamaños {#sizes-tab}

![Cuadro de diálogo de diseño del componente Título](/help/assets/title-design.png)

* **Tipos permitidos/tamaños para autores**: habilite o deshabilite los tipos de encabezados que estarán disponibles para los autores de contenido cuando usen el componente Título.
* **Tipo/tamaño predeterminado**: defina el tipo de encabezado que se asignará automáticamente cuando un autor de contenido añada el componente Título a una página.
* **Deshabilitar el vínculo**: desactive la compatibilidad con vínculos en el componente de título para impedir que los autores de contenido se vinculen desde títulos.

>[!NOTE]
>
>La capacidad para definir un vínculo para el título se introdujo en la versión 2.2.0 de los componentes principales.

### Pestaña Estilos {#styles-tab}

El componente Título es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Título es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
