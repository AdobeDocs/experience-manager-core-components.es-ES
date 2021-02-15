---
title: Componente de navegación de idioma
description: El componente de navegación por idiomas proporciona navegación por idioma o país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 2%

---


# Componente de navegación de idioma{#language-navigation-component}

El componente de navegación de idioma proporciona un idioma o país de navegación para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.

## Uso {#usage}

Los sitios web se proporcionan a menudo en varios idiomas en diferentes regiones. El componente de navegación de idioma permite que un visitante vista la misma página en distintos idiomas o configuraciones regionales. Así que si eres un lector de la versión en alemán suizo del sitio web, puedes cambiar fácilmente a la versión en inglés de EE. UU. de la misma página. El componente Navegación de idioma se encarga de comprender la estructura de idioma del sitio y busca la página correspondiente automáticamente.

* Para ver un ejemplo de cómo funciona la función de localización del componente de navegación de idioma, consulte [la sección a1/>.](#example)
* Para ver un ejemplo de cómo funcionan juntas las funciones de localización de los otros componentes principales, consulte la [Localización de características de la página Componentes principales](/help/get-started/localization.md).

El [cuadro de diálogo de edición](#edit-dialog) permite la definición de la raíz de navegación del sitio global, así como la profundidad en la estructura a la que debe ir la navegación. Mediante el cuadro de diálogo [diseño](#design-dialog), el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación por idiomas es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de navegación de idioma y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_langnav).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación de idioma [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de edición permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación.

Generalmente, estas configuraciones sólo necesitan realizarse en el nivel de plantilla de página. Sin embargo, se pueden cambiar en el nivel de página mediante el cuadro de diálogo [editar](#edit-dialog).

### Ficha Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente de navegación de idioma](/help/assets/language-navigation-design.png)

* **Raíz de navegación**
   * Aquí es donde la navegación por el idioma del sitio debe inicio.
   * La estructura de idioma del sitio comienza en el siguiente nivel debajo de esta raíz.
* **Profundidad de la estructura de idiomas**
   * Se trata de cuántos niveles del árbol de contenido por debajo de la **Raíz de navegación** representan la estructura de idioma del sitio. Ejemplos:
      * `1` normalmente significa que solo se puede elegir el idioma.
      * `2` normalmente significa que usted tiene una elección de idioma y país.
      * `3` normalmente significa que tiene una opción de idioma, país y región.

#### Ejemplo {#example}

Supongamos que su contenido tiene este aspecto:

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para el WKND del sitio, es probable que desee colocar el componente Navegación de idioma en una plantilla de página como parte del encabezado. Una vez que forme parte de la plantilla, puede establecer la **Raíz de navegación** del componente en `/content/wknd`, ya que es allí donde comienza el contenido localizado para ese sitio. También desea establecer que la **Profundidad de la estructura del lenguaje** sea `2`, ya que la estructura es de dos niveles (país y luego idioma).

Con el valor **Raíz de navegación**, el componente de idioma sabe que después de `/content/wknd` que comienza la navegación y puede generar opciones de navegación de idioma reconociendo los dos niveles siguientes en el árbol de contenido como la estructura de navegación de idioma del sitio (tal como se define en el valor **Profundidad de estructura de idioma**).

Independientemente de la página que esté viendo un usuario, el componente Navegación de idioma puede encontrar la página correspondiente en otro idioma, conociendo la ubicación de la página actual y trabajando hacia atrás hasta la raíz, y luego reenviando a la página correspondiente.

### Ficha Estilos {#styles-tab}

El componente de navegación de idioma admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Editar cuadro de diálogo {#edit-dialog}

Generalmente, el componente de navegación de idioma solo necesita agregarse y configurarse en las plantillas de página de un sitio. Sin embargo, si el componente Navegación de idioma debe agregarse a una página de contenido individual, el cuadro de diálogo de edición permite que un autor de contenido configure los mismos valores como se describe en el [cuadro de diálogo de diseño](#design-dialog).

Además, puede establecer un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente de navegación de idioma](/help/assets/language-navigation-edit.png)

## Capa de datos del cliente de Adobe {#data-layer}

El componente de navegación de idioma admite la capa de datos del cliente de Adobe [](/help/developing/data-layer/overview.md).
