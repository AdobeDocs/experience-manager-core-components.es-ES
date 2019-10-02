---
title: Incrustar componente
seo-title: Incrustar componente
description: El componente Incrustar permite incrustar contenido externo en una página de contenido de AEM.
seo-description: El componente Incrustar permite incrustar contenido externo en una página de contenido de AEM.
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 97f1461b57079806f9f96d325d9b763538e32127

---


# Incrustar componente{#embed-component}

El componente Integrado de componentes principales permite incrustar contenido externo en una página de contenido de AEM.

## Uso {#usage}

El componente Core Component Embed permite al autor del contenido definir el contenido externo seleccionado para que se incruste en una página de contenido de AEM. Además, existe una opción para definir el HTML de forma libre que se va a incrustar.

* Las propiedades del componente se pueden definir en el cuadro de diálogo [](#configure-dialog)Configurar.
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

Developers can add additional URL processors by [following the developer documentation of the Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Insertable {#embeddable}

Embeddables allow for more customization of the embedded resource, which can be parameterized and include additional information. An author is able to select from pre-configured trusted embeddables and the component ships with a Youtube embeddable out-of-the-box.

The Embeddable field defines the type of processor you want to use. **** In the case of the YouTube embeddable you can then define:

* **Video ID - The unique video ID from YouTube of the resource you want to embed**
* **Width - The width of the embedded video**
* **Height - The height of the embedded video**

Other embeddables would offer similar fields and can be defined by a developer by following the developer documentation of the Embed Component.[](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embeddables must be enabled at the template level via the [Design Dialog](#design-dialog) to be available to the page author.

### HTML {#html}

You can add free-form HTML to your page using the Embed Component.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Las etiquetas no seguras, como las secuencias de comandos, se filtrarán del HTML introducido y no se representarán en la página resultante.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Embed Component and the defaults set when placing the Embed Component.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Deshabilitar URL** : desactiva la opción de **URL** para el autor del contenido cuando se selecciona
* **Deshabilitar incrustables** : desactiva la opción **Incrustable** para el autor del contenido cuando se selecciona, independientemente de qué procesadores se permiten incrustar.
* **Disable HTML - Disables the HTML option for the content author when selected.******
* **Allowed Embeddables** - Multislect that defines which embeddable processors are available to the content author, provided that the **Embeddable** option is active.
