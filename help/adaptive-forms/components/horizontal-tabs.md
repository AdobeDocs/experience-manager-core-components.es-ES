---
title: 'Componente principal de Forms adaptable: pestañas horizontales'
description: Uso o personalización del componente principal de las fichas horizontales de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1584'
ht-degree: 3%

---


# Tabulaciones horizontales {#horizontal-tabs-adaptive-forms-core-component}

Las fichas horizontales de un formulario adaptable hacen referencia a un patrón de diseño en el que varias secciones de un formulario se agrupan y se muestran como fichas independientes, alineadas horizontalmente. El usuario puede cambiar entre las fichas para acceder a diferentes secciones del formulario. Cada ficha actúa como un déclencheur para mostrar y ocultar el contenido del formulario relacionado. Las pestañas horizontales ayudan a organizar formularios largos en secciones manejables y a mejorar la experiencia del usuario. Las fichas pueden ayudar a que un formulario sea más accesible para los usuarios con discapacidades, ya que pueden cambiar entre secciones con la navegación mediante el teclado.

Las pestañas generalmente se crean como una serie de vínculos o botones, y cada vínculo o botón corresponde a una sección del formulario. Cuando un usuario hace clic en una ficha, el contenido del formulario se actualiza de forma dinámica para mostrar la sección correspondiente.

## Uso {#reasons-to-use-horizontal-tabs}

Los motivos comunes para utilizar pestañas horizontales en un Formulario adaptable son:

* **Mejora del uso**: Las pestañas horizontales facilitan a los usuarios el desplazamiento por el formulario, especialmente si este tiene varias secciones o un gran número de campos.

* **Gestión del espacio**: Las pestañas horizontales ayudan a conservar espacio en la pantalla al agrupar las secciones de formulario relacionadas en fichas y mostrar solo una sección a la vez.

* **Mejor organización**: Las fichas proporcionan una estructura clara y organizada para un formulario, lo que facilita a los usuarios comprender y completar el formulario.

* **Mayor participación del usuario**: Las pestañas horizontales pueden hacer que un formulario sea visualmente más atractivo y atractivo para los usuarios, lo que puede mejorar la tasa de finalización del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de las fichas horizontales de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de las fichas horizontales de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal fichas/v1/pageHorizontal tab). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de pestañas horizontales para los visitantes con el cuadro de diálogo Configurar . También puede definir opciones de pestañas horizontales con facilidad para que el usuario tenga una experiencia óptima.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Ajustar datos en objeto** - Seleccione &quot;Ajuste de datos en un objeto&quot; para colocar los datos de campo del asistente dentro de un objeto JSON. Si no se elige, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño** - Puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en el lugar, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear &quot;Nombre&quot;, &quot;Nombre central&quot; y &quot;Apellido&quot; en un formulario en una sola fila.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Elementos {#items-tab}

![Ficha Elementos](/help/adaptive-forms/assets/tabsontop_itemstab.png)

La variable **Agregar** permite seleccionar un componente para agregarlo como panel en la ventana de selección de componentes. Después de añadir el componente, puede ver las siguientes opciones:

* **Icono** : El icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información de objeto.
* **Descripción** - La descripción utilizada como texto del panel. De forma predeterminada, el nombre del componente seleccionado para el panel.
* **Eliminar**: toque o haga clic para eliminar el panel del componente de acordeón.
* **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Ficha Contenido de ayuda {#help-content}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Ficha Accesibilidad](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

* **función de HTML para que anuncie el lector de pantalla** - La función de HTML es un atributo utilizado para especificar el propósito de un elemento HTML para tecnologías de asistencia, como lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función &quot;etiqueta&quot; y su campo de entrada puede tener la función &quot;cuadro de texto&quot;. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarla correctamente al usuario.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente Acordeón de Forms adaptable, puede establecer lo siguiente:

* Componentes principales que un creador de formularios puede agregar al acordeón en el editor de Forms adaptable
* Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente de acordeón en el editor de Forms adaptable.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

La variable **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente de pestañas horizontales del editor de Forms adaptable.

### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de las fichas horizontales de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de las fichas horizontales de Forms adaptable.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.
