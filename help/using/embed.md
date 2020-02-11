---
title: Incrustar componente
description: El componente Incrustar permite incrustar contenido externo en una página de contenido de AEM.
translation-type: tm+mt
source-git-commit: 65f900ad6759206a13f2bda6169900f62d968d8d

---


# Incrustar componente{#embed-component}

El componente Integrado de componentes principales permite incrustar contenido externo en una página de contenido de AEM.

## Uso {#usage}

El componente Core Component Embed permite al autor del contenido definir el contenido externo seleccionado para que se incruste en una página de contenido de AEM. Además, existe una opción para definir el código HTML de forma libre que se va a incrustar.

* Las propiedades del componente se pueden definir en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los valores predeterminados del componente al agregarlo a una página se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente incrustado es v1, que se introdujo con la versión 2.7.0 de los componentes principales en septiembre de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como servicio de nube |
|--- |--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de incrustación, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_embed)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente incrustado [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el recurso externo que se va a incrustar en la página. Primero elija qué tipo de recurso debe incrustarse:

* [URL](#url)
* [Insertable](#embeddable)
* [HTML](#html)

### URL {#url}

La incrustación más sencilla es la URL. Simplemente pegue la dirección URL del recurso que desea incrustar en el campo **URL** . El componente intentará acceder al recurso y, si uno de los procesadores puede representarlo, mostrará un mensaje de confirmación debajo del campo **URL** . Si no es así, el campo se marcará por error.

El componente Incrustar se envía con procesadores para los siguientes tipos de recursos:

* Recursos que cumplen con el estándar [oEmbed](https://oembed.com/) , incluidos Facebook Post, Instagram, SoundCloud, Twitter y YouTube
* Pinterest

Los desarrolladores pueden agregar procesadores de URL adicionales [siguiendo la documentación del desarrollador del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### Insertable {#embeddable}

Las incrustaciones permiten una mayor personalización del recurso incrustado, que se puede parametrizar e incluir información adicional. Un autor puede seleccionar elementos incrustables de confianza preconfigurados y el componente se distribuye con un componente incorporado de YouTube incorporado de forma predeterminada.

El campo **Incrustable** define el tipo de procesador que desea utilizar. En el caso de la incrustación de YouTube, puede definir:

* **ID** de vídeo: ID de vídeo único de YouTube del recurso que desea incrustar
* **Anchura** : anchura del vídeo incrustado
* **Altura** : altura del vídeo incrustado

Otros elementos incrustados ofrecerían campos similares y un desarrollador puede definirlos [siguiendo la documentación del desarrollador del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Las incrustaciones deben habilitarse en el nivel de plantilla mediante el cuadro de diálogo [](#design-dialog) Diseño para que estén disponibles para el autor de la página.

### HTML {#html}

Puede agregar HTML de forma libre a la página mediante el componente Incrustar.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Las etiquetas no seguras, como las secuencias de comandos, se filtrarán del HTML introducido y no se representarán en la página resultante.

#### Seguridad {#security}

El código HTML que puede introducir el autor se filtra por motivos de seguridad para evitar ataques de secuencias de comandos entre sitios que podrían, por ejemplo, permitir a los autores obtener derechos administrativos.

*En general,* todas las secuencias de comandos y `style` los elementos, así como todos `on*` y `style` los atributos, se eliminarán del resultado.

Sin embargo, las reglas son más complicadas porque el componente incrustado sigue el conjunto global de reglas de filtrado del marco de saneamiento HTML AntiSamy de AEM, que se puede encontrar en `/libs/cq/xssprotection/config.xml`. Un desarrollador puede superponerlo para la configuración específica del proyecto, si es necesario.

Puede encontrar información adicional sobre seguridad en la documentación para desarrolladores de [AEM para instalaciones](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) locales, así como en instalaciones de [AEM como servicio de nube.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Aunque las reglas del marco de saneamiento AntiSamy pueden configurarse superponiendo `/libs/cq/xssprotection/config.xml`, estos cambios afectan a todo el comportamiento de HTL y JSP y no sólo al componente básico incrustado.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Incrustar y los valores predeterminados establecidos al colocar el componente Incrustar.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **Deshabilitar URL** : desactiva la opción de **URL** para el autor del contenido cuando se selecciona
* **Deshabilitar incrustables** : desactiva la opción **Incrustable** para el autor del contenido cuando se selecciona, independientemente de qué procesadores se permiten incrustar.
* **Deshabilitar HTML** : desactiva la opción **HTML** para el autor del contenido cuando se selecciona.
* **Incrustaciones** permitidas: multiselección que define qué procesadores incrustables están disponibles para el autor del contenido, siempre que la opción **Incrustable** esté activa.
