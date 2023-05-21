---
title: Componente Pestañas
description: El componente Pestañas permite crear varias pestañas para organizar el contenido de una página.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: e8b3e55a42b6be6262d6f51b9569c0be3e8ce6c3
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 100%

---

# Componente Pestañas {#tabs-component}

El componente Pestañas de componente principal permite la organización del contenido en varias pestañas.

## Uso {#usage}

El componente Pestañas permite al autor del contenido organizar el contenido de la página en varias pestañas.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor del contenido definir varias pestañas, así como establecer la pestaña activa. Con el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede definir qué componentes se pueden añadir a las pestañas y personalizar los estilos.

>[!TIP]
>
>Se admiten los componentes de pestaña anidados (pestañas dentro de pestañas).
>
>Los componentes de pestaña simples (no anidados) se pueden localizar o seleccionar mediante el [árbol de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es#content-tree); sin embargo, las pestañas anidadas no.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Tabs es la versión 1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| Versión 1 | Compatible  con la <br>[versión 2.17.4](/help/versions.md) y anterior | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Pestañas, ver ejemplos de sus opciones de configuración y la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_tabs_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Pestañas [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Vinculación profunda a un panel {#deep-linking}

Los componentes [Carrusel,](carousel.md) Pestañas y [Acordeón](accordion.md) admiten el enlace directo a un panel dentro del componente.

Para ello:

1. Visualice la página con el componente utilizando la opción **[Ver como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#view-as-published)** en el editor de páginas.
1. Inspeccione el contenido de la página e identifique el ID del panel.
   * Por ejemplo `id="accordion-86196c94d3-item-ca319dbb0b"`
1. El ID se convierte en el anclaje que puede anexar a la URL mediante un hash (`#`).
   * Por ejemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Si se desplaza a la dirección URL con el ID de panel como anclaje, el explorador se desplazará directamente al componente en cuestión y mostrará el panel especificado. Si el panel está configurado para no expandirse de forma predeterminada, se expandirá automáticamente.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido crear, cambiar el nombre y reorganizar pestañas, así como definir la pestaña activa.

### Pestaña Elementos {#items-tab}

![Pestaña Elementos del cuadro de diálogo de edición del componente](/help/assets/tabs-edit-items.png)

Utilice el botón **Añadir** para abrir el selector de componentes y elegir qué componente añadir como pestaña. Una vez añadida, se añade una entrada a la lista, que contiene las siguientes columnas:

* **Icono**: el icono del tipo de componente de la pestaña para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción**: la descripción utilizada como texto de la pestaña, de forma predeterminada, es el nombre del componente seleccionado para la pestaña.
* **Eliminar**: toque o haga clic para eliminar la pestaña del componente de pestaña.
* **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de las pestañas.

>[!TIP]
>
>Si la ventana móvil de la página se reduce para que el cuadro de diálogo de edición pase a estar en pantalla completa, el botón **Añadir** se ocultará. Los componentes se pueden añadir al componente Pestañas arrastrando [desde el explorador de componentes y soltando en el componente Pestañas del editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#inserting-a-component).

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Pestañas](/help/assets/tabs-edit-properties.png)

* **Elemento activo**: el autor del contenido puede definir qué pestaña está activa cuando se carga la página.
   * Con la opción **Por defecto**, se selecciona la primera pestaña.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña del cuadro de diálogo de edición del componente pestaña de accesibilidad](/help/assets/tabs-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: valor de un atributo de etiqueta ARIA para el componente

## Seleccionar panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un panel diferente y editarlo, así como para reorganizar fácilmente el orden de las pestañas.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las pestañas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las pestañas y se refleja en la numeración.
* El tipo de componente de la pestaña se muestra primero, seguido de la descripción de la pestaña con la fuente más clara.

![Seleccionar la ventana emergente del panel](/help/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a esa pestaña.
* Las pestañas se pueden cambiar utilizando los controladores de arrastre.

>[!NOTE]
>
>El autor no puede seleccionar las pestañas cuando se encuentra en modo **Editar**. Utilice el modo **[Vista previa](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#preview-mode)** o la opción **[Ver como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#view-as-published)** para interactuar con las pestañas como lector del contenido publicado.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como elementos al componente de pestañas, así como definir qué estilos personalizados están disponibles para el autor del contenido.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes puede añadir el autor de contenido como elementos al componente de pestañas.

La pestaña Componentes permitidos funciona del mismo modo que la del mismo nombre cuando [define la directiva y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Estilos {#styles-tab}

El componente Pestañas es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Pestañas es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
