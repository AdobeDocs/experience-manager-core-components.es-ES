---
title: 'Componente principal de formularios adaptables: pestañas horizontales'
description: Uso o personalización del componente principal de pestañas horizontales de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 100%

---

# Pestañas horizontales {#horizontal-tabs-adaptive-forms-core-component}

Las pestañas horizontales de un Formulario adaptable hacen referencia a un patrón de diseño en el que varias secciones de un formulario se agrupan conjuntamente y se muestran como pestañas independientes, alineadas horizontalmente. Se puede pasar de una pestaña a otra para acceder a diferentes secciones del formulario. Cada pestaña actúa como un activador para mostrar y ocultar el contenido del formulario relacionado. Las pestañas horizontales ayudan a organizar formularios largos en secciones manejables y mejoran la experiencia del usuario. Las pestañas pueden ayudar a que un formulario sea más accesible para las personas con discapacidades, ya que pueden cambiar entre secciones con la navegación mediante el teclado.

Las pestañas generalmente se crean como una serie de vínculos o botones, y cada vínculo o botón corresponde a una sección del formulario. Cuando se hace clic en una pestaña, el contenido del formulario se actualiza de forma dinámica para mostrar la sección correspondiente.

## Uso {#reasons-to-use-horizontal-tabs}

Las razones más comunes para utilizar pestañas horizontales en un Formulario adaptable son las siguientes:

* **Uso mejorado**: las pestañas horizontales facilitan a los usuarios el desplazamiento por el formulario, especialmente si este tiene varias secciones o un varios número de campos.

* **Administración del espacio**: las pestañas horizontales ayudan a conservar espacio en la pantalla al agrupar las secciones de formulario relacionadas en pestañas y mostrar solo una sección a la vez.

* **Mejor organización**: las pestañas proporcionan una estructura clara y organizada para un formulario, lo que facilita la comprensión y cumplimentación del formulario.

* **Mayor participación del usuario**: las pestañas horizontales pueden hacer que un formulario sea visualmente más atractivo y atrayente para los usuarios, lo que puede mejorar la tasa de finalización del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de pestañas horizontales de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las pestañas horizontales para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones de pestañas horizontales con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Ajustar datos en objeto**: seleccione “Ajustar los datos en un objeto” para colocar los datos del asistente dentro de un objeto JSON. Si no se selecciona, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño**: puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en su sitio, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear el Nombre, Segundo nombre y Apellido en un formulario en una sola fila.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Elementos {#items-tab}

![Pestaña Elementos](/help/adaptive-forms/assets/tabsontop_itemstab.png)

El botón **Agregar** permite seleccionar un componente para añadirlo como un panel en la ventana de selección de componentes. Después de añadir el componente, podrá ver las siguientes opciones:

* **Icono**: el icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información sobre herramientas.
* **Descripción**: la descripción utilizada como texto del panel. De forma predeterminada, el nombre del componente seleccionado para el panel.
* **Eliminar**: toque o haga clic para eliminar el panel del componente de pestañas horizontales.
* **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

* **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente de formularios adaptables, puede establecer lo siguiente:

* Los componentes principales que un creador de formularios puede añadir a las pestañas horizontales del editor de formularios adaptables.
* Nombres simples para estilos (clases CSS) que pueden aplicarse en el cuadro de diálogo de propiedades del componente de pestañas horizontales en el editor de formularios adaptables.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente de pestañas horizontales del editor de formularios adaptable.

![Pestañas horizontales](/help/adaptive-forms/assets/horizontaltabs_designdilog.png)

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de las pestañas horizontales de formularios adaptable es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/horizontaltabs_designstyletab.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de las pestañas horizontales de formularios adaptable.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.
