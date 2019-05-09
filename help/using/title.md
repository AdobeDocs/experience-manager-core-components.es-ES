---
title: Componente de título
seo-title: Componente de título
description: nulo
seo-description: El componente Título de componente principal es un componente de encabezado de sección que incluye edición in-situ.
uuid: cf 190861-e 5 cd -42 b 8-9193-842 b 8 df 8 c 5 c 6 c 6
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 243 efc 75-fcf 9-427 d -9303-9642 b 0602991
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de título{#title-component}

El componente Título de componente principal es un componente de encabezado de sección que incluye edición in-situ.

## Uso {#usage}

El componente Título está diseñado para utilizarse como título o encabezado de una sección de contenido. El autor de la plantilla puede definir los niveles de encabezados disponibles en el cuadro de diálogo [de diseño](#design-dialog). El editor de contenido puede seleccionar los niveles de encabezados disponibles en el cuadro de diálogo [de edición](#edit-dialog). Para mayor comodidad, también hay disponible una edición in-situ sencilla del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Título es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](title-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-36.png)

### Biblioteca de componentes

Para experimentar el componente Título, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título y seleccionar el nivel de encabezado.

* **Título** : Si está vacío, se utilizará el título de página
* **Tipo/Tamaño** : define el nivel de encabezado del título
* **Vínculo** : define el contenido al que se vinculará el título. Puede ser una ruta a una página de contenido, una URL externa o un anclaje de página.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>La capacidad para definir un vínculo para el título se introdujo con la versión 2.2.0 de los componentes principales.

El editor in-situ también se puede utilizar para editar el texto del componente de título.

![](assets/chlimage_1-37.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

### Ficha Tamaños {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **Tipos permitidos/Tamaños para autores** : habilite o deshabilite los tipos de encabezados que estarán disponibles para los autores de contenido cuando utilicen el componente Título.
* **Tipo o tamaño predeterminado**: defina el tipo de encabezado que se asignará automáticamente cuando un autor de contenido agregue el componente Título a una página.
* **Deshabilitar vínculo**: deshabilite la compatibilidad con vínculos en el componente Título para impedir que los autores de contenido puedan vincular los títulos.

>[!CAUTION]
>
>La capacidad para definir un vínculo para el título se introdujo con la versión 2.2.0 de los componentes principales.

### Ficha Estilos {#styles-tab}

El componente Título admite el sistema [de estilos AEM](authoring.md#component-styling).