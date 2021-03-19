---
title: Componente de lista de fragmentos de contenido
description: El componente Lista de fragmentos de contenido de componentes principales permite mostrar una lista de fragmentos de contenido.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 5%

---


# Componente de lista de fragmentos de contenido{#content-fragment-list-component}

El componente Lista de fragmentos de contenido de componentes principales permite mostrar una lista de [fragmentos de contenido](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

## Uso {#usage}

El componente de lista de fragmentos de contenido del componente principal permite incluir una lista de [fragmentos de contenido](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) en una página basada en un modelo de fragmento de contenido. Esto puede resultar especialmente útil para crear [contenido sin encabezado](https://helpx.adobe.com/es/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) que otras aplicaciones pueden consumir fácilmente.

* La lista y sus propiedades se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los estilos se pueden aplicar al componente en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de fragmento de contenido es v1, que se introdujo con la versión 2.4.0 de los componentes principales en mayo de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente de lista de fragmentos de contenido, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cflist).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de lista de fragmentos de contenido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo configurar permite al autor del contenido definir qué fragmentos de contenido forman la lista y los elementos de esos fragmentos que se van a incluir.

### Ficha Propiedades

La pestaña **Properties** define qué fragmentos de contenido se incluyen en la lista. Se basa principalmente en un modelo de fragmento de contenido seleccionado, pero hay otras opciones de filtro disponibles.

![Ficha Propiedades del cuadro de diálogo de edición del componente Lista de fragmentos de contenido](/help/assets/content-fragment-list-properties.png)

* **Modelo** : ruta al modelo de fragmento de contenido en el que se basa la lista.
   * De forma predeterminada, todos los fragmentos de contenido del modelo definido como **Model Path** se incluyen en la lista.
* **Ruta principal** : ruta principal desde la que se debe crear la lista.
   * Los fragmentos de contenido basados en la **Ruta del modelo** seleccionada se filtrarán a los de la **Ruta principal** especificada.
      * Toque o haga clic en el botón **Abrir cuadro de diálogo de selección** situado en la parte derecha del campo para especificar la ruta.
* **Etiquetas** : en la lista solo se incluirán los fragmentos de contenido con las etiquetas especificadas.
   * Toque o haga clic en el botón **Abrir cuadro de diálogo de selección** situado en la parte derecha del campo para especificar las etiquetas.
   * Toque o haga clic en la X situada junto a las etiquetas seleccionadas para eliminarlas.
* **Ordenar por** : Campo del modelo de fragmento de contenido mediante el cual se ordenará la lista
   * Solo se pueden seleccionar los campos de texto (numéricos, de fecha y hora).
* **Orden** : orden en que se ordenará la lista por campo  **Ordenar** por campo
   * Ascendente o descendente
* **Máximo de elementos** : número máximo de elementos que se mostrarán en la lista
   * Ningún valor devolverá todos los elementos.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

>[!NOTE]
>Las opciones **Ordenar por**, **Ordenar por** y **Máx. elementos** se introdujeron con la versión 2.7.0 de los componentes principales.

### Ficha Elementos

De forma predeterminada, todos los elementos del Modelo de fragmento de contenido se incluyen en la lista (a menos que estén limitados por el campo **Max Items** ). La pestaña **Elements** permite especificar solo elementos específicos para incluir.

![Ficha Elementos del cuadro de diálogo de edición del componente Lista de fragmentos de contenido](/help/assets/content-fragment-list-elements.png)

* **Elementos** : solo aparecen los elementos de los fragmentos de contenido de la lista especificada.
   * Toque o haga clic en el botón **Add** para añadir un nuevo elemento.
   * Toque o haga clic en el botón **Delete** para eliminar un elemento seleccionado.
   * Arrastre el control **Order** para reorganizar el orden de los elementos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente de lista de fragmentos de contenido.
