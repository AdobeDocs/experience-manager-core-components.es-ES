---
title: Componente Acordeón
description: El componente Acordeón de componentes principales permite crear una colección de paneles organizados en un acordeón de una página.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 1%

---


# Componente de acordeón{#accordion-component}

El componente Acordeón de componentes principales permite crear una colección de paneles organizados en un acordeón de una página.

## Uso {#usage}

El componente Acordeón de componente principal permite la creación de una colección de componentes, compuestos como paneles y organizados en un acordeón de una página, similar al [Componente de fichas](tabs.md), pero permite expandir y contraer los paneles.

* Las propiedades del acordeón se pueden definir en el [cuadro de diálogo de configuración](#configure-dialog).
* El orden de los paneles del acordeón se puede definir en el cuadro de diálogo de configuración, así como en el [panel de selección pover](#select-panel-popover).
* Los valores predeterminados del componente Acordeón al agregarlo a una página se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Vinculación profunda a un panel {#deep-linking}

El acordeón y los [componentes de pestañas](tabs.md) admiten la vinculación directa a un panel dentro del componente.

Para ello:

1. Vea la página con el componente utilizando la opción **[Ver como aparece publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** en el editor de páginas.
1. Inspect muestra el contenido de la página e identifica el ID del panel.
   * Por ejemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. El ID se convierte en el anclaje que puede anexar a la URL mediante un hash (`#`).
   * Por ejemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Si se desplaza a la dirección URL con el ID de panel como anclaje, el navegador se desplazará directamente al componente en cuestión y mostrará el panel especificado. Si el panel está configurado para no expandirse de forma predeterminada, se expandirá automáticamente.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Acordeón es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente Acordeón, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_accordion).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Acordeón [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de acordeón, sus paneles y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Elementos {#items-tab}

![Ficha Elementos del cuadro de diálogo de edición del componente Acordeón](/help/assets/accordion-edit-items.png)

Utilice el botón **Add** para abrir el selector de componentes y elegir qué componente añadir como panel. Una vez añadida, se añade una entrada a la lista, que contiene las columnas siguientes:

* **Icono** : el icono del tipo de componente del panel para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : la descripción utilizada como texto del panel, de forma predeterminada, con el nombre del componente seleccionado para el panel.
* **Eliminar** : toque o haga clic para eliminar el panel del componente de acordeón.
* **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de los paneles.

>[!TIP]
>
>Si la ventanilla móvil de la página se reduce para que el cuadro de diálogo de edición pase a estar en pantalla completa, el botón **Add** se ocultará. Los componentes se pueden añadir al componente Acordeón arrastrando [desde el navegador de componentes y soltando en el componente Acordeón en el editor de páginas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Acordeón](/help/assets/accordion-edit-properties.png)

* **Expansión de un solo elemento** : cuando se selecciona, esta opción fuerza a que un solo elemento de acordeón se expanda a la vez. Expandir un elemento colapsará todos los demás.
* **Elementos ampliados** : esta opción define los elementos que se expanden de forma predeterminada cuando se carga la página.
   * Cuando se selecciona **Expansión de un solo elemento**, se debe seleccionar un panel. De forma predeterminada, el primer panel está seleccionado.
   * Cuando **Expansión de un solo elemento** no está seleccionada, esta opción es de selección múltiple y opcional.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Seleccionar el panel emergente {#select-panel-popover}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un panel diferente para editarlo, así como para reorganizar fácilmente el orden de los paneles dentro del acordeón.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, los paneles de acordeón configurados se muestran como una lista desplegable.

![Seleccionar la ventana emergente del panel](/help/assets/select-panel-popover.png)

* La lista se ordena según la disposición asignada de los paneles y se refleja en la numeración.
* El tipo de componente del panel se muestra primero, seguido de la descripción del panel en una fuente más ligera.
* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a ese panel.
* Los paneles se pueden reorganizar en su lugar mediante los controles de arrastre.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor de contenido que utiliza el componente de acordeón y los valores predeterminados establecidos al colocar el componente de acordeón.

### Ficha Propiedades {#properties-tab-design}

![Ficha Propiedades del cuadro de diálogo Diseño](/help/assets/accordion-design-properties.png)

* **Elementos de encabezado permitidos** : esta lista desplegable de selección múltiple define el encabezado de elemento de acordeón de los elementos HTML que un autor puede seleccionar.
* **Elemento de encabezado predeterminado** : esta lista desplegable define el elemento de acordeón predeterminado encabezado por elemento HTML.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes el autor de contenido puede añadir como elementos a los paneles del componente de acordeón.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre cuando [define la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Pestaña Estilos {#styles-tab}

El componente Acordeón es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Acordeón es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
