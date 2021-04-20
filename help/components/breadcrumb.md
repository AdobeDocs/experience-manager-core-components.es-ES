---
title: Componente de ruta de exploración
description: El componente de ruta de exploración del componente principal es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 2%

---


# Componente de ruta de exploración{#breadcrumb-component}

El componente de ruta de exploración del componente principal es un componente de navegación que crea una ruta de exploración de vínculos en función de la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente Ruta de navegación muestra la posición de la página actual dentro de la jerarquía del sitio, lo que permite a los visitantes navegar por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad de mostrar la página actual o las páginas ocultas, pueden ser definidas por el autor de la plantilla en el [cuadro de diálogo de diseño](#design-dialog). A continuación, el editor de contenido puede elegir si se deben mostrar o no páginas ocultas y el nivel de navegación real del componente en el [cuadro de diálogo de edición](#edit-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de ruta de exploración es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- | --- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/breadcrumb-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de ruta de exploración, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_breadcrumb).

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente de ruta de exploración es compatible con [schema.org microdata](https://schema.org/BreadcrumbList).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de ruta de exploración [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido suprimir las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![Cuadro de diálogo de edición de componentes de la ruta de exploración](/help/assets/breadcrumb-edit.png)

* **Nivel de inicio de navegación** : en el lugar de la jerarquía, el componente de ruta de exploración debe comenzar a desplazarse hacia abajo hasta la página actual. Por ejemplo:

   * 0 empieza en `/content`
   * 1 empieza en `/content/<yourSite>`
   * 2 empieza en `/content/<yourSite>/<country>`

* **Mostrar elementos de navegación ocultos** : mostrar páginas marcadas como ocultas en la ruta de exploración (de forma predeterminada, no se mostrarán)
* **Ocultar página actual** : elimine la página actual en la ruta de exploración (de forma predeterminada se mostrará).
* **Deshabilitar sombreado** : si la página en la jerarquía es una redirección, se mostrará el nombre de la página de redirección en lugar del destino. Consulte [Shadow Site Structure Support](navigation.md#shadow-structure) del componente de navegación para obtener más información.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir cuáles son los valores predeterminados para que las opciones supriman las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debería mostrar.

### Pestaña principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Nivel de inicio de navegación** : define el valor predeterminado para el lugar en la jerarquía en el que el componente de ruta de exploración debe comenzar a caminar hacia abajo hasta la página actual cuando se agrega el componente de ruta de exploración a una página.
* **Mostrar elementos de navegación ocultos** : Define el valor predeterminado de la opción  **Mostrar** elementos de navegación ocultos cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar página actual**: Define el valor predeterminado de la opción  **Ocultar** página actual cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Deshabilitar sombreado** : Define el valor predeterminado de la opción  **Deshabilitar** sombreado cuando se agrega el componente de ruta de exploración a una página.

### Pestaña Estilos {#styles-tab}

El componente Ruta de navegación es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Ruta de navegación es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
