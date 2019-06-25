---
title: Componente Acordeón
seo-title: Componente Acordeón
description: nulo
seo-description: El componente Componente central Accordion permite crear una colección de paneles organizados en un acordeón en una página.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: bbd54d433cbeee5395dc8b90bc47f9b44747e25b

---


# Accordion Component{#accordion-component}

El componente Componente central Accordion permite crear una colección de paneles organizados en un acordeón en una página.

## Uso {#usage}

The Core Component Accordion component allows for the creation of a collection of components, composed as panels, and arranged in an accordion on a page, similar to the [Tabs Component](tabs.md), but allows for expanding and collapsing of the panels.

* The accordion&#39;s properties can be defined in the [configure dialog](#configure-dialog).
* The order of the panels of the accordion can be defined in the configure dialog as well as the [select panel popover](#select-planel.md).
* Defaults for the Accordion Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente Acordeón es v 1, introducida con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/accordion.html).

## Technical Details {#technical-details}

The latest technical documentation about the Accordion Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de acordeón, sus paneles y cómo se comportará y aparecerá para un visitante de la página.

### Items Tab {#items-tab}

![](assets/screen-shot-2019-06-21-08.26.38.png)

Use the **Add** button to open the component selector to choose which component to add as a panel. Una vez agregado, se agrega una entrada a la lista, que contiene las columnas siguientes:

* **Icono** : el icono del tipo de componente del panel para facilitar la identificación en la lista. Pase el ratón para ver el nombre completo del componente como información de objeto.
* **Descripción** : La descripción utilizada como texto del panel, predeterminada al nombre del componente seleccionado para el panel.
* **Eliminar** : toque o haga clic para eliminar el panel del componente Acordeón.
* **Reorganizar** : toque o haga clic y arrastre para cambiar el orden de los paneles.

### Properties Tab {#properties-tab}

![](assets/screen-shot-2019-06-21-08.26.53.png)

* **Expansión** de un solo elemento: cuando se selecciona, esta opción fuerza a cada elemento de acordeón a expandirse por vez. Al expandir un elemento, se contraerá el resto.
* **Elementos** ampliados: Esta opción define los elementos que se expanden de forma predeterminada al cargar la página.
   * When **Single item expansion** is selected, one panel must be selected. De forma predeterminada, se selecciona el primer panel.
   * When **Single item expansion** is not selected, this option is a multi-select and is optional.

## Select Panel Popover {#seelct-panel-popover}

The content author can use the **Select Panel** option on the component toolbar to change to a different panel for editing as well as to easily rearrange the order of the panels within the accordion.

![](assets/screen-shot-2019-06-21-08.49.36.png)

Once selecting the **Select Panel** option in the component toolbar, the configured accordion panels are displayed as a drop-down.

![](assets/screen-shot-2019-06-21-08.52.14.png)

* La lista se ordena por la organización asignada de los paneles y se refleja en la numeración.
* El tipo de componente del panel se muestra primero, seguido de la descripción del panel en la fuente más clara.
* Al tocar o hacer clic en una entrada del menú desplegable, se cambia la vista del editor a ese panel.
* Los paneles se pueden reorganizar en contexto empleando los controles de arrastrar.

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Accordion y los valores predeterminados establecidos al colocar el componente Acordeón.

### Properties Tab {#properties-tab-design}

![](assets/screen-shot-2019-06-21-08.58.11.png)

* **Elementos** de encabezado permitidos: esta lista desplegable de selección múltiple define los elementos HTML de encabezado del elemento de acordeón que pueden ser seleccionados por un autor.
* **Elemento** Encabezado predeterminado: Esta lista desplegable define el elemento HTML predeterminado del encabezado del elemento de acordeón.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](authoring.md#component-styling).
