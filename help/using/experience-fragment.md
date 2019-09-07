---
title: Componente de fragmento de experiencias
seo-title: Componente de fragmento de experiencias
description: El componente Fragmento de experiencia permite al autor de contenido agregar una variación de fragmento de experiencia a una página.
seo-description: El componente Fragmento de experiencia permite al autor de contenido agregar una variación de fragmento de experiencia a una página.
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 12d18a31c5507f5bbc713383f4d194d8ab8c4d58

---


# Componente de fragmento de experiencias{#experience-fragment-component}

El componente Fragmento de experiencia de componente principal permite al autor de contenido colocar una variación de fragmento de experiencia en una página mientras se admite una estructura localizada del sitio.

## Uso {#usage}

El componente Fragmento de experiencia de componente principal permite que el autor de contenido seleccione entre las varaciones de fragmentos de experiencias existentes y coloque uno en la página de contenido. El componente Fragmento de experiencia también admite una estructura localizada del sitio.

* Las propiedades de los componentes se pueden definir en el cuadro de diálogo [de configuración](#configure-dialog).
* Los valores predeterminados para el componente al agregarlos a una página se pueden definir en el cuadro de diálogo [de diseño](#design-dialog).

## Compatibilidad con estructura de sitio localizada {#localized-site-structure}

El componente Fragmento de experiencia es adaptable a estructuras localizadas del sitio y procesa el fragmento de experiencia adecuado en función de la localización de la página. Para ello, el fragmento de experiencia debe cumplir las condiciones siguientes.

* El componente Fragmento de experiencia se agrega a una plantilla.
* Esa plantilla se utiliza para crear una nueva página de contenido que forma parte de una estructura localizada a continuación `/content/<site>`.
* El fragmento de experiencia al que se hace referencia en una página de contenido forma parte de una estructura de fragmento de experiencia localizada que sigue `/content/experience-fragments` los mismos patrones que el sitio siguiente `/content/<site>` , incluido el uso de los mismos nombres de componente.

En este caso, el fragmento con la misma localización (idioma, modelo o Live Copy), se procesará como parte de la plantilla.

Este comportamiento está limitado a Componentes de fragmento de experiencia añadidos a plantillas. Los componentes de fragmento de experiencia añadidos a páginas de contenido individuales representarán las representaciones exactas de fragmentos de experiencia configuradas dentro del componente.

### Ejemplo {#example}

Supongamos que su contenido tiene un aspecto similar al siguiente:

```
/content
+-- experience-fragments
   \-- we-retail
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Observe que la estructura a continuación `/content/experience-fragments/we-retail` refleja la estructura de `/content/we-retail`.

En este caso, si el componente Fragmento de experiencia `/content/experience-fragments/we-retail/us/en/footerTextXf` se coloca en una plantilla, las páginas localizadas creadas en función de esa plantilla representarán automáticamente el fragmento de experiencia localizado que corresponde a la página de contenido localizado.

Así pues, si navega a una página de contenido dentro `/content/we-retail/ch/de` de la que utiliza la misma plantilla, `/content/experience-fragments/we-retail/ch/de/footerTextXf` se procesará en lugar `/content/experience-fragments/we-retail/us/en/footerTextXf`de.

### Reserva {#fallback}

El componente Fragmento de experiencia intentará encontrar un componente localizado correspondiente en el orden siguiente.

1. Ffirst intenta encontrar una raíz de idioma.
1. Si no se encuentra, intenta encontrar un modelo.
1. Si no se encuentra, intenta encontrar una Live Copy.
1. Si no se encuentra, el fragmento de experiencia se configurará de forma predeterminada en el componente.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de experiencia es v 1, que se introdujo con la versión 2.6.0 de los componentes principales en agosto de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Fragmento de experiencias, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/experience-fragment.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de experiencia [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/experience-fragment/v1/experience-fragment).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido seleccionar la variación de fragmento de experiencia que debe procesarse en la página.

![](assets/screen-shot-2019-08-23-10.49.21.png)

Utilice el botón **Abrir cuadro de diálogo** de selección para abrir el selector de componentes para seleccionar qué variación de componente de fragmento de experiencia agregar a la página de contenido.

Si agrega el componente Fragmento de experiencia a una plantilla, tenga en cuenta que se localizará automáticamente siempre que los fragmentos de experiencias estén localizados, de modo que los elementos procesados en la página pueden variar del componente seleccionado explícitamente. [Consulte el ejemplo anterior](#example) para obtener más información.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Fragmento de experiencia y los valores predeterminados establecidos al colocar el componente Fragmento de experiencia.

![](assets/screen-shot-2019-08-23-10.48.36.png)

El componente Fragmento de experiencia admite el sistema [de estilos AEM](authoring.md#component-styling).
