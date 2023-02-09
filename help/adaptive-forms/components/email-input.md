---
title: 'Componente principal de Forms adaptable: entrada de correo electrónico'
description: Uso o personalización del componente principal de entrada de correo electrónico adaptable de Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1776'
ht-degree: 1%

---


# Entrada de correo electrónico {#Email-input-adaptive-forms-core-component}

El componente principal de entrada de correo electrónico de formulario adaptable se utiliza para recopilar direcciones de correo electrónico de los usuarios. El campo de entrada de correo electrónico permite al explorador validar que los datos introducidos son un formato de dirección de correo electrónico válido. Generalmente se representa como un cuadro de texto y tiene validaciones de patrones para aceptar solo direcciones de correo electrónico válidas. El campo de entrada de correo electrónico se puede personalizar aún más con atributos adicionales como &quot;requerido&quot;, &quot;marcador de posición&quot; y &quot;patrón&quot; para establecer las validaciones de los datos de entrada.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Existen varias razones por las que resulta beneficioso incluir un componente de entrada de correo electrónico en un formulario adaptable, incluidas:

* **Conveniencia del usuario**: Una entrada de correo electrónico facilita a los usuarios la introducción de sus direcciones de correo electrónico, ya que proporciona una indicación clara de los datos esperados en el campo.

* **Comunicación personalizada**: La recopilación de direcciones de correo electrónico de los usuarios a través de un formulario permite una comunicación personalizada, como el envío de correos electrónicos de confirmación o boletines.

* **Generación de posibles clientes**: Recopilando direcciones de correo electrónico a través de un formulario, las empresas pueden crear su lista de correo electrónico y utilizarla para la generación de posibles clientes.

* **Autenticación de usuarios**: Las direcciones de correo electrónico se pueden utilizar como medio de autenticación para acceder a contenido o servicios restringidos.

* **Recopilación de comentarios**: Una entrada de correo electrónico en un formulario de comentarios permite a la empresa comunicarse con el usuario para realizar un seguimiento o aclarar sus comentarios.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de entrada de correo electrónico de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad de AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de la entrada de correo electrónico adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de correo electrónico para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de entrada de correo electrónico con facilidad para una experiencia de usuario perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/email_basictab.png)

* **Nombre** - El nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición** : el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Valor predeterminado** - Esta opción le permite agregar un valor predeterminado en un campo de formulario. If **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla . Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.


### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/email_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo de formulario se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número máximo de caracteres** - Esta opción le permite especificar el número máximo de caracteres permitidos en el campo. Si introduce caracteres buenos que no sean el valor especificado en **Número máximo de caracteres**, aparece un mensaje de error en la pantalla . La variable **Mensaje de error máximo de caracteres** permite agregar un mensaje de error personalizado.

* **Mensaje de error máximo de caracteres** - El **Mensaje de error máximo de caracteres** El cuadro de diálogo le permite agregar un mensaje de error personalizado si introduce caracteres buenos que no sean el valor especificado en **Número máximo de caracteres** .

* **Número mínimo de caracteres** - Esta opción le permite especificar el número mínimo de caracteres permitidos en el campo . Si introduce caracteres inferiores al valor especificado en **Número mínimo de caracteres**, aparece un mensaje de error en la pantalla . La variable **Mensaje de error de caracteres mínimos** permite agregar un mensaje de error personalizado.

* **Mensaje de error de caracteres mínimos** - El **Mensaje de error de caracteres mínimos** El cuadro de diálogo le permite agregar un mensaje de error personalizado si introduce caracteres menores que el valor especificado en la variable **Número mínimo de caracteres** .

<br>

    La opción **Patrón de validación** permite introducir un patrón para validar el ID de correo electrónico introducido. Si el ID de correo electrónico no se valida con el valor introducido en la opción **Patrón** , el mensaje de error aparece en pantalla.
    * **Patrón**: esta opción le permite introducir los patrones de verificación permitidos para el correo electrónico. También se permiten expresiones regulares.
    * **Mensaje de error**: Esta opción permite introducir un mensaje que se muestra en la pantalla si el ID de correo electrónico no se valida con el valor introducido en la opción **Patrón**

### Ficha Contenido de ayuda {#help-content-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/email_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/email_accessibilitytab.png)

En el **Accesibilidad** , los valores se establecen para [Accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) etiquetas para el componente. Hay varias opciones disponibles para usar el texto del lector de pantalla:

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.


   * **Texto personalizado**: Seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado . Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   * **Descripción**: Seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   * **Título**: Seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   * **Nombre**: Seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   * **Ninguna**: Seleccione esta opción si no desea agregar para etiquetas de accesibilidad de ARIA.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de entrada Correo electrónico.


### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de entrada de correo electrónico de Forms adaptable es compatible con la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de entrada de correo electrónico adaptable de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

### Ficha Formatos {#format-tab}

La pestaña format permite especificar formatos de fecha predeterminados y personalizados.
