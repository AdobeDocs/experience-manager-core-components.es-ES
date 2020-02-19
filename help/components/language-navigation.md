---
title: Componente de navegación de idioma
description: El componente de navegación por idiomas proporciona navegación por el idioma o país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Language Navigation Component{#language-navigation-component}

El componente de navegación de idioma proporciona navegación por el idioma o país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.

## Uso {#usage}

Los sitios web se proporcionan a menudo en varios idiomas en diferentes regiones. El componente de navegación por idiomas permite que un visitante vea la misma página en distintos idiomas o configuraciones regionales. Así que si eres un lector de la versión en alemán suizo del sitio web, puedes cambiar fácilmente a la versión en inglés de EE. UU. de la misma página. El componente Navegación de idioma se encarga de comprender la estructura de idioma del sitio y busca la página correspondiente automáticamente.

* Para ver un ejemplo de cómo funciona la función de localización del componente de navegación de idioma, consulte [la sección siguiente](#example).
* Para ver un ejemplo de cómo funcionan conjuntamente las funciones de localización de los otros componentes principales, consulte la página [Características de](/help/get-started/localization.md)localización de la páginaComponentes principales.

El cuadro de diálogo [de](#edit-dialog) edición permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación por idiomas es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de navegación de idioma, así como ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_langnav)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación de idiomas [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de edición permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación.

Generalmente, estas configuraciones sólo necesitan realizarse en el nivel de plantilla de página. Sin embargo, se pueden cambiar en el nivel de página a través del cuadro de diálogo [de](#edit-dialog)edición.

### Ficha Propiedades {#properties-tab}

![](/help/assets/screen_shot_2018-01-12at133642.png)

* **Raíz de navegación**
   * Aquí es donde debería comenzar la navegación por el idioma del sitio.
   * La estructura de idioma del sitio comienza en el siguiente nivel debajo de esta raíz.
* **Profundidad de la estructura de idiomas**
   * Son tantos los niveles del árbol de contenido debajo de la raíz **de** navegación que representan la estructura de idioma del sitio. Ejemplos:
      * `1` normalmente significa que solo se puede elegir el idioma.
      * `2` normalmente significa que usted tiene una elección de idioma y país.
      * `3` normalmente significa que tiene una opción de idioma, país y región.

#### Ejemplo {#example}

Supongamos que su contenido tiene este aspecto:

```
/content
+-- we-retail
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

Para el sitio We.Retail, probablemente desee colocar el componente Navegación de idioma en una plantilla de página como parte del encabezado. Una vez que forma parte de la plantilla, puede establecer la raíz **de** navegación del componente en `/content/we-retail` , ya que es allí donde comienza el contenido localizado para ese sitio. También desea establecer la profundidad **de la estructura de** idioma `2` , ya que la estructura tiene dos niveles (país y idioma).

Con el valor Raíz **de** navegación, el componente Idioma sabe que después de `/content/we-retail` eso comienza la navegación y puede generar opciones de navegación por el idioma reconociendo los dos niveles siguientes en el árbol de contenido como la estructura de navegación por el idioma del sitio (tal como se define en el valor Profundidad **de la estructura del** lenguaje).

Independientemente de la página que esté viendo un usuario, el componente Navegación de idioma puede encontrar la página correspondiente en otro idioma, conociendo la ubicación de la página actual y trabajando hacia atrás hasta la raíz, y luego reenviando a la página correspondiente.

### Ficha Estilos {#styles-tab}

El componente de navegación de idioma admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.

## Edit Dialog {#edit-dialog}

Generalmente, el componente de navegación de idioma solo necesita agregarse y configurarse en las plantillas de página de un sitio. Sin embargo, si el componente Navegación de idioma debe agregarse a una página de contenido individual, el cuadro de diálogo de edición permite al autor del contenido configurar los mismos valores que se describen en el cuadro de diálogo [de](#design-dialog)diseño.

![](/help/assets/screen_shot_2018-01-12at133353.png)
