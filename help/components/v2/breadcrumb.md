---
title: Componente Ruta de exploración (versión 2)
description: El componente principal Ruta de exploración es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.
role: Architect, Developer, Admin, User
exl-id: 5f2e6fef-e2f6-48e2-8dac-008db3131044
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 99%

---

# Componente Ruta de exploración (versión 2) {#breadcrumb-component}

El componente principal Ruta de exploración es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente Ruta de exploración muestra la posición de la página actual dentro de la jerarquía del sitio, lo que permite a los visitantes navegar por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad de mostrar la página actual o las páginas ocultas, puede definirlas el autor de la plantilla en el [cuadro de diálogo de diseño](#design-dialog). A continuación, el editor de contenido puede elegir si se deben mostrar o no páginas ocultas y el nivel de navegación real del componente en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 2 del componente Ruta de exploración, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018.

>[!CAUTION]
>
>Este documento describe la versión 2 del componente Ruta de exploración.
>
>Para obtener más información sobre la versión actual del componente Ruta de exploración, consulte el documento [Componente Ruta de exploración](/help/components/breadcrumb.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Ruta de exploración, así como ver ejemplos de sus opciones de configuración, además de la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_breadcrumb_es).

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente Ruta de exploración es compatible con [los microdatos de schema.org](https://schema.org/BreadcrumbList).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Ruta de exploración [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido suprimir las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![Cuadro de diálogo de edición del componente Ruta de exploración](/help/assets/breadcrumb-edit.png)

* **Nivel de inicio de navegación**: punto de la jerarquía en el que el componente Ruta de exploración debe comenzar a desplazarse hacia abajo hasta la página actual. Por ejemplo:

   * 0 empieza en `/content`
   * 1 empieza en `/content/<yourSite>`
   * 2 empieza en `/content/<yourSite>/<country>`

* **Mostrar elementos de navegación ocultos**: mostrar páginas marcadas como ocultas en la ruta de exploración (de forma predeterminada, no se mostrarán)
* **Ocultar página actual**: elimine la página actual en la ruta de exploración (de forma predeterminada se mostrará).
* **Deshabilitar sombreado**: si la página en la jerarquía es una redirección, se mostrará el nombre de la página de redirección en lugar del destino. Consulte [Compatibilidad con estructuras de sitios sombreadas](../v1/navigation.md#shadow-structure) del componente Navegación para obtener más información.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir cuáles son los valores predeterminados para que las opciones supriman las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debería mostrar.

### Pestaña Principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Nivel de inicio de navegación**: define el valor predeterminado para el lugar en la jerarquía en el que el componente Ruta de exploración debe comenzar a avanzar hacia abajo hasta la página actual cuando se agrega el componente Ruta de exploración a una página.
* **Mostrar elementos de navegación ocultos**: define el valor predeterminado de la opción **Mostrar elementos de navegación ocultos** cuando se agrega el componente Ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar página actual**: define el valor predeterminado de la opción **Ocultar página actual** cuando se agrega el componente Ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Deshabilitar sombreado**: define el valor predeterminado de la opción **Deshabilitar sombreado** cuando se agrega el componente de ruta de exploración a una página.

### Pestaña Estilos {#styles-tab}

El componente Ruta de exploración es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Ruta de exploración es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
