---
title: 'Componente principal de Forms adaptable: entrada de texto (cuadro de texto)'
description: Uso o personalización del componente principal de entrada de texto adaptable de Forms.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1750'
ht-degree: 1%

---

# Entrada de texto (cuadro de texto) {#text-input-adaptive-forms-core-component}

Un componente de entrada de texto (cuadro de texto) permite al usuario introducir y editar una o varias líneas de texto, según el atributo de tipo del elemento de entrada. El componente de entrada de texto puede colocarse dentro de un formulario y generalmente se etiqueta con un texto útil que identifica fácilmente su propósito. Se trata de un elemento fundamental de cualquier formulario, que se utiliza ampliamente para recopilar distintos tipos de datos de los usuarios, son sencillos, flexibles y se pueden configurar para validar entradas, mejorar la precisión de la recopilación de datos.


**Ejemplo**

![](/help/adaptive-forms/assets/text-input.png)


## Uso {#reasons-to-use-text-input-field}

Existen varias razones para utilizar el componente de entrada de texto en un formulario adaptable:

* **Recopilación de datos**: Los campos de entrada de texto son uno de los elementos de formulario más comunes que se utilizan para recopilar una amplia gama de información de los usuarios, como nombres, direcciones de correo electrónico, números de teléfono y otros tipos de datos de texto.

* **Fácil de usar**: Los campos de entrada de texto son sencillos y fáciles de usar, lo que facilita a los usuarios la introducción y edición de texto.

* **Flexibilidad**: Los campos de entrada de texto se pueden utilizar para recopilar una amplia gama de información, desde entradas de texto cortas de una sola línea hasta entradas de texto multilínea más largas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del acordeón de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posterior. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posterior |
|---|---|---|
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/adaptive-forms/version.md) y posterior | Compatible con<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posterior pero inferior a 2.0.0. |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre las fichas de Forms adaptables en el componente principal principal principal en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de texto para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de entrada de texto con facilidad para una experiencia de usuario perfecta.

![Ficha básica](/help/adaptive-forms/assets/textinput_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición** : el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.

* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Valor predeterminado** - Esta opción le permite agregar un valor predeterminado en un campo de formulario. El texto desaparece cuando el usuario empieza a escribir en el campo. If **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla . Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

* **Permitir líneas múltiples** - Esta opción permite al usuario introducir varias líneas en un campo de formulario.

* **Permitir texto enriquecido** - El cuadro de diálogo de edición proporciona herramientas de formato de texto enriquecido estándar que permiten al usuario dar formato al texto.

* **Atributo de relleno automático** - La opción Rellenar automáticamente rellena los campos del formulario según un patrón o texto introducido previamente. Cuando el usuario empieza a escribir texto en el campo de formulario, las sugerencias aparecen en una lista desplegable desde la que puede seleccionar la opción adecuada.

### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/textinput_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número máximo de caracteres** - Esta opción le permite especificar el número máximo de caracteres permitidos en el componente. Si introduce caracteres buenos que no sean el valor especificado en **Número máximo de caracteres**, aparece un mensaje de error en la pantalla . La variable **Mensaje de error máximo de caracteres** permite agregar un mensaje de error personalizado.

* **Mensaje de error máximo de caracteres** - El **Mensaje de error máximo de caracteres** El cuadro de diálogo le permite agregar un mensaje de error personalizado si introduce caracteres buenos que no sean el valor especificado en **Número máximo de caracteres** .

* **Número mínimo de caracteres** - Esta opción le permite especificar el número mínimo de caracteres permitidos en el campo . Si introduce caracteres inferiores al valor especificado en **Número mínimo de caracteres**, aparece un mensaje de error en la pantalla . La variable **Mensaje de error de caracteres mínimos** permite agregar un mensaje de error personalizado.

* **Mensaje de error de caracteres mínimos** - El **Mensaje de error de caracteres mínimos** El cuadro de diálogo le permite agregar un mensaje de error personalizado si introduce caracteres menores que el valor especificado en la variable **Número mínimo de caracteres** .

La variable **Patrón de validación** permite introducir un patrón para validar el texto introducido. En caso de que el texto no se valide con el valor introducido en **Patrón** , el mensaje de error aparece en pantalla.

* **Patrón** - Esta opción le permite introducir los patrones de verificación permitidos para el texto. También se permiten expresiones regulares.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra en la pantalla si el texto introducido no se valida con el valor introducido en la variable **Patrón** option

### Ficha Contenido de ayuda {#help-content-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/textinput_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

**Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Cuadro de texto.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar los estilos CSS de un componente. El cuadro Texto adaptable de Forms Componente principal es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del cuadro de texto adaptable de Forms.

* **Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

### Ficha Formatos {#format-tab}

La pestaña format permite especificar formatos de número predeterminados y personalizados.

![Ficha Formato](/help/adaptive-forms/assets/telephoneinput_format.png)

