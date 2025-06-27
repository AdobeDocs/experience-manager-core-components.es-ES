---
title: Componente Carrusel
description: El componente Carrusel permite al autor del contenido presentar el contenido en un carrusel giratorio.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Carrusel{#carousel-component}

El componente de carrusel de componentes principales permite al autor del contenido presentar el contenido en un carrusel navegable.

{{traditional-aem}}

## Uso {#usage}

Con el componente Carrusel, el autor del contenido organizará el contenido en un carrusel giratorio de diapositivas.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor de contenido crear, asignar nombres y ordenar varias diapositivas, así como habilitar la transición automática con retraso. Con el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede definir qué componentes se pueden agregar al carrusel, habilitar o deshabilitar las transiciones automáticas y personalizar los estilos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Carrusel es la versión 1, que se introdujo con la versión 2.2.0 de los componentes principales en octubre de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Carrusel, ver ejemplos de sus opciones de configuración y HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_carousel_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Carrusel [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Vinculación profunda a un panel {#deep-linking}

Los componentes Carrusel, [Pestañas](tabs.md) y [Acordeón](accordion.md) admiten el enlace directo a un panel dentro del componente.

Para ello:

1. Visualice la página con el componente utilizando la opción **[Ver como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#view-as-published)** en el editor de páginas.
1. Inspeccione el contenido de la página e identifique el ID del panel.
   * Por ejemplo `id="carousel-bfe4fa6647-item-47f1a7ca67-tabpanel"`
1. El ID se convierte en el anclaje que puede anexar a la URL mediante un hash (`#`).
   * Por ejemplo `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#carousel-bfe4fa6647-item-47f1a7ca67-tabpanel`

Si se desplaza a la dirección URL con el ID de panel como anclaje, el explorador se desplazará directamente al componente en cuestión y mostrará el panel especificado. Si el panel está configurado para no mostrarse de forma predeterminada, se desplazará a automáticamente.

## Carrusel y diseño interactivo {#responsive-design}

Todos los componentes principales están diseñados para responder completamente, lo que garantiza una experiencia sin problemas en todos los dispositivos.

Algunos componentes avanzados, como el componente Carrusel, pueden requerir una consideración específica en el contexto del proyecto de implementación para mantener la capacidad de respuesta en todas las condiciones. Consulte el documento [Diseño interactivo de los componentes principales](/help/responsive.md) para obtener más información.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido añadir, cambiar el nombre y reorganizar las diapositivas, así como definir la configuración de transición automática.

### Pestaña Elementos {#items-tab}

![Pestaña Elementos del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-items.png)

Utilice el botón **Añadir** para abrir el selector de componentes y elegir qué componente añadir como pestaña. Una vez añadida, se añade una entrada a la lista, que contiene las siguientes columnas:

* **Icono**: el icono del tipo de componente de la pestaña para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Descripción**: la descripción utilizada como texto de la pestaña, de forma predeterminada, es el nombre del componente seleccionado para la pestaña.
* **Eliminar**: toque o haga clic para eliminar la pestaña del componente de pestañas.
* **Reordenar**: toque o haga clic y arrastre para ordenar las pestañas.

>[!TIP]
>
>Si la ventana móvil de la página se reduce para que el cuadro de diálogo de edición pase a estar en pantalla completa, el botón **Añadir** se ocultará. Los componentes se pueden añadir al componente de carrusel [arrastrando desde el explorador de componentes y soltando en el componente de carrusel en el editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#inserting-a-component-from-the-components-browser).

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-properties.png)

En la pestaña **Propiedades**, el autor del contenido puede configurar la transición automática de las diapositivas.

* **Elemento activo**: el autor del contenido puede definir qué pestaña está activa cuando se carga la página.
* **Transición automática de diapositivas**: cuando esté activo, el componente avanzará automáticamente a la siguiente diapositiva después de un retraso especificado.
* **Retraso de transición**: cuando se selecciona la transición automática de diapositivas, este valor se utiliza para definir el retardo entre transiciones (en milisegundos).
* **Deshabilitar la pausa automática al pasar el puntero**: cuando se selecciona la **transición automática de diapositivas**, la transición de carrusel se pausa automáticamente cada vez que se pasa el puntero por encima del carrusel. Seleccione esta opción para que la transición no se detenga.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

>[!NOTE]
>
>Los controles avanzados de diapositivas no están activados en el modo **Editar**. Utilice el modo [**Vista previa**](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#preview-mode) o la opción **[Ver como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#view-as-published)** para interactuar con el carrusel como lo haría un lector del contenido publicado.
>
>La función de avance automático no está habilitada cuando se encuentra en modo **Editar**. Utilice la opción **[Ver como publicado](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#view-as-published)** para ver la función de avance automático como lo haría un lector del contenido publicado.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Carrusel](/help/assets/carousel-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: valor de un atributo de la etiqueta aria para el carrusel, el cual describe su contenido
* **Anterior**: valor de un atributo de la etiqueta aria para la etiqueta de botón anterior de la navegación del carrusel
* **Siguiente**: valor de un atributo de la etiqueta aria para la etiqueta de botón siguiente de la navegación del carrusel
* **Reproducción**: valor de un atributo de la etiqueta aria para la etiqueta del botón de reproducción de la navegación del carrusel
* **Pausa**: valor de un atributo de la etiqueta aria para la etiqueta del botón de pausa de la navegación del carrusel
* **Lista de pestañas**: valor de un atributo de la etiqueta aria para la etiqueta de lista de elementos de la navegación del carrusel
* **Establecer la etiqueta aria del elemento en su título**: si está activada, esta opción establece automáticamente el título de los elementos de carrusel en su descripción de la etiqueta aria.

## Seleccionar panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a una diapositiva diferente para editarla, así como para reorganizar fácilmente el orden de las diapositivas.

![Icono Seleccionar panel](/help/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, las diapositivas configuradas se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de las diapositivas y se refleja en la numeración.
* El tipo de componente de la diapositiva se muestra primero, seguido de la descripción de la diapositiva con la fuente más clara.

![Seleccionar el panel](/help/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a esa diapositiva.
* La diapositiva se puede reordenar mediante los controladores de arrastre.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como diapositivas al componente de carrusel, así como definir los valores predeterminados de transición automática y qué estilos personalizados están disponibles para el autor del contenido.

### Pestaña Propiedades {#properties-tab-1}

La pestaña **Propiedades** se utiliza para definir la configuración predeterminada de las transiciones de diapositivas cuando un autor de contenido añade el componente de carrusel a una página.

![Cuadro de diálogo de diseño del componente Carrusel](/help/assets/carousel-design.png)

* **Diapositivas de transición automática**: define si, de forma predeterminada, la opción para avanzar automáticamente el carrusel a la siguiente diapositiva está activada cuando el autor de contenido añade el componente de carrusel a una página.
* **Prefijar elementos de control**: si está activada, los elementos de control se colocan delante de los elementos del carrusel para mejorar la accesibilidad.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes puede añadir el autor de contenido como diapositivas al componente de carrusel.

La pestaña Componentes permitidos funciona del mismo modo que la del mismo nombre cuando [define la directiva y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Estilos {#styles-tab}

El componente Carrusel es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Carrusel es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
