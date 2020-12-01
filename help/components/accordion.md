---
title: Componente de acordeón
description: El componente Acordeón de componentes principales permite la creación de una colección de paneles organizados en un acordeón en una página.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 1%

---


# Componente de acordeón{#accordion-component}

El componente Acordeón de componentes principales permite la creación de una colección de paneles organizados en un acordeón en una página.

## Uso {#usage}

El componente Acordeón de componentes principales permite la creación de una colección de componentes, compuestos como paneles y dispuestos en un acordeón en una página, similar al [Componente de fichas](tabs.md), pero permite expandir y contraer los paneles.

* Las propiedades del acordeón se pueden definir en el cuadro de diálogo [configurar](#configure-dialog).
* El orden de los paneles del acordeón se puede definir en el cuadro de diálogo de configuración, así como en la ventana emergente [seleccionar panel](#select-panel-popover).
* Los valores predeterminados del componente Acordeón al agregarlo a una página se pueden definir en el cuadro de diálogo [diseño](#design-dialog).

## Vinculación profunda a un panel {#deep-linking}

El componente Acordeón y [Componentes de fichas](tabs.md) admiten la vinculación directa a un panel dentro del componente.

Para ello:

1. Vista la página con el componente mediante la opción **[Vista tal como se publica](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** en el editor de páginas.
1. Inspect muestra el contenido de la página e identifica el ID del panel.
   * Por ejemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. El ID se convierte en el anclaje que puede anexar a la dirección URL mediante un hash (`#`).
   * Por ejemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Si se desplaza a la URL con el ID del panel como anclaje, el navegador se desplazará directamente al componente en cuestión y mostrará el panel especificado. Si el panel está configurado para no expandirse de forma predeterminada, se expandirá automáticamente.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Acordeón es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Acordeón y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_accordion).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de acordeón [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de acordeón, sus paneles y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Elementos {#items-tab}

![Ficha Elementos del cuadro de diálogo de edición del componente Acordeón](/help/assets/accordion-edit-items.png)

Utilice el botón **Añadir** para abrir el selector de componentes y elegir qué componente agregar como panel. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:

* **Icono** : icono del tipo de componente del panel para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : descripción utilizada como texto del panel, de forma predeterminada según el nombre del componente seleccionado para el panel.
* **Eliminar** : toque o haga clic para eliminar el panel del componente de acordeón.
* **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de los paneles.

>[!TIP]
>
>Si se reduce la ventanilla de la página para que el cuadro de diálogo de edición se muestre a pantalla completa, se ocultará el botón **Añadir**. Los componentes se pueden agregar al componente Acordeón [arrastrándolos desde el navegador de componentes y colocándolos en el componente Acordeón en el editor de páginas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Acordeón](/help/assets/accordion-edit-properties.png)

* **Expansión**  de un solo elemento: cuando se selecciona, esta opción fuerza la expansión de un solo elemento de acordeón a la vez. Al expandir un elemento, se contraerán todos los demás.
* **Elementos**  expandidos: esta opción define los elementos que se expanden de forma predeterminada cuando se carga la página.
   * Cuando **Se selecciona la expansión de un solo elemento**, se debe seleccionar un panel. De forma predeterminada, se selecciona el primer panel.
   * Cuando **expansión de un solo elemento** no está seleccionada, esta opción es una selección múltiple y es opcional.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Seleccionar ventana emergente de panel {#select-panel-popover}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas del componente para cambiar a otro panel para editarlo y reorganizar fácilmente el orden de los paneles dentro del acordeón.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, los paneles de acordeón configurados se muestran como una lista desplegable.

![Ventana emergente Seleccionar panel](/help/assets/select-panel-popover.png)

* La lista se ordena por la disposición asignada de los paneles y se refleja en la numeración.
* El tipo de componente del panel se muestra primero, seguido de la descripción del panel con una fuente más ligera.
* Al tocar o hacer clic en una entrada de la lista desplegable, la vista del editor pasa a ese panel.
* Los paneles se pueden reorganizar en su lugar mediante los controladores de arrastre.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente de acordeón y los valores predeterminados establecidos al colocar el componente de acordeón.

### Ficha Propiedades {#properties-tab-design}

![Ficha Propiedades del cuadro de diálogo Diseño](/help/assets/accordion-design-properties.png)

* **Elementos**  de encabezado permitidos: esta lista desplegable de selección múltiple define el encabezado de elemento de acordeón elementos HTML que un autor puede seleccionar.
* **Elemento**  de encabezado predeterminado: esta lista desplegable define el elemento HTML de encabezado de elemento de acordeón predeterminado.

### Ficha Componentes permitidos {#allowed-components-tab}

La ficha **Componentes permitidos** se utiliza para definir qué componentes puede agregar el autor del contenido como elementos a los paneles del componente de acordeón.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre cuando [define la política y las propiedades de un Contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Ficha Estilos {#styles-tab}

El componente Acordeón admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).
