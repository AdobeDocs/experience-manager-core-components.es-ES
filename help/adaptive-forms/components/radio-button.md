---
title: 'Componente principal de Forms adaptable: botón de radio'
description: Uso o personalización del componente principal del botón de radio de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 1%

---


# Botón de opción {#radio-button-adaptive-forms-core-component}

Un botón de opción de un formulario adaptable es un tipo de elemento de entrada que permite al usuario seleccionar una opción de un grupo de opciones relacionadas. Se representa mediante un pequeño botón circular que está relleno o vacío para indicar si la opción está seleccionada o no. Cuando un usuario selecciona un botón de radio, el resto del grupo deja de estar seleccionado. Los botones de opción suelen utilizarse cuando hay varias opciones mutuamente excluyentes y solo se puede seleccionar una a la vez.

**Ejemplo**

![](/help/adaptive-forms/assets/radio-button.png)

**Cuadro de diálogo Propiedades**

![](/help/adaptive-forms/assets/radio-button-properties.png)

En este ejemplo, el elemento Opciones se utiliza para agrupar los botones de radio. La variable **Mostrar texto** se utiliza para proporcionar una etiqueta para un elemento y **Valor de datos** se utiliza para especificar el valor que se envía al servidor cuando se envía el formulario.

Cada opción de botón de radio tiene un valor de datos y un atributo de texto mostrado . Si un usuario selecciona el &quot;1-10&quot;, el valor de datos correspondiente se envía al servidor cuando se envía el formulario. Estos datos se pueden procesar mediante una secuencia de comandos del lado del servidor para determinar qué opciones seleccionó el usuario y se pueden utilizar para realizar diversas acciones, como actualizar otros campos del formulario o enviar los datos del formulario a una secuencia de comandos del lado del servidor para un procesamiento posterior.

Además, cada botón de opción se puede configurar para que tenga valores de procesamiento diferentes para cada opción, y esto se puede configurar mediante el Editor de reglas de Forms adaptable

## Uso {#reasons-to-use-radio-button}

Existen varias razones para utilizar botones de opción en un formulario, entre ellas:

* **Opciones limitadas**: Los botones de opción se utilizan para proporcionar una lista de opciones predefinidas entre las que el usuario puede elegir y solo se puede seleccionar una opción a la vez. Esto resulta útil cuando el número de opciones es limitado y mutuamente excluyente.

* **Borrar representación**: Los botones de radio son claros y fáciles de entender, lo que facilita a los usuarios saber lo que seleccionan.

* **Coherencia**: El uso de botones de opción garantiza una forma uniforme y estandarizada de presentar opciones a los usuarios, facilitando su comprensión e interacción con el formulario.

* **Más fácil de usar**: Los botones de radio son fáciles de usar, especialmente para usuarios que no están familiarizados con la tecnología o que tienen movilidad limitada.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del botón de radio adaptable de Forms se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del botón de radio adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia con el botón de radio para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de los botones de opción con facilidad para que el usuario tenga una experiencia óptima.

![Ficha Básico](/help/adaptive-forms/assets/radiobutton_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

   En el **Opciones** , puede agregar valores de datos y mostrar pares de texto utilizando la pestaña **Agregar** botón. Una vez añadida una nueva opción, se pueden realizar las siguientes acciones:

   * **Valor de datos** - Esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   * **Mostrar texto** - Esta opción permite introducir el contenido que se mostrará en un formulario adaptable.
   * **Eliminar** - Toque o haga clic para eliminar la opción de un botón de radio .
   * **Reorganizar** - Toque o haga clic y arrastre para reorganizar el orden de las opciones.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.

* **Tipo de datos del valor enviado** - Esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si la variable **tipo de datos del valor enviado** está configurado como `Number` y se agregan datos de cadena a **Valor de datos** &#x200B; de &#x200B; en el **Opciones** , la pantalla muestra un `Value type mismatch` mensaje de error.

* **Opciones predeterminadas** - Esta opción le permite agregar valores predeterminados que están preseleccionados cuando se carga el formulario. Si la variable **tipo de datos del valor enviado** está configurado como `Number` y se agregan datos de cadena a **Opciones predeterminadas**, la pantalla muestra un `Value type mismatch` mensaje de error.

* **Opciones de visualización** - Esta opción se utiliza para definir la alineación visual de los botones de radio en un formulario adaptable. Las dos opciones admitidas son:
   * **Horizontal** - Cuando se selecciona esta opción, los botones de opción se muestran de izquierda a derecha en un formulario adaptable.
   * **Vertical** - Cuando se selecciona esta opción, los botones de opción se muestran de arriba a abajo en un formulario adaptable.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/radiobutton_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo de formulario se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Ficha Contenido de ayuda {#helpcontent-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/radiobutton_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Botón de radio.


### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal del botón de radio adaptable de Forms es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del botón de radio adaptable de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

