---
title: 'Componente principal de formularios adaptables: entrada de texto (cuadro de texto)'
description: Uso o personalización del componente principal de entrada de texto de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 49d9fe69-0578-4489-beaa-a18cdb14add7
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2120'
ht-degree: 100%

---


# Componente Cuadro de texto{#text-input-adaptive-forms-core-component}

Un componente de entrada de texto (cuadro de texto) permite al usuario introducir y editar una o varias líneas de texto, según el atributo de tipo del elemento de entrada. El componente de entrada de texto puede colocarse dentro de un formulario y generalmente se etiqueta con un texto útil que identifica fácilmente su propósito. Se trata de un elemento fundamental de cualquier formulario, que se emplea ampliamente para recopilar distintos tipos de datos de los usuarios. Son sencillos, flexibles y se pueden configurar para validar entradas y mejorar la precisión de la recopilación de datos.

{{traditional-aem}}

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/text-input.png)


## Uso {#reasons-to-use-text-input-field}

Existen varias razones para utilizar el componente de entrada de texto en un formulario adaptable:

- **Recopilación de datos**: los campos de entrada de texto son uno de los elementos de formulario más comunes que se utilizan para recopilar una amplia gama de información de los usuarios, como nombres, direcciones de correo electrónico, números de teléfono y otros tipos de datos de texto.

- **Fácil de usar**: los campos de entrada de texto son sencillos y sencillos de usar, lo que facilita a los usuarios la introducción y edición de texto.

- **Flexibilidad**: los campos de entrada de texto se pueden usar para recopilar una amplia gama de información, desde entradas de texto cortas de una sola línea hasta entradas multilínea más largas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del cuadro de texto de los formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y los componentes principales 1.1.12 para AEM 6.5.16.0 Forms o versiones posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_es). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de cuadro de texto de los formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de texto para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de entrada de texto con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/textinput_basictab.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Valor predeterminado**: esta opción le permite agregar un valor predeterminado en un campo de formulario. El texto desaparece cuando el usuario empieza a escribir en el campo. Si se selecciona **Componente desactivado** o **Componente de solo lectura**, aparece en pantalla el valor predeterminado. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

- **Permitir líneas múltiples**: esta opción permite al usuario introducir varias líneas en un campo de formulario.

- **Atributo de relleno automático**: la opción permite a los usuarios introducir un valor que se rellena automáticamente dentro del campo de formulario en función de la información almacenada.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/textinput_validationtab.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe introducir un valor antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

- **Número máximo de caracteres**: esta opción le permite especificar el número máximo de caracteres permitidos en el componente. Si introduce caracteres superiores al valor especificado en **Número máximo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado.

- **Mensaje de error de número máximo de caracteres**: el cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado si introduce más caracteres que el valor especificado en **Número máximo de caracteres**.

- **Número mínimo de caracteres**: esta opción permite especificar el número mínimo de caracteres permitidos en el campo. Si introduce menos caracteres que el valor especificado en **Número mínimo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número mínimo de caracteres** permite añadir un mensaje de error personalizado.

- **Mensaje de error de caracteres mínimos**: el cuadro de diálogo **Mensaje de error de caracteres mínimos** permite añadir un mensaje de error personalizado si se introducen caracteres inferiores al valor especificado en la opción **Número mínimo de caracteres**.

La opción **Patrón de validación** permite introducir un patrón para validar el texto introducido. En caso de que el texto no se valide con el valor introducido en la opción **Patrón**, aparece el mensaje de error en pantalla.

- **Patrón**: esta opción le permite introducir los patrones de verificación permitidos para el texto. También se permiten expresiones regulares.

- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra en pantalla si el texto introducido no se valida con el valor introducido en la opción **Patrón**

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/textinput_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/textinput_accessibiltytab.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de cuadro de texto.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de cuadro de texto de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal Cuadro de texto de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/datepicker_customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

### Pestaña Formatos {#formats-tab}

La pestaña Formatos permite especificar formatos de fecha predeterminados y personalizados.

![Pestaña Formato](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
