---
title: Componente de fichas
description: El componente Fichas permite la creación de varias fichas para organizar el contenido de una página.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de fichas {#tabs-component}

El componente Fichas de componentes principales permite organizar el contenido en varias fichas.

## Uso {#usage}

El componente Fichas permite al autor del contenido organizar el contenido de la página en varias fichas.

El cuadro de diálogo [de](#edit-dialog) edición permite al autor del contenido definir varias fichas, así como establecer la ficha activa. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede definir qué componentes se pueden agregar a las fichas y personalizar los estilos.

>[!TIP]
>
>Se admiten componentes de ficha anidados (fichas dentro de fichas).
>
>Los componentes de ficha simples (no anidados) pueden ubicarse o seleccionarse mediante el árbol [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)contenido; sin embargo, las fichas anidadas no pueden estar.

## Vinculación profunda a un panel {#deep-linking}

Los componentes [Fichas y](accordion.md) Acordeón admiten la vinculación directa a un panel dentro del componente.

Para ello:

1. Vista de la página con el componente mediante la opción **[Vista como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** en el editor de páginas.
1. Inspect muestra el contenido de la página e identifica el ID del panel.
   * Por ejemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. El ID se convierte en el anclaje que se puede anexar a la URL mediante un hash (`#`).
   * Por ejemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Si se desplaza a la URL con el ID del panel como anclaje, el navegador se desplazará directamente al componente en cuestión y mostrará el panel especificado. Si el panel está configurado para no expandirse de forma predeterminada, se expandirá automáticamente.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Tabs es v1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Tabs y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_tabs)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Tabs [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido crear, cambiar el nombre y reorganizar fichas, así como definir la ficha activa.

### Ficha Elementos {#items-tab}

![Ficha Elementos del cuadro de diálogo de edición del componente Tabuladores](/help/assets/tabs-edit-items.png)

Utilice el botón **Añadir** para abrir el selector de componentes y elegir qué componente agregar como ficha. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:

* **Icono** : icono del tipo de componente de la ficha para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : la descripción utilizada como texto de la ficha, de forma predeterminada según el nombre del componente seleccionado para la ficha.
* **Eliminar** : toque o haga clic para eliminar la ficha del componente de ficha.
* **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de las fichas.

>[!TIP]
>
>Si se reduce la ventanilla de la página para que el cuadro de diálogo de edición se muestre a pantalla completa, se ocultará el botón **Añadir** . Los componentes se pueden añadir al componente Tabs [arrastrándolos desde el navegador de componentes y colocándolos en el componente Tabs del editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)de páginas.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Tabs](/help/assets/tabs-edit-properties.png)

* **Elemento** activo: el autor del contenido puede definir qué ficha está activa cuando se carga la página.
   * Con la opción **Predeterminado** , se seleccionará la primera ficha.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Ficha Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad del cuadro de diálogo de edición del componente Tabuladores](/help/assets/tabs-edit-accessibility.png)

En la ficha **Accesibilidad** , se pueden definir valores para las etiquetas de accesibilidad [de](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para el componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Select Panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un panel diferente para editarlo y reorganizar fácilmente el orden de las fichas.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las fichas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las fichas y se refleja en la numeración.
* El tipo de componente de la ficha se muestra primero, seguido de la descripción de la ficha en una fuente más ligera.

![Ventana emergente Seleccionar panel](/help/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, se cambia la vista del editor a esa ficha.
* Las fichas se pueden reorganizar en su lugar mediante los controladores de arrastre.

>[!NOTE]
>
>El autor no puede seleccionar las fichas cuando se encuentra en el modo de **edición** . Utilice el modo de **[Previsualización](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** o la opción **[Vista como publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interactuar con las fichas como un lector del contenido publicado.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como elementos al componente de fichas, así como definir qué estilos personalizados están disponibles para el autor del contenido.

### Allowed Components Tab {#allowed-components-tab}

La ficha Componentes **** permitidos se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente de fichas.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre al [definir la política y las propiedades de un Contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Ficha Estilos {#styles-tab}

El componente Tabs es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilos AEM.
