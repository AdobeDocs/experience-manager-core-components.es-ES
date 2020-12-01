---
title: Componente de carrusel
description: El componente Carrusel permite al autor del contenido presentar contenido en un carrusel rotatorio.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 1%

---


# Componente de carrusel{#carousel-component}

El componente de carrusel de componentes principales permite al autor del contenido presentar el contenido en un carrusel navegable.

## Uso {#usage}

Con el componente Carrusel, el autor del contenido organiza el contenido en un carrusel rotatorio de diapositivas.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor del contenido crear, nombrar y ordenar varias diapositivas, así como habilitar la transición automática con retraso. Mediante el cuadro de diálogo [diseño](#design-dialog), el autor de la plantilla puede definir qué componentes se pueden agregar al carrusel, activar o desactivar las transiciones automáticas y personalizar los estilos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Carrusel es v1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Carrusel y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_carousel).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de carrusel [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido agregar, cambiar el nombre y reorganizar diapositivas, así como definir la configuración de transición automática.

### Ficha Elementos {#items-tab}

![Ficha Elementos del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-items.png)

Utilice el botón **Añadir** para abrir el selector de componentes y elegir qué componente agregar como ficha. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:

* **Icono** : icono del tipo de componente de la ficha para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : descripción utilizada como texto de la ficha, de forma predeterminada según el nombre del componente seleccionado para la ficha.
* **Eliminar** : toque o haga clic para eliminar la ficha del componente de fichas.
* **Reordenar** : toque o haga clic y arrastre para ordenar las fichas.

>[!TIP]
>
>Si se reduce la ventanilla de la página para que el cuadro de diálogo de edición se muestre a pantalla completa, se ocultará el botón **Añadir**. Los componentes se pueden agregar al componente Carrusel arrastrándolos [desde el navegador de componentes y colocándolos en el componente Carrusel en el editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-properties.png)

En la ficha **Propiedades**, el autor del contenido puede definir las diapositivas para que se transición automáticamente.

* **Transición automática de diapositivas** : al activarse, el componente avanzará automáticamente a la siguiente diapositiva tras un retraso especificado.
* **Retraso**  de transición: cuando se selecciona transición automática de diapositivas, este valor se utiliza para definir el retraso entre transiciones (en milisegundos).
* **Deshabilitar la pausa automática al pasar**  el cursor por encima del carrusel: cuando  **se selecciona** la diapositiva de transición automática, la transición del carrusel se pausa automáticamente cada vez que el cursor se sitúa sobre el carrusel. Seleccione esta opción para que la transición no se detenga.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

>[!NOTE]
>
>Los controles de avance de diapositivas no están activados cuando están en el modo **Editar**. Utilice el modo [**Previsualización**](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) o la opción **[Vista tal como Publicada](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interactuar con el carrusel como un lector del contenido publicado.
>
>La función de avance automático no está habilitada cuando se encuentra en el modo **Editar**. Utilice la opción **[Vista como Publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para ver la función de avance automático como un lector del contenido publicado.

### Ficha Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-accessibility.png)

En la ficha **Accesibilidad**, se pueden definir valores para las etiquetas [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Seleccionar panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas del componente para cambiar a una diapositiva diferente y editarla, así como para reorganizar fácilmente el orden de las diapositivas.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las diapositivas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las diapositivas y se refleja en la numeración.
* El tipo de componente de la diapositiva se muestra primero, seguido de la descripción de la diapositiva en una fuente más clara.

![Seleccione el panel](/help/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, se cambia la vista del editor a esa diapositiva.
* La diapositiva se puede reordenar en su lugar mediante los controladores de arrastre.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como diapositivas al componente de carrusel, así como definir los valores predeterminados de transición automática y qué estilos personalizados están disponibles para el autor del contenido.

### Ficha Propiedades {#properties-tab-1}

La ficha **Propiedades** se utiliza para definir la configuración predeterminada de las transiciones de diapositivas cuando un autor de contenido agrega el componente carrusel a una página.

![Cuadro de diálogo Diseño del componente Carrusel](/help/assets/carousel-design.png)

* **Transición automática de diapositivas** : define si, de forma predeterminada, la opción para avanzar automáticamente el carrusel a la siguiente diapositiva está activada cuando el autor del contenido agrega el componente de carrusel a una página.
* **Retraso**  de transición: define el valor predeterminado del retraso de transición entre diapositivas (en milisegundos) cuando un autor de contenido agrega el componente de carrusel a una página.
* **Deshabilitar la pausa automática al pasar**  el ratón por encima: define si la opción predeterminada para desactivar la pausa automática de diapositivas está activada cuando el autor del contenido selecciona  **automáticamente la** diapositiva de transición.

### Ficha Componentes permitidos {#allowed-components-tab}

La ficha **Componentes permitidos** se utiliza para definir qué componentes puede agregar el autor del contenido como diapositivas al componente de carrusel.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre cuando [define la política y las propiedades de un Contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Ficha Estilos {#styles-tab}

El componente Carrusel es compatible con el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).
