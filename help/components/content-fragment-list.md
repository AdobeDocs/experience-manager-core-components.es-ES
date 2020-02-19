---
title: Componente de lista de fragmentos de contenido
description: El componente Lista de fragmentos de contenido de componentes principales permite mostrar una lista de fragmentos de contenido.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de lista de fragmentos de contenido{#content-fragment-list-component}

El componente Lista de fragmentos de contenido de componentes principales permite mostrar una lista de fragmentos [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)contenido.

## Uso {#usage}

El componente de lista de fragmentos de contenido de componentes principales permite incluir una lista de fragmentos [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) contenido en una página basada en un modelo de fragmento de contenido. Esto puede resultar especialmente útil para crear contenido [sin](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) encabezado que otras aplicaciones pueden consumir fácilmente.

* La lista y sus propiedades se pueden seleccionar en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los estilos se pueden aplicar al componente en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido es v1, que se introdujo con la versión 2.4.0 de los componentes principales en mayo de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Lista de fragmentos de contenido, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la Biblioteca [de](https://adobe.com/go/aem_cmp_library_cflist)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista de fragmentos de contenido [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué fragmentos de contenido componen la lista y los elementos de dichos fragmentos que se van a incluir.

### Ficha Propiedades

La ficha **Propiedades** define qué fragmentos de contenido se incluyen en la lista. Se basa principalmente en un modelo de fragmento de contenido seleccionado, pero hay otras opciones de filtro disponibles.

![](/help/assets/screen-shot-2019-09-25-10.32.10.png)

* **Modelo** : Ruta al modelo de fragmento de contenido en el que se basa la lista.
   * De forma predeterminada, todos los fragmentos de contenido del modelo definido como Ruta **del** modelo se incluyen en la lista.
* **Ruta** principal: ruta principal desde la que se debe crear la lista.
   * Los fragmentos de contenido basados en la ruta **del** modelo seleccionada se filtrarán a los de la ruta **** principal especificada.
      * Toque o haga clic en el botón **Abrir cuadro de diálogo** de selección en el lado derecho del campo para especificar la ruta.
* **Etiquetas** : solo se incluirán en la lista los fragmentos de contenido con las etiquetas especificadas.
   * Toque o haga clic en el botón **Abrir cuadro de diálogo** de selección en la parte derecha del campo para especificar las etiquetas.
   * Toque o haga clic en la X situada junto a las etiquetas seleccionadas para eliminarlas.
* **Ordenar por** : campo del modelo de fragmento de contenido según el cual se ordenará la lista
   * Solo se pueden seleccionar los campos de texto (incluidos los numéricos, de fecha y de hora).
* **Orden** : Cómo se ordenará la lista según el campo **Ordenar por**
   * Ascendente o descendente
* **Número máximo de elementos** : número máximo de elementos que se mostrarán en la lista
   * Ningún valor devolverá todos los elementos.

>[!NOTE]
>Las opciones **Ordenar por**, **Ordenar** y **Máx. elementos** se introdujeron con la versión 2.7.0 de los componentes principales.

### Ficha Elementos

De forma predeterminada, todos los elementos del Modelo de fragmento de contenido se incluirán en la lista (a menos que estén limitados por el campo Elementos **** máximos). La ficha **Elementos** permite especificar solo elementos específicos para incluir.

![](/help/assets/screen-shot-2019-05-08-10.47.34.png)

* **Elementos** : solo aparecerán los elementos de los fragmentos de contenido de la lista especificada.
   * Toque o haga clic en el botón **Agregar** para agregar un nuevo elemento.
   * Toque o haga clic en el botón **Eliminar** para eliminar un elemento seleccionado.
   * Arrastre el control **Orden** para reorganizar el orden de los elementos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente de lista de fragmentos de contenido.
