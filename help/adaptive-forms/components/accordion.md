---
title: Acordeón de formulario adaptable
description: Utilice el acordeón para organizar y simplificar un formulario largo o complejo dividiéndolo en secciones más pequeñas y manejables.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 0cfdc56fe5508e156eee2ae818be311748af7247
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 3%

---

# Componente Acordeón {#accordion-component-adaptive-forms-core-component}

El componente principal de acordeón permite a los usuarios crear secciones expandibles y contraíbles en un formulario adaptable. A menudo se utiliza para organizar y simplificar formularios largos o complejos, dividiéndolos en secciones más pequeñas y manejables. Cada sección de un acordeón suele estar representada por un encabezado en el que el usuario puede hacer clic para expandir o contraer el contenido correspondiente. El contenido puede ser cualquier componente principal.

## Uso {#usage}

Existen varias razones por las que resulta beneficioso incluir un acordeón en un formulario adaptable, entre ellas:

* **Ahorro de espacio**: Un acordeón permite a los usuarios expandir y contraer secciones de un formulario, lo que reduce el espacio necesario para mostrar todos los campos del formulario a la vez.

* **Navegación**: Se puede utilizar un acordeón para crear una estructura de navegación jerárquica, facilitando a los usuarios la búsqueda de los campos de formulario que necesitan.

* **Experiencia del usuario**: El acordeón se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

* **Long Forms**: El acordeón es un componente ideal para manejar formularios largos, ya que permite a los usuarios centrarse en una sección a la vez, en lugar de intentar procesar mucha información a la vez.

Puede utilizar:

* La variable [cuadro de diálogo configurar](#configure-dialog) para especificar las propiedades del componente acordeón.

* La variable [Seleccionar la ventana emergente del panel](#select-panel-popover)  para definir el orden de los paneles del acordeón. Esto permite al autor organizar los paneles en el orden en que deberían aparecer los paneles.

* Opciones para que un autor de formularios active o desactive determinadas funciones de la sección [cuadro de diálogo de diseño](#design-dialog). Por ejemplo, un autor puede desactivar ciertos campos o secciones de un formulario. Estas opciones permiten al autor tener bueno control sobre el diseño y la funcionalidad del formulario, lo que facilita la creación de formularios adaptados a las necesidades específicas de la organización.

El cuadro de diálogo de configuración, la ventana emergente del panel de selección y el cuadro de diálogo de diseño forman parte de los componentes principales creados para facilitar la creación de formularios y proporcionar una forma eficaz de crear formularios complejos.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del acordeón de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posterior. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posterior |
|---|---|---|
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/adaptive-forms/version.md) y posterior | Compatible con<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posterior pero inferior a 2.0.0. |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente Acordeón en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de acordeón para los visitantes con el cuadro de diálogo Configurar . También puede definir con facilidad elementos de acordeón, paneles, comportamiento y apariencia para que la experiencia de usuario sea perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/accordion_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Ajustar datos en objeto** - Seleccione &quot;Ajuste de datos en un objeto&quot; para colocar los datos de campo del asistente dentro de un objeto JSON. Si no se elige, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño** - Puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en el lugar, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear &quot;Nombre&quot;, &quot;Nombre central&quot; y &quot;Apellido&quot; en un formulario en una sola fila.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Elementos {#items-tab}

![Ficha Elementos](/help/adaptive-forms/assets/accordion_itemstab.png)

El botón Add permite seleccionar un componente para agregarlo como panel en la ventana de selección de componentes. Después de añadir el componente, puede ver las siguientes opciones:

* **Icono** : El icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información de objeto.
* **Descripción** - La descripción utilizada como texto del panel. De forma predeterminada, el nombre del componente está seleccionado para el panel.
* **Eliminar**: toque o haga clic para eliminar el panel del componente de acordeón.
* **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Ficha Contenido de ayuda {#help-content}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Ficha Accesibilidad](/help/adaptive-forms/assets/accordion_accessibility.png)

**Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente Acordeón de Forms adaptable, puede establecer lo siguiente:

* El tipo de elementos de encabezado del HTML que se permiten y establecen como predeterminados (como H1, H2, H3, etc.)
* Componentes principales que un creador de formularios puede agregar al acordeón en el editor de Forms adaptable
* Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente de acordeón en el editor de Forms adaptable.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Propiedades {#properties-tab-design}

La ficha Propiedades permite a los autores de plantillas definir elementos de encabezado de HTML predeterminados y permitidos para los autores de formularios:

![Pestaña Propiedades del cuadro de diálogo de diseño](/help/assets/accordion-design-properties.png)

* **Elementos de encabezado permitidos**: Una lista desplegable con varias opciones que permite al autor de la plantilla elegir los encabezados que los elementos pueden utilizar para crear acordeón.

* **Elemento Encabezado predeterminado**: Una lista desplegable establece el elemento Encabezado predeterminado para el componente de acordeón.

### Pestaña Componentes permitidos {#allowed-components-tab}

La variable **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente Acordeón del editor de Forms adaptable.

![Pestaña Componentes permitidos](/help/adaptive-forms/assets/accordion_allowedcomponents.png)

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar los estilos CSS de un componente. El componente principal del acordeón de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Ficha Estilo](/help/adaptive-forms/assets/accordion_style.png)

* **Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente acordeón.

* **Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

