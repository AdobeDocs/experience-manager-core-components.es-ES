---
title: Componente de navegación de idioma
seo-title: Componente de navegación de idioma
description: nulo
seo-description: El componente de navegación de idioma proporciona una navegación de idioma o país para un sitio, para que los visitantes puedan desplazarse a la misma página en una configuración regional distinta.
uuid: ce 736458-9 cdf -4 bc 2-b 90 f -9 c 5 a 62 fe 1 ca 0
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 8 f 232 eb 0-65 d 5-4075-8668-75 f 1366882 c 8
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8a34ecc432e489b8dc025aeda29d8eba9c788861

---


# Language Navigation Component{#language-navigation-component}

El componente de navegación de idioma proporciona una navegación de idioma o país para un sitio, para que los visitantes puedan desplazarse a la misma página en una configuración regional distinta.

## Uso {#usage}

Los sitios Web generalmente se proporcionan en varios idiomas para distintas regiones. El componente de navegación de idioma permite a un visitante ver la misma página en diferentes idiomas o configuraciones regionales. Por lo tanto, si es lector en la versión suiza suiza del sitio web, puede cambiar fácilmente a la versión en inglés de EE. UU. de la misma página. El componente Navegación de idioma gestiona la comprensión de la stuctura del idioma del sitio y encuentra la página correspondiente automáticamente.

El cuadro de diálogo [de edición](#edit-dialog) permite definir la raíz de navegación del sitio global, así como la profundidad con la que debe ir la navegación. Con el cuadro de diálogo [de diseño](#design-dialog), el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación de idioma es v 1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de navegación de idioma, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación de idioma [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de edición permite definir la raíz de navegación del sitio global, así como la profundidad con la que debe ir la navegación.

Normalmente, sólo estas configuraciones deben realizarse en el rango de plantilla de página. Sin embargo, pueden cambiarse en el nivel de página a través del cuadro de diálogo [de edición](#edit-dialog).

### Ficha Propiedades {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Raíz de navegación**
   * Aquí es donde debería comenzar la navegación langauge del sitio.
   * La estructura de idioma del sitio comienza en el siguiente nivel debajo de esta raíz.
* **Profundidad de la estructura de idiomas**
   * Este es el número de niveles del árbol de contenido debajo de **la raíz de navegación** que representan la estructura de idioma del sitio. Ejemplos:
      * `1` normalmente significa que sólo tiene la opción de idioma.
      * `2` significa que tiene una elección de idioma y país.
      * `3` normalmente significa que tiene una elección de lanzamiento, país y región.

#### Ejemplo {#example}

Supongamos que su contenido tiene un aspecto similar al siguiente:

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      +-- it
+-- wknd-events
\-- wknd-shop
```

Para el sitio We. Retail, probablemente desee colocar el componente de navegación de idioma en una plantilla de página como parte del encabezado. Una vez parte de la plantilla, puede definir la raíz **de navegación** del componente como `/content/we-retail` desde donde comienza el contenido localizado para dicho sitio. También desea definir la profundidad de la estructura **del lenguaje** como que se debe `2` a que su estructura es de dos niveles (país a continuación).

Con el valor **Raíz** de navegación, el componente Lenguaje sabe que después de `/content/we-retail` que comienza la navegación y puede generar opciones de navegación de idioma, reconozca los dos niveles siguientes en el árbol de contenido como estructura de navegación de idioma del sitio (tal como se define en el valor **Profundidad** de la estructura del lenguaje).

Independientemente de la página que esté viendo un usuario, el componente Navegación de idioma puede buscar la página correspondiente en otro idioma, conociendo la ubicación de la página actual y trabajando hacia atrás en la raíz y luego hacia la página correspondiente.

### Ficha Estilos {#styles-tab}

El componente de navegación de idioma admite el sistema [de estilos AEM](authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

Generalmente, sólo es necesario agregar y configurar el componente Navegación de langtering en las plantillas de página de un sitio. Sin embargo, si el componente Navegación de idioma debe agregarse a una página de contenido individual, el cuadro de diálogo de edición permite que un autor de contenido configure los mismos valores descritos en el cuadro de diálogo [de diseño](#design-dialog).

![](assets/screen_shot_2018-01-12at133353.png)
