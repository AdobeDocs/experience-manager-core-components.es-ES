---
title: Componente carrusel
description: El componente Carrusel permite al autor del contenido presentar el contenido en un carrusel giratorio.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 1%

---


# Componente de carrusel{#carousel-component}

El componente de carrusel de componentes principales permite al autor del contenido presentar el contenido en un carrusel navegable.

## Uso {#usage}

Con el componente Carrusel, el autor del contenido organizará el contenido en un carrusel giratorio de diapositivas.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor de contenido crear, asignar nombres y ordenar varias diapositivas, así como habilitar la transición automática con demora. Con el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede definir qué componentes se pueden agregar al carrusel, habilitar o deshabilitar las transiciones automáticas y personalizar los estilos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Carrusel es v1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente Carrusel, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_carousel).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Carrusel [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido añadir, cambiar el nombre y reorganizar diapositivas, así como definir la configuración de transición automática.

### Ficha Elementos {#items-tab}

![Ficha Elementos del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-items.png)

Utilice el botón **Add** para abrir el selector de componentes y elegir qué componente añadir como pestaña. Una vez añadida, se añade una entrada a la lista, que contiene las columnas siguientes:

* **Icono** : el icono del tipo de componente de la pestaña para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción** : La descripción utilizada como texto de la pestaña, de forma predeterminada, es el nombre del componente seleccionado para la pestaña.
* **Eliminar** : toque o haga clic para eliminar la ficha del componente de pestañas.
* **Reordenar** : toque o haga clic y arrastre para ordenar las pestañas.

>[!TIP]
>
>Si la ventanilla móvil de la página se reduce para que el cuadro de diálogo de edición pase a estar en pantalla completa, el botón **Add** se ocultará. Los componentes se pueden añadir al componente de carrusel arrastrando [desde el navegador de componentes y soltando en el componente de carrusel en el editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-properties.png)

En la pestaña **Properties**, el autor del contenido puede configurar las diapositivas para la transición automática.

* **Transición automática de diapositivas** : cuando esté activo, el componente avanzará automáticamente a la siguiente diapositiva después de un retraso especificado.
* **Retraso de transición** : cuando se selecciona Automáticamente diapositivas de transición, este valor se utiliza para definir el retardo entre transiciones (en milisegundos).
* **Deshabilitar la pausa automática al pasar el cursor** : cuando se selecciona la  **diapositiva de transición** automática, la transición de carrusel se pausa automáticamente cada vez que el cursor pasa el ratón sobre el carrusel. Seleccione esta opción para que la transición no se detenga.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

>[!NOTE]
>
>Los controles avanzados de diapositivas no están activados en el modo **Edit**. Utilice el modo [**Preview**](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) o la opción **[View as Published](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para interactuar con el carrusel como haría un lector del contenido publicado.
>
>La función de avance automático no está habilitada cuando se encuentra en modo **Editar**. Utilice la opción **[Ver como aparece publicado](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** para ver la función de avance automático como lo haría un lector del contenido publicado.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas [ARIA accesibilidad](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta** : Valor de un atributo de etiqueta ARIA para el componente

## Seleccionar panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a una diapositiva diferente para editarla, así como para reorganizar fácilmente el orden de las diapositivas.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las diapositivas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las diapositivas y se refleja en la numeración.
* El tipo de componente de la diapositiva se muestra primero, seguido de la descripción de la diapositiva en fuente más ligera.

![Seleccione el panel](/help/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a esa diapositiva.
* La diapositiva se puede reordenar en su lugar mediante los controles de arrastre.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como diapositivas al componente de carrusel, así como definir los valores predeterminados de transición automática y qué estilos personalizados están disponibles para el autor del contenido.

### Ficha Propiedades {#properties-tab-1}

La pestaña **Properties** se utiliza para definir la configuración predeterminada de las transiciones de diapositivas cuando un autor de contenido añade el componente de carrusel a una página.

![Cuadro de diálogo Diseño del componente Carrusel](/help/assets/carousel-design.png)

* **Diapositivas de transición automática** : define si, de forma predeterminada, la opción para avanzar automáticamente el carrusel a la siguiente diapositiva está activada cuando el autor de contenido añade el componente de carrusel a una página.
* **Retraso de transición** : define el valor predeterminado del retraso de transición entre diapositivas (en milisegundos) cuando un autor de contenido añade el componente de carrusel a una página.
* **Deshabilitar la pausa automática al pasar el cursor** : Define si, de forma predeterminada, la opción para desactivar la pausa automática de la diapositiva está habilitada cuando el autor de contenido selecciona  **Automáticamente la** diapositiva de transición.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes el autor de contenido puede añadir como diapositivas al componente de carrusel.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre cuando [define la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Pestaña Estilos {#styles-tab}

El componente Carrusel es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Carrusel es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
