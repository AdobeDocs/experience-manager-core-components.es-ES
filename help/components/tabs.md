---
title: Componente de fichas
description: El componente Fichas permite la creación de varias fichas para organizar el contenido de una página.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de fichas

El componente Fichas de componentes principales permite organizar el contenido en varias fichas.

## Uso {#usage}

El componente Fichas permite al autor del contenido organizar el contenido de la página en varias fichas.

El cuadro de diálogo [de](#edit-dialog) edición permite al autor del contenido definir varias fichas, así como establecer la ficha activa. Mediante el cuadro de diálogo [de](#design-dialog)diseño, el autor de la plantilla puede definir qué componentes se pueden agregar a las fichas y personalizar los estilos.

>[!NOTE]
>
>Se admiten componentes de ficha anidados (fichas dentro de fichas).
>
>Los componentes de ficha simples (no anidados) pueden ubicarse o seleccionarse mediante el árbol [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)contenido; sin embargo, las fichas anidadas no pueden estar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Tabs es v1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Tabs y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_tabs)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Tabs [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido crear, cambiar el nombre y reorganizar fichas, así como definir la ficha activa.

### Ficha Elementos {#items-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.16.png)

Utilice el botón **Agregar** para abrir el selector de componentes y elegir qué componente agregar como ficha. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:

* **Icono** : icono del tipo de componente de la ficha para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : la descripción utilizada como texto de la ficha, de forma predeterminada según el nombre del componente seleccionado para la ficha.
* **Eliminar** : toque o haga clic para eliminar la ficha del componente de ficha.
* **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de las fichas.

>[!TIP]
>
>Si se reduce la ventanilla de la página para que el cuadro de diálogo de edición se muestre a pantalla completa, se ocultará el botón **Agregar** . Los componentes se pueden añadir al componente Tabs [arrastrándolos desde el navegador de componentes y colocándolos en el componente Tabs del editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)de páginas.

### Ficha Propiedades {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.32.png)

En la ficha **Propiedades** , el autor del contenido puede definir qué ficha está activa cuando se carga la página. Con la opción **Predeterminado** , se seleccionará la primera ficha.

### Ficha Accesibilidad {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.40.png)

En la ficha **Accesibilidad** , se pueden definir valores para las etiquetas de accesibilidad [de](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para el componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Select Panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un panel diferente para editarlo y reorganizar fácilmente el orden de las fichas.

![](/help/assets/screenshot_2018-10-11at165417.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las fichas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las fichas y se refleja en la numeración.
* El tipo de componente de la ficha se muestra primero, seguido de la descripción de la ficha en una fuente más ligera.

![](/help/assets/screenshot_2018-10-11at165154.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, se cambia la vista del editor a esa ficha.
* Las fichas se pueden reorganizar en su lugar mediante los controladores de arrastre.

>[!NOTE]
>
>El autor no puede seleccionar las fichas cuando se encuentra en el modo de **edición** . Utilice el modo **[Vista previa](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)**o la opción**[ Ver como publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interactuar con las fichas como lector del contenido publicado.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como elementos al componente de fichas, así como definir qué estilos personalizados están disponibles para el autor del contenido.

### Ficha Componentes permitidos {#allowed-components-tab}

La ficha Componentes **** permitidos se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente de fichas.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre al [definir la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Ficha Estilos {#styles-tab}

El componente Tabs es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
