---
title: Componente Lista de fragmentos de contenido
description: El componente principal Lista de fragmentos de contenido permite mostrar una lista de fragmentos de contenido.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '806'
ht-degree: 100%

---

# Componente Lista de fragmentos de contenido{#content-fragment-list-component}

El componente principal Lista de fragmentos de contenido permite mostrar una lista de [fragmentos de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es).

## Uso {#usage}

El componente principal Lista de fragmentos de contenido permite incluir una lista de [fragmentos de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es) en una página basada en un modelo de fragmento de contenido. Esto puede resultar especialmente útil para crear [contenido sin encabezado](https://helpx.adobe.com/es/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) que otras aplicaciones pueden consumir fácilmente.

* La lista y sus propiedades se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los estilos se pueden aplicar al componente en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|----|---|---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](v1/content-fragment-list.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Lista de fragmentos de contenido, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cflist_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Lista de fragmentos de contenido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué fragmentos de contenido forman la lista y los elementos de esos fragmentos que se van a incluir.

### Pestaña Propiedades

La pestaña **Propiedades** define qué fragmentos de contenido se incluyen en la lista. Se basa principalmente en un modelo de fragmento de contenido seleccionado, pero hay otras opciones de filtro disponibles.

![Pestaña Propiedades del cuadro de diálogo de edición del componente Lista de fragmentos de contenido](/help/assets/content-fragment-list-properties.png)

* **Modelo**: ruta al modelo de fragmento de contenido en el que se basa la lista.
   * De forma predeterminada, todos los fragmentos de contenido del modelo definido como **Ruta de modelo** se incluyen en la lista.
* **Ruta principal**: ruta principal desde la que se debe crear la lista.
   * Los fragmentos de contenido basados en la **Ruta de modelo** seleccionada se filtrarán a los de la **Ruta principal** especificada.
      * Pulse o haga clic en el botón **Abrir cuadro de diálogo de selección** situado en la parte derecha del campo para especificar la ruta.
* **Etiquetas**: en la lista solo se incluirán los fragmentos de contenido con las etiquetas especificadas.
   * Pulse o haga clic en el botón **Abrir cuadro de diálogo de selección** situado en la parte derecha del campo para especificar las etiquetas.
   * Pulse o haga clic en la X situada junto a las etiquetas seleccionadas para eliminarlas.
* **Ordenar por**: campo del modelo de fragmento de contenido mediante el cual se ordenará la lista
   * Solo se pueden seleccionar los campos de texto (numéricos, de fecha y hora).
* **Orden**: orden que seguirá la lista con el campo **Ordenar por**
   * Ascendente o descendente
* **Máximo de elementos**: número máximo de elementos que se mostrarán en la lista
   * Si no hay ningún valor, se devolverán todos los elementos.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

>[!NOTE]
>Las opciones **Ordenar por**, **Orden** y **Máximo de elementos** se introdujeron con la versión 2.7.0 de Componentes principales.

### Pestaña Elementos

De forma predeterminada, todos los elementos del Modelo de fragmento de contenido se incluyen en la lista (a menos que estén limitados por el campo **Máximo de elementos**). La pestaña **Elementos** permite especificar los elementos específicos que se quieren incluir.

![Pestaña Elementos del cuadro de diálogo de edición del componente Lista de fragmentos de contenido](/help/assets/content-fragment-list-elements.png)

* **Elementos**: solo aparecen los elementos de los fragmentos de contenido de la lista especificada.
   * Pulse o haga clic en el botón **Añadir** para agregar un nuevo elemento.
   * Pulse o haga clic en el botón **Eliminar** para eliminar un elemento seleccionado.
   * Arrastre el control **Ordenar** para reorganizar el orden de los elementos.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Lista de fragmentos de contenido](/help/assets/content-fragment-list-styles.png)

El componente Lista de fragmentos de contenido es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Lista de fragmentos de contenido es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
