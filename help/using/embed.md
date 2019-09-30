---
title: Incrustar componente
seo-title: Incrustar componente
description: El componente Incrustar permite incrustar contenido externo en una página de contenido de AEM.
seo-description: El componente Incrustar permite incrustar contenido externo en una página de contenido de AEM.
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 6882a0d8247328c403dc11a25ed9d079aefede69

---


# Incrustar componente{#embed-component}

El componente Integrado de componentes principales permite incrustar contenido externo en una página de contenido de AEM.

## Uso {#usage}

El componente Core Component Embed permite al autor del contenido definir el contenido externo seleccionado para que se incruste en una página de contenido de AEM. Además, existe una opción para definir el HTML de forma libre que se va a incrustar.

* Las propiedades de los componentes se pueden definir en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los valores predeterminados del componente al agregarlo a una página se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente incrustado es v1, que se introdujo con la versión 2.7.0 de los componentes principales en septiembre de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de incrustación, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/embed.html)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente incrustado [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el recurso externo que se va a incrustar en la página. Primero elija qué tipo de recurso debe incrustarse: **URL**, **incrustable** o **HTML**.

### URL {#url}

La incrustación más sencilla es la URL. Simplemente pegue la dirección URL del recurso que desea incrustar en el campo **URL** . El componente intentará acceder al recurso y, si uno de los procesadores puede representarlo, mostrará un mensaje de confirmación debajo del campo **URL** . Si no es así, el campo se marcará por error.

El componente Incrustar se envía con procesadores para los siguientes tipos de recursos:

* Recursos que cumplen con el estándar [oEmbed](https://oembed.com/) , incluidos Facebook Post, Instagram, SoundCloud, Twitter y YouTube
* Pinterest

Los desarrolladores pueden agregar procesadores de URL adicionales [siguiendo la documentación del desarrollador del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Incrustación {#embeddable}

Las incrustaciones permiten una mayor personalización del recurso incrustado, que se puede parametrizar e incluir información adicional. Un autor puede seleccionar elementos incrustables de confianza preconfigurados y el componente se distribuye con un procesador de YouTube incorporado.

El campo **Incrustable** define el tipo de procesador que desea utilizar. En el caso del procesador de YouTube, puede definir:

* **ID** de vídeo: ID de vídeo único de YouTube del recurso que desea incrustar
* **Anchura** : anchura del vídeo incrustado
* **Altura** : altura del vídeo incrustado

Otros procesadores ofrecerían campos similares y pueden ser definidos por un desarrollador [siguiendo la documentación del desarrollador del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Los procesadores integrados deben habilitarse en el nivel de plantilla mediante el cuadro de diálogo [](#design-dialog) Diseño para que el autor de la página pueda acceder a ellos.

### HTML {#html}

Puede agregar HTML de forma libre a la página mediante el componente Incrustar.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Las etiquetas no seguras, como las secuencias de comandos, se filtrarán del HTML introducido y no se representarán en la página resultante.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Incrustar y los valores predeterminados establecidos al colocar el componente Incrustar.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Deshabilitar URL** : desactiva la opción de **URL** para el autor del contenido cuando se selecciona
* **Deshabilitar incrustables** : desactiva la opción **Incrustable** para el autor del contenido cuando se selecciona, independientemente de qué procesadores se permiten incrustar.
* **Deshabilitar HTML** : desactiva la opción **HTML** para el autor del contenido cuando se selecciona.
* **Incrustaciones** permitidas: multiselección que define qué procesadores incrustables están disponibles para el autor del contenido, siempre que la opción **Incrustable** esté activa.
