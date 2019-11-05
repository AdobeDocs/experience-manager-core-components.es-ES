---
title: Componente de acordeón
seo-title: Componente de acordeón
description: nulo
seo-description: El componente Acordeón de componentes principales permite la creación de una colección de paneles organizados en un acordeón en una página.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: User
content-type: reference
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: da404fff6c6e934bbe06a5c4d441d89281ed0c54

---


# Componente de acordeón{#accordion-component}

El componente Acordeón de componentes principales permite la creación de una colección de paneles organizados en un acordeón en una página.

## Uso {#usage}

El componente Acordeón de componentes principales permite la creación de una colección de componentes, compuestos como paneles y dispuestos en un acordeón en una página, similar al componente [](tabs.md)Tabs, pero permite expandir y contraer los paneles.

* Las propiedades del acordeón se pueden definir en el cuadro de diálogo [](#configure-dialog)configurar.
* El orden de los paneles del acordeón se puede definir en el cuadro de diálogo de configuración, así como en la ventana emergente [del panel de](#select-planel.md)selección.
* Los valores predeterminados del componente Acordeón al agregarlo a una página se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Acordeón es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Acordeón y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/accordion.html)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Acordeón [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de acordeón, sus paneles y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Elementos {#items-tab}

![](assets/screen-shot-2019-06-21-08.26.38.png)

Utilice el botón **Agregar** para abrir el selector de componentes y elegir qué componente agregar como panel. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:

* **Icono** : icono del tipo de componente del panel para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : descripción utilizada como texto del panel, de forma predeterminada según el nombre del componente seleccionado para el panel.
* **Eliminar** : toque o haga clic para eliminar el panel del componente de acordeón.
* **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Ficha Propiedades {#properties-tab}

![](assets/screen-shot-2019-06-21-08.26.53.png)

* **Expansión** de un solo elemento: cuando se selecciona, esta opción fuerza la expansión de un solo elemento de acordeón a la vez. Al expandir un elemento, se contraerán todos los demás.
* **Elementos** expandidos: esta opción define los elementos que se expanden de forma predeterminada cuando se carga la página.
   * Cuando se selecciona la expansión **** de un solo elemento, se debe seleccionar un panel. De forma predeterminada, se selecciona el primer panel.
   * Cuando no se selecciona la expansión **** de un solo elemento, esta opción es de selección múltiple y es opcional.

>[!TIP]
>
>Si se reduce la ventanilla de la página para que el cuadro de diálogo de edición se muestre a pantalla completa, se ocultará el botón **Agregar** . Los componentes se pueden añadir al componente Acordeón [arrastrándolos desde el navegador de componentes y colocándolos en el componente Acordeón en el editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent)de páginas.

## Ventana emergente Seleccionar panel {#seelct-panel-popover}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un panel diferente para editarlo y reorganizar fácilmente el orden de los paneles dentro del acordeón.

![](assets/screen-shot-2019-06-21-08.49.36.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, los paneles de acordeón configurados se muestran como una lista desplegable.

![](assets/screen-shot-2019-06-21-08.52.14.png)

* La lista se ordena según la disposición asignada de los paneles y se refleja en la numeración.
* El tipo de componente del panel se muestra primero, seguido de la descripción del panel con una fuente más ligera.
* Al tocar o hacer clic en una entrada de la lista desplegable, la vista del editor pasa a ese panel.
* Los paneles se pueden reorganizar en su lugar mediante los controladores de arrastre.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente de acordeón y los valores predeterminados establecidos al colocar el componente de acordeón.

### Ficha Propiedades {#properties-tab-design}

![](assets/screen-shot-2019-06-21-08.58.11.png)

* **Elementos** de encabezado permitidos: esta lista desplegable de selección múltiple define el encabezado de elemento de acordeón elementos HTML que un autor puede seleccionar.
* **Elemento** de encabezado predeterminado: esta lista desplegable define el elemento HTML de encabezado de elemento de acordeón predeterminado.

### Ficha Componentes permitidos {#allowed-components-tab}

La ficha Componentes **** permitidos se utiliza para definir qué componentes puede agregar el autor del contenido como elementos a los paneles del componente de acordeón.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre al [definir la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Ficha Estilos {#styles-tab}

El componente Acordeón es compatible con el sistema [de](authoring.md#component-styling)estilo AEM.
