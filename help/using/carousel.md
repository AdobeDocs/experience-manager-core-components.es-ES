---
title: Componente Carrusel
seo-title: Componente Carrusel
description: nulo
seo-description: El componente Carrusel permite al autor del contenido presentar contenido en un carrusel rotatorio.
uuid: 34934491-bd 85-4 f 1 e-ae 22-bb 48 ed 4 dbd 5 c
content-type: referencia
topic-tags: componentes principales
discoiquuid: 3510812 b -9 d 3 e -40 fe-b 986-0 f 15 d 40 b 42 ad 42
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente Carrusel{#carousel-component}

El componente Carrusel de componente principal permite al autor del contenido presentar contenido en un carrusel navegable.

## Uso {#usage}

Con el componente Carrusel, el autor de contenido organiza el contenido en un carrusel rotatorio de diapositivas.

El cuadro [de diálogo](#edit-dialog) de edición permite al autor del contenido crear, nombrar y ordenar varias diapositivas, así como activar la transición automática con demora. Con el cuadro de diálogo [](#design-dialog)de diseño, el autor de la plantilla puede definir qué componentes se pueden agregar al carrusel, activar o desactivar transiciones automáticas y personalizar los estilos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Carrusel es v 1, introducida con la versión 2.2.0 de los componentes principales en octubre de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

A continuación se muestra una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/screenshot_2018-11-28at140433.png)

### Biblioteca de componentes {#component-library}

Para experimentar el componente Carrusel, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/carousel.html).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Carrusel [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido agregar, renombrar y reorganizar diapositivas, así como definir la configuración de transición automática.

### Ficha Elementos {#items-tab}

![](assets/screenshot_2018-10-12at102451.png)

Utilice el botón **Agregar** para abrir el selector de componentes y elegir qué componente agregar como ficha. Una vez agregado, se agrega una entrada a la lista, que contiene las columnas siguientes:

* **Icono** : el icono del tipo de componente de la ficha para facilitar la identificación en la lista. Pase el ratón para ver el nombre completo del componente como información de objeto.
* **Descripción** : La descripción utilizada como texto de la ficha, predeterminada al nombre del componente seleccionado para la ficha.
* **Eliminar** : toque o haga clic para eliminar la ficha del componente fichas.
* **Reordenar** : toque o haga clic y arrastre para ordenar las fichas.

### Ficha Propiedades {#properties-tab}

![](assets/screenshot_2018-11-28at141054.png)

En la ficha **Propiedades** , el autor de contenido puede configurar las diapositivas para que se transituren automáticamente.

* **Transición automática de diapositivas** : cuando se activa, el componente pasará automáticamente a la siguiente diapositiva después de un retraso especificado.
* **Retraso** de transición: cuando se selecciona automáticamente diapositivas de transición, este valor se utiliza para definir el retraso entre transiciones (en milisegundos).
* **Deshabilitar pausa automática al pasar el ratón** por encima: cuando **se seleccionan diapositivas** de transición automáticamente, la transición de carrusel se pausa automáticamente siempre que el cursor se sitúa sobre el carrusel. Seleccione esta opción para que la transición no se pause.

>[!NOTE]
>
>Los controles avanzados de diapositivas no están activados en el modo **de edición** . Utilice [**el modo Vista previa**](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) o **[la](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** opción Ver como publicado para interactuar con el carrusel como un lector del contenido publicado.
>
>La función de avance automático no está habilitada en el modo **de edición** . Utilice **[la opción Ver como publicado](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** para ver la función de avance automático como un lector del contenido publicado.

## Seleccionar panel {#select-panel}

El autor de contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a una diapositiva diferente para editarla y reorganizar fácilmente el orden de las diapositivas.

![](assets/screenshot_2018-10-11at165417.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas del componente, las diapositivas configuradas se muestran como una lista desplegable.

* La lista se ordena por la disposición asignada de las diapositivas y se refleja en la numeración.
* El tipo de componente de la diapositiva se muestra primero, seguido de la descripción de la diapositiva en la fuente más clara.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* Al tocar o hacer clic en una entrada del menú desplegable, cambia la vista del editor a esa diapositiva.
* La diapositiva se puede reordenar en contexto utilizando los controles de arrastrar.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes pueden agregarse como diapositivas al componente carrusel, así como definir valores predeterminados de transición automática y qué estilos personalizados están disponibles para el autor del contenido.

### Ficha Propiedades {#properties-tab-1}

La pestaña **Propiedades** se utiliza para definir la configuración predeterminada de las transiciones de diapositivas cuando un autor de contenido agrega el componente carrusel a una página.

![](assets/screenshot_2018-11-28at141824.png)

* **Transición de transición automática** : Define si de forma predeterminada la opción de avanzar automáticamente el carrusel a la siguiente diapositiva está activada cuando el autor del contenido agrega el componente carrusel a una página.
* **Retraso** de transición: define el valor predeterminado del retraso de transición entre las diapositivas (en milisegundos) cuando un autor de contenido agrega el componente carrusel a una página.
* **Deshabilitar pausa automática al pasar el ratón** : Define si de forma predeterminada la opción para desactivar la pausa automática de la diapositiva está habilitada cuando **el autor de contenido selecciona automáticamente diapositivas** de transición.

### Ficha Componentes permitidos {#allowed-components-tab}

La **ficha Componentes** permitidos se utiliza para definir qué componentes pueden agregarse como diapositivas al componente Carrusel por autor del contenido.

La ficha Componentes permitidos funciona de la misma manera que la ficha del mismo nombre al [definir la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Ficha Estilos {#styles-tab}

El componente Carrusel admite el sistema [de estilos AEM](authoring.md#component-styling).