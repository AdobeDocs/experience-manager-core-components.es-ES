---
title: Componente Lista de fragmentos de contenido
seo-title: Componente Lista de fragmentos de contenido
description: nulo
seo-description: El componente Lista de fragmentos de contenido principal permite mostrar una lista de fragmentos de contenido.
contentOwner: bohnert
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente Lista de fragmentos de contenido{#content-fragment-list-component}

El componente Lista de fragmentos de contenido principal permite mostrar una lista de [fragmentos de contenido](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

## Uso {#usage}

El componente Lista de fragmentos de contenido de componente principal permite incluir una lista de fragmentos [de contenido](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) en una página basada en un modelo de fragmento de contenido. Esto puede resultar especialmente útil para crear [contenido](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) headless que pueda consumir fácilmente otras aplicaciones.

* La lista y sus propiedades se pueden seleccionar en el cuadro de diálogo [de configuración](#configure-dialog).
* Se pueden aplicar estilos al componente en el cuadro de diálogo [de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido es v 1, que se introdujo con la versión 2.4.0 de los componentes principales en mayo de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Lista de fragmentos de contenido, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista de fragmentos de contenido [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir qué fragmentos de contenido comprenden la lista y los elementos de esos fragmentos que se van a incluir.

### Ficha Propiedades

La ficha **Propiedades** define qué fragmentos de contenido se incluyen en la lista. Se basa principalmente en un modelo de fragmento de contenido seleccionado, pero hay otras opciones de filtro disponibles.

![](assets/screen-shot-2019-05-08-10.47.19.png)

* **Modelo** - Ruta al modelo de fragmentos de contenido en el que se basa la lista.
   * De forma predeterminada, se incluyen en la lista todos los fragmentos de contenido del modelo definido como **Ruta** modelo.
* **Ruta principal** - Ruta principal desde la cual se debe crear la lista.
   * Los fragmentos de contenido basados en la ruta **del modelo** seleccionada se filtrarán a los de la ruta **principal especificada**.
   * Toque o haga clic en el botón **Abrir cuadro de diálogo** de selección en la parte derecha del campo para especificar la ruta.
* **Etiquetas** : Solo se incluirán en la lista los fragmentos de contenido con las etiquetas especificadas.
   * Toque o haga clic en el botón **Abrir cuadro de diálogo** de selección en la parte derecha del campo para especificar las etiquetas.
   * Toque o haga clic en la X junto a las etiquetas seleccionadas para eliminarlas.


### Ficha Elementos

De forma predeterminada, todos los elementos del Modelo de fragmento de contenido se incluirán en la lista. **Los elementos** le permiten especificar solo elementos específicos para incluir.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **Elementos** : Solo aparecerán los elementos de los fragmentos de contenido de la lista especificada.
   * Toque o haga clic en el botón **Agregar** para agregar un nuevo elemento
   * Toque o haga clic en **el** botón Eliminar para eliminar un elemento seleccionado
   * Arrastre el control **de pedido** para cambiar el orden de los elementos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los estilos aplicados al componente Lista de fragmentos de contenido.