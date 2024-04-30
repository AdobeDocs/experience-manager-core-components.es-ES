---
title: 'Componente principal de Formularios adaptables: entrada de correo electrónico'
description: Uso o personalización del componente principal de entrada de correo electrónico de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: ht
source-wordcount: '2054'
ht-degree: 100%

---

# Entrada de correo electrónico {#Email-input-adaptive-forms-core-component}

<span class="preview"> Este artículo incluye contenido sobre la función de **Permitir texto enriquecido en el título**, una función previa al lanzamiento. Solo se puede acceder a la función previa al lanzamiento mediante nuestro [canal previo al lanzamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=es#new-features).</span>

El componente principal de entrada de correo electrónico de Formulario adaptable se utiliza para recopilar direcciones de correo electrónico de los usuarios. El campo de entrada de correo electrónico permite al explorador validar que los datos introducidos tienen un formato de dirección de correo electrónico válida. Se suele representar como un cuadro de texto y tiene validaciones de patrones para aceptar solo direcciones de correo electrónico válidas. El campo de entrada de correo electrónico se puede personalizar aún más con atributos adicionales como “obligatorio”, “marcador de posición” y “patrón” para establecer las validaciones de los datos de entrada.

**Ejemplo**
![ejemplo](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Existen varias razones por las que resulta beneficioso incluir un componente de entrada de correo electrónico en un Formulario adaptable, entre ellas, las siguientes:

- **Comodidad del usuario**: una entrada de correo electrónico facilita a los usuarios la introducción de sus direcciones de correo electrónico, ya que proporciona una indicación clara de los datos previstos en el campo.

- **Comunicación personalizada**: la recopilación de direcciones de correo electrónico de los usuarios a través de un formulario permite una comunicación personalizada, como el envío de correos electrónicos de confirmación o boletines.

- **Generación de posibles clientes**: recopilando direcciones de correo electrónico a través de un formulario, las empresas pueden crear su lista de correo electrónico y utilizarla para la generación de posibles clientes.

- **Autenticación de usuarios**: las direcciones de correo electrónico se pueden utilizar como medio de autenticación para acceder al contenido o a los servicios restringidos.

- **Recopilación de comentarios**: una entrada de correo electrónico en un formulario de comentarios permite a la empresa comunicarse con el usuario para realizar un seguimiento o aclarar sus comentarios.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de entrada de correo electrónico de Formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de correo electrónico para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de entrada de correo electrónico con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/email_basictab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece encima del componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
- **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Valor predeterminado**: esta opción le permite agregar un valor predeterminado en un campo de formulario. Si **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.
- **Atributo de relleno automático**: la opción permite a los usuarios introducir un valor que se rellena automáticamente dentro del campo de formulario en función de la información almacenada.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/email_validationtab.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe introducir un valor antes de continuar con el envío de un formulario. No puede seleccionar la opción **Ocultar componente** o **Deshabilitar componente**  en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

- **Mensaje de validación de la secuencia de comandos**: esta opción le permite escribir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

- **Número máximo de caracteres**: esta opción permite especificar el número máximo de caracteres permitidos en el campo. Si introduce más caracteres que el valor especificado en **Número máximo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado.

- **Mensaje de error de número máximo de caracteres**: el cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado si introduce más caracteres que el valor especificado en **Número máximo de caracteres**.

- **Número mínimo de caracteres**: esta opción permite especificar el número mínimo de caracteres permitidos en el campo. Si introduce menos caracteres que el valor especificado en **Número mínimo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número mínimo de caracteres** permite añadir un mensaje de error personalizado.

- **Mensaje de error del número mínimo de caracteres mínimos**: el cuadro de diálogo **Mensaje de error del número mínimo de caracteres** permite añadir un mensaje de error personalizado si introduce menos caracteres que el valor especificado en la variable **Número mínimo de caracteres**.
<br>

La opción **Patrón de validación** permite introducir un patrón para validar el ID de correo electrónico introducido. Si el ID de correo electrónico no se valida con el valor introducido en la opción **Patrón**, el mensaje de error aparecerá en pantalla.

- **Patrón**: esta opción permite introducir los patrones de verificación permitidos para el correo electrónico. También se permiten expresiones regulares.
- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra en la pantalla si el ID de correo electrónico no se valida con el valor introducido en la opción **Patrón**

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/email_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/email_accessibilitytab.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Entrada de correo electrónico.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de entrada de correo electrónico de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de entrada de correo electrónico de formularios adaptables.

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

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
