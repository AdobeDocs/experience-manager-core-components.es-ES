---
title: Componente de navegación de idioma
description: El componente de navegación por idiomas proporciona navegación por idioma o país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 2%

---


# Language Navigation Component{#language-navigation-component}

El componente de navegación de idioma proporciona un idioma o país de navegación para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.

## Uso {#usage}

Los sitios web se proporcionan a menudo en varios idiomas en diferentes regiones. El componente de navegación de idioma permite que un visitante vista la misma página en distintos idiomas o configuraciones regionales. Así que si eres un lector de la versión en alemán suizo del sitio web, puedes cambiar fácilmente a la versión en inglés de EE. UU. de la misma página. El componente Navegación de idioma se encarga de comprender la estructura de idioma del sitio y busca la página correspondiente automáticamente.

* Para ver un ejemplo de cómo funciona la función de localización del componente de navegación de idioma, consulte [la sección siguiente](#example).
* Para ver un ejemplo de cómo funcionan conjuntamente las funciones de localización de los demás componentes principales, consulte la página [Características de la](/help/get-started/localization.md)Localización de la páginaComponentes principales.

El cuadro de diálogo [de](#edit-dialog) edición permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación por idiomas es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de navegación de idioma, así como ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_langnav)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación de idiomas [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de edición permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación.

Generalmente, estas configuraciones sólo necesitan realizarse en el nivel de plantilla de página. Sin embargo, se pueden cambiar en el nivel de página a través del cuadro de diálogo [de](#edit-dialog)edición.

### Ficha Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente de navegación de idioma](/help/assets/language-navigation-design.png)

* **Raíz de navegación**
   * Aquí es donde la navegación por el idioma del sitio debe inicio.
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

Para el WKND del sitio, es probable que desee colocar el componente Navegación de idioma en una plantilla de página como parte del encabezado. Una vez que forma parte de la plantilla, puede establecer la raíz **de** navegación del componente en `/content/wknd` , ya que es ahí donde comienza el contenido localizado para ese sitio. También desea establecer la profundidad **de la estructura de** idioma `2` , ya que la estructura tiene dos niveles (país y idioma).

Con el valor Raíz **de** navegación, el componente Idioma sabe que después de `/content/wknd` eso comienza la navegación y puede generar opciones de navegación por el idioma reconociendo los dos niveles siguientes en el árbol de contenido como la estructura de navegación por el idioma del sitio (tal como se define en el valor Profundidad **de la estructura del** lenguaje).

Independientemente de la página que esté viendo un usuario, el componente Navegación de idioma puede encontrar la página correspondiente en otro idioma, conociendo la ubicación de la página actual y trabajando hacia atrás hasta la raíz, y luego reenviando a la página correspondiente.

### Ficha Estilos {#styles-tab}

El componente de navegación de idioma admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.

## Edit Dialog {#edit-dialog}

Generalmente, el componente de navegación de idioma solo necesita agregarse y configurarse en las plantillas de página de un sitio. Sin embargo, si el componente Navegación de idioma debe agregarse a una página de contenido individual, el cuadro de diálogo de edición permite al autor del contenido configurar los mismos valores que se describen en el cuadro de diálogo [de](#design-dialog)diseño.

Además, puede configurar un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la capa [](/help/developing/data-layer/overview.md)de datos.

* Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente de navegación de idioma](/help/assets/language-navigation-edit.png)
