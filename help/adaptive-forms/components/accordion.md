---
title: Acordeón de formulario adaptable
description: Utilice el acordeón para organizar y simplificar un formulario largo o complejo, dividiéndolo en secciones más pequeñas y manejables.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 8388de05c86641d4887b48a9fd10901cb5a19998
workflow-type: tm+mt
source-wordcount: '2174'
ht-degree: 100%

---

# Componente Acordeón {#accordion-component-adaptive-forms-core-component}

El componente principal Acordeón permite a los usuarios crear secciones expandibles y contraíbles en un formulario adaptable. A menudo se utiliza para organizar y simplificar formularios largos o complejos, dividiéndolos en secciones más pequeñas y manejables. Cada sección de un acordeón suele estar representada por un encabezado en el que el usuario puede hacer clic para expandir o reducir el contenido correspondiente. El contenido puede ser cualquier componente principal.

![ejemplo](/help/adaptive-forms/assets/example-accordion.png)

## Uso {#usage}

Existen varias razones por las que resulta beneficioso incluir un acordeón en un Formulario adaptable, entre ellas:

- **Ahorro de espacio**: un acordeón permite a los usuarios expandir y contraer secciones de un formulario, lo que reduce el espacio necesario para mostrar todos los campos del formulario a la vez.

- **Navegación**: un acordeón sirve para crear una estructura de navegación jerárquica, facilitando a los usuarios la búsqueda de los campos de formulario que necesitan.

- **Experiencia del usuario**: el acordeón se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

- **Formularios largos**: el acordeón es un componente ideal para manejar formularios largos, ya que permite a los usuarios centrarse en una sección a la vez, en lugar de intentar procesar mucha información a la vez.

Puede utilizar lo siguiente:

- El [cuadro de diálogo de configuración](#configure-dialog) para especificar las propiedades del componente acordeón.

- La opción [Seleccionar la ventana emergente del panel](#select-panel-popover) sirve para definir el orden de los paneles del acordeón. Esto permite al autor organizar los paneles en el orden en que deberían aparecer.

- Opciones para que un autor de formularios active o desactive determinadas funciones del [cuadro de diálogo Diseño](#design-dialog). Por ejemplo, un autor puede desactivar determinados campos o secciones de un formulario. Estas opciones permiten que el autor tenga un mayor control sobre el diseño y la funcionalidad del formulario, lo que facilita la creación de formularios que se adaptan a las necesidades específicas de la organización.

El cuadro de diálogo de configuración, seleccionar la ventana emergente del panel y el cuadro de diálogo Diseño, todos forman parte de los componentes principales que logran facilitar la generación de formularios y proporcionar una forma eficaz de crear formularios complejos.

## Versión y compatibilidad {#version-and-compatibility}


El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación, se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente Acordeón en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de acordeón para los visitantes con el cuadro de diálogo de configuración. También puede definir con facilidad los elementos de acordeón, paneles, comportamiento y apariencia para que la experiencia del usuario sea perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/acc-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Agrupar datos de componentes secundarios al enviar el formulario (ajustar datos en objeto)**: cuando se selecciona la opción, los datos de sus componentes secundarios se anidan dentro del objeto JSON del componente principal. Sin embargo, si la opción no está seleccionada, los datos JSON enviados tienen una estructura plana, sin ningún objeto para el componente principal. Por ejemplo:

   - Cuando la opción está seleccionada, los datos de los componentes secundarios (por ejemplo, calle, ciudad y código postal) se anidan dentro del componente principal (dirección) como un objeto JSON. Esto crea una estructura jerárquica y los datos se organizan bajo el componente principal.

     Estructura de los datos enviados:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Cuando la opción no está seleccionada, los datos JSON enviados tienen una estructura plana sin ningún objeto para el componente principal (dirección). Todos los datos se encuentran al mismo nivel, sin ninguna organización jerárquica.


     Estructura de los datos enviados:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Diseño**: puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en su sitio, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear el Nombre, Segundo nombre y Apellido en un formulario en una sola fila.

- **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Repetir acordeón {#repeat-accordion}

![acordeón repetido](/help/adaptive-forms/assets/repeat-accordion.png)

Puede utilizar las opciones de repetibilidad para duplicar paneles de acordeón y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente de acordeón y acceder a su configuración, se presentan las siguientes opciones:

- **Hacer que el acordeón sea repetible**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
- **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el panel de acordeón. Un valor de cero indica que el panel de acordeón no se repite; el valor predeterminado es cero.
- **Máximo de repeticiones**: define el número máximo de veces que se puede repetir el panel de acordeón. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro del acordeón, siga los pasos que se proporcionan en el artículo [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=es).

### Pestaña Elementos {#items-tab}

![Pestaña Elementos](/help/adaptive-forms/assets/acc-items.png)

El botón Agregar permite seleccionar un componente para agregarlo como panel en la ventana de selección de componentes. Después de añadir el componente, podrá ver las siguientes opciones:

- **Icono**: el icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información sobre herramientas.
- **Descripción**: la descripción utilizada como texto del panel. El nombre del componente está seleccionado para el panel de forma predeterminada,
- **Eliminar**: toque o haga clic para eliminar el panel del componente de acordeón.
- **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/acc-helpcontent.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/acc-accessisbilty.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [Accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente. Hay varias opciones disponibles para usar el texto del lector de pantalla:

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.


   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea agregar etiquetas de accesibilidad de ARIA.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente acordeón de formularios adaptables, puede establecer lo siguiente:

- El tipo de elementos de encabezado HTML que se permiten y establecen como valor predeterminado (como H1, H2, H3, etc.)
- Componentes principales que un creador de formularios puede agregar al acordeón en el editor de formularios adaptables
- Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente de acordeón en el editor de formularios adaptables.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Propiedades {#properties-tab-design}

La pestaña Propiedades permite a los autores de plantillas definir elementos de encabezado HTML predeterminados y permitidos para los autores de formularios:

![Pestaña Propiedades del cuadro de diálogo Diseño](/help//adaptive-forms/assets/accordion-design-properties.png)

- **Elementos de encabezado permitidos**: una lista desplegable con varias opciones que permite al autor de la plantilla elegir qué elementos de encabezado puede utilizar el autor de formularios para el acordeón.

- **Elemento Encabezado predeterminado**: una lista desplegable establece el elemento Encabezado predeterminado para el componente de acordeón.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña de componentes permitidos del cuadro de diálogo Diseño](/help//adaptive-forms/assets/accordion-allowed-components.png)

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden agregar como elementos a los paneles en el componente de acordeón del editor de formularios adaptables.

### Pestaña Estilos {#styles-tab}

![Pestaña estilo del cuadro de diálogo de diseño](/help/adaptive-forms/assets/accordion-styles-tab.png)

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de acordeón de formularios adaptables es compatible con [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente de acordeón.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![acordion-custom-properties-tab](/help/adaptive-forms/assets/accordion-custom-properties-tab.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Vea también {#see-also}

{{see-also}}