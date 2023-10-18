---
title: 'Componente principal de formularios adaptables: entrada de texto (cuadro de texto)'
description: Uso o personalización del componente principal de entrada de texto de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 100%

---

# Entrada de texto (cuadro de texto) {#text-input-adaptive-forms-core-component}

Un componente de entrada de texto (cuadro de texto) permite al usuario introducir y editar una o varias líneas de texto, según el atributo de tipo del elemento de entrada. El componente de entrada de texto puede colocarse dentro de un formulario y generalmente se etiqueta con un texto útil que identifica fácilmente su propósito. Se trata de un elemento fundamental de cualquier formulario, que se emplea ampliamente para recopilar distintos tipos de datos de los usuarios. Son sencillos, flexibles y se pueden configurar para validar entradas y mejorar la precisión de la recopilación de datos.


**Ejemplo**

![](/help/adaptive-forms/assets/text-input.png)


## Uso {#reasons-to-use-text-input-field}

Existen varias razones para utilizar el componente de entrada de texto en un formulario adaptable:

* **Recopilación de datos**: los campos de entrada de texto son uno de los elementos de formulario más comunes que se utilizan para recopilar una amplia gama de información de los usuarios, como nombres, direcciones de correo electrónico, números de teléfono y otros tipos de datos de texto.

* **Fácil de usar**: los campos de entrada de texto son sencillos y sencillos de usar, lo que facilita a los usuarios la introducción y edición de texto.

* **Flexibilidad**: los campos de entrada de texto se pueden usar para recopilar una amplia gama de información, desde entradas de texto cortas de una sola línea hasta entradas multilínea más largas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de pestañas de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de texto para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de entrada de texto con facilidad para una experiencia del usuario perfecta.

![Pestaña Básicos](/help/adaptive-forms/assets/textinput_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Valor predeterminado**: esta opción le permite agregar un valor predeterminado en un campo de formulario. El texto desaparece cuando el usuario empieza a escribir en el campo. Si se selecciona **Componente desactivado** o **Componente de solo lectura**, aparece en pantalla el valor predeterminado. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento de envío del formulario.

* **Permitir líneas múltiples**: esta opción permite al usuario introducir varias líneas en un campo de formulario.

* **Permitir texto enriquecido**: el cuadro de diálogo de edición proporciona herramientas de formato de texto enriquecido estándar que permiten al usuario dar formato al texto.

* **Atributo de rellenado automático**: la opción de rellenado automático rellena los campos del formulario según un patrón o texto introducido previamente. Cuando el usuario empieza a escribir texto en el campo de formulario, las sugerencias aparecen en una lista desplegable desde la que puede seleccionar la opción adecuada.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/textinput_validationtab.png)

* **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básico** cuando se selecciona esta opción.

* **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo se deja en blanco.

* **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número máximo de caracteres**: esta opción le permite especificar el número máximo de caracteres permitidos en el componente. Si introduce caracteres superiores al valor especificado en **Número máximo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado.

* **Mensaje de error de número máximo de caracteres**: el cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado si introduce más caracteres que el valor especificado en **Número máximo de caracteres**.

* **Número mínimo de caracteres**: esta opción permite especificar el número mínimo de caracteres permitidos en el campo. Si introduce menos caracteres que el valor especificado en **Número mínimo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número mínimo de caracteres** permite añadir un mensaje de error personalizado.

* **Mensaje de error de caracteres mínimos**: el cuadro de diálogo **Mensaje de error de caracteres mínimos** permite añadir un mensaje de error personalizado si se introducen caracteres inferiores al valor especificado en la opción **Número mínimo de caracteres**.

La opción **Patrón de validación** permite introducir un patrón para validar el texto introducido. En caso de que el texto no se valide con el valor introducido en la opción **Patrón**, aparece el mensaje de error en pantalla.

* **Patrón**: esta opción le permite introducir los patrones de verificación permitidos para el texto. También se permiten expresiones regulares.

* **Mensaje de error**: esta opción permite introducir un mensaje que se muestra en pantalla si el texto introducido no se valida con el valor introducido en la opción **Patrón**.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/textinput_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de cuadro de texto.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de cuadro de texto de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de cuadro de texto de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Formatos {#format-tab}

La pestaña Formatos permite especificar formatos de número predeterminados y personalizados.

![Pestaña Formato](/help/adaptive-forms/assets/telephoneinput_format.png)


## Artículo relacionado {#related-article}

* [Creación de un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=es)

* [Creación de un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)


>[!MORELIKETHIS]
>
>* [Acordeón](/help/adaptive-forms/components/accordion.md)
>* [Botón](/help/adaptive-forms/components/button.md)
>* [Grupo de casillas de verificación](/help/adaptive-forms/components/checkbox-group.md)
>* [Selector de fecha](/help/adaptive-forms/components/date-picker.md)
>* [Lista desplegable](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de correo electrónico](/help/adaptive-forms/components/email-input.md)
>* [Contenedor del formulario](/help/adaptive-forms/components/form-container.md)
>* [Archivo adjunto](/help/adaptive-forms/components/file-attachment.md)
>* [Pie de página](/help/adaptive-forms/components/footer.md)
>* [Encabezado](/help/adaptive-forms/components/header.md)
>* [Pestañas horizontales](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagen](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Contenedor de panel](/help/adaptive-forms/components/panel-container.md)
>* [Botón de opción](/help/adaptive-forms/components/radio-button.md)
>* [Botón Restablecer](/help/adaptive-forms/components/reset-button.md)
>* [Botón Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de teléfono](/help/adaptive-forms/components/telephone-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Asistente](/help/adaptive-forms/components/wizard.md)

## Vea también {#see-also}

{{see-also}}