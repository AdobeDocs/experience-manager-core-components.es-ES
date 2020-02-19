---
title: Componente de ruta de navegación
description: El componente de ruta de navegación del componente principal es un componente de navegación que crea una ruta de navegación de vínculos en función de la ubicación de la página en la jerarquía de contenido.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de ruta de navegación{#breadcrumb-component}

El componente de ruta de navegación del componente principal es un componente de navegación que crea una ruta de navegación de vínculos en función de la ubicación de la página en la jerarquía de contenido.

## Uso {#usage}

El componente de ruta de navegación muestra la posición de la página actual dentro de la jerarquía del sitio, lo que permite a los visitantes navegar por la jerarquía de páginas desde su ubicación actual. Esto suele integrarse en encabezados o pies de página.

Las opciones disponibles, como el nivel de navegación predeterminado y la capacidad de mostrar la página actual o las páginas ocultas, pueden ser definidas por el autor de la plantilla en el cuadro de diálogo [de](#design-dialog)diseño. A continuación, el editor de contenido puede elegir si se deben mostrar o no las páginas ocultas y el nivel de navegación real del componente en el cuadro de diálogo [de](#edit-dialog)edición.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de ruta de navegación es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](v1/breadcrumb-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de ruta de navegación, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_breadcrumb)componentes.

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente de ruta de navegación admite microdatos [de](https://schema.org/BreadcrumbList)esquema.org.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de ruta de navegación [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido suprimir las páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

![](/help/assets/screen_shot_2018-01-12at124250.png)

* **Nivel** de inicio de navegación: donde, en la jerarquía, el componente de ruta de exploración debe empezar a desplazarse hacia abajo hasta la página actual. Por ejemplo en We.Retail:

   * 0 empieza en `/content`
   * 1 empieza en `/content/we-retail`
   * 2 empieza en `/content/we-retail/<country>`

* **Mostrar elementos** de navegación ocultos: mostrar páginas marcadas como ocultas en la ruta de exploración (de forma predeterminada, no se mostrarán)
* **Ocultar página** actual: Suprimir la página actual en la ruta de exploración (de forma predeterminada se mostrará)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los valores predeterminados para las opciones de supresión de páginas ocultas y activas en las rutas de exploración, así como la profundidad en la jerarquía que debe mostrar.

### Ficha Principal {#main-tab}

![](/help/assets/screen_shot_2018-01-12at124437.png)

* **Nivel** de inicio de navegación: define el valor predeterminado para dónde en la jerarquía el componente de ruta de exploración debe empezar a desplazarse hacia abajo hasta la página actual cuando se agrega el componente de ruta de exploración a una página.
* **Mostrar elementos** de navegación ocultos: define el valor predeterminado de la opción **Mostrar elementos** de navegación ocultos cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

* **Ocultar página** actual: define el valor predeterminado de la opción **Ocultar página** actual cuando se agrega el componente de ruta de exploración a una página.

   * No activa ni desactiva la opción para el autor. Solo establece el valor predeterminado.

### Ficha Estilos {#styles-tab}

El componente de ruta de navegación es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
