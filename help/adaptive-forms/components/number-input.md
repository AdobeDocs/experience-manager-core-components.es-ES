---
title: 'Componente principal de Forms adaptable: entrada de número'
description: Uso o personalización del componente principal de entrada del número de Forms adaptable.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 1%

---

# Entrada de número {#number-input-adaptive-forms-core-component}

Un componente Entrada de número de un formulario adaptable es un tipo de campo de formulario que permite a los usuarios introducir valores numéricos. El componente se representa generalmente mediante un campo de texto con una flecha hacia arriba y hacia abajo para incrementar y reducir el número.

También se puede utilizar con atributos como min, max, step, value, etc. Estos atributos se pueden utilizar para establecer los valores mínimo y máximo permitidos en el campo, el intervalo de paso para incrementar o reducir el número y el valor predeterminado del campo.

Este componente se puede utilizar para recopilar datos numéricos como edad, cantidad, etc. También se puede utilizar para realizar operaciones matemáticas como la suma y la resta. Este componente también se puede utilizar para validar los datos numéricos introducidos por el usuario.

Para la accesibilidad, es importante especificar &quot;etiqueta&quot; que describa el propósito del campo de entrada de número y qué tipo de entrada se espera.

**Ejemplo**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Uso {#reasons-to-use-number-input-numeric-stepper}

Existen varias razones por las que resulta beneficioso incluir un componente de entrada numérico en un formulario adaptable, entre ellas:

* **Operaciones matemáticas**: Los campos numéricos se pueden utilizar para realizar operaciones matemáticas como adición, resta, multiplicación y división.

* **Intervalo de datos**: Los campos numéricos pueden utilizarse para establecer un rango de valores válidos mediante los atributos min, max y step.

* **Contenido dinámico**: El componente numérico se puede utilizar para mostrar datos dinámicos basados en los campos del formulario.


## Versión y compatibilidad {#version-and-compatibility}

El componente principal del acordeón de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posterior. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posterior |
|---|---|---|
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/adaptive-forms/version.md) y posterior | Compatible con<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posterior pero inferior a 2.0.0. |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/adaptive-forms/version.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de entrada del número de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de números para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de entrada numérica con facilidad para una experiencia de usuario perfecta.

### Ficha básica {#basic-tab}

![Ficha básica](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición** : el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Tipo de número** - Esta opción le permite seleccionar el tipo de valores numéricos &#x200B; se permiten en el campo de formulario. Puede seleccionar tipos Decimal o Entero en el menú desplegable.
* **Valor predeterminado** - Esta opción le permite agregar un valor predeterminado en un campo de formulario. If **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla . Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número menor/número más pequeño** - Utilice esta opción para seleccionar el número mínimo permitido que se debe introducir en el campo de formulario. Si el valor es menor que el número especificado en **Número menor/número más pequeño** se introduce en el campo de formulario, aparece el mensaje de error.

* **Mensaje de error mínimo** - Esta opción le permite introducir un mensaje de error que se muestra cuando el usuario introduce un valor menor que el valor especificado en la variable **Número mínimo/número mínimo** .

* **Excluir valor mínimo** - Seleccione esta casilla de verificación si no desea el valor mínimo especificado en la variable **Número menor/número más pequeño** que se incluirá en el rango de valores &#x200B; que se introducirá en el campo de formulario.

* **Número más alto/Número más grande** - Utilice esta opción para seleccionar el número máximo permitido que se debe introducir en el campo de formulario. Si el número es bueno al especificado en **Número más alto/Número más grande** se introduce en el campo de formulario, aparece el mensaje de error.

* **Máximo mensaje de error** - Esta opción le permite introducir un mensaje de error que se muestra cuando el usuario introduce un valor bueno que el especificado en **Número más alto/Número más grande** .

* **Excluir valor máximo** - Seleccione esta casilla de verificación si no desea el valor máximo especificado en la variable **Número más alto/Número más grande** para incluir en el rango de valores que se van a introducir en el campo de formulario.

### Ficha Contenido de ayuda {#help-content}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/numberinput_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Ficha Accesibilidad](/help/adaptive-forms/assets/numberinput_accessibility.png)

**Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está pensado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

### Ficha Formatos {#formats-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/numberinput_formattab.png)

* **Formato de visualización** - Esta opción le permite seleccionar la opción de diferentes formatos numéricos-enteros para la visualización. Cuando el usuario selecciona cualquier opción del **Tipo** menú desplegable, la variable **Formato** se vuelve visible en el panel. Puede elegir un formato específico en el que se muestren los números al usuario.

* **Número de dígitos antes del separador decimal (1234.000)** - Utilice esta opción para especificar el número de dígitos que se mostrarán antes del punto decimal.

* **Número de dígitos después del separador decimal (1234.000)** - Utilice esta opción para especificar el número de dígitos que se mostrarán después del punto decimal.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de entrada Número.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar los estilos CSS de un componente. El componente principal de entrada de Número de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Styletab](/help/adaptive-forms/assets/datepicker_styletab.png)

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de entrada del número de Forms adaptable.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en Forms adaptable . Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el editor del estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

### Ficha Formatos {#format-tab}

La pestaña format permite especificar formatos de número predeterminados y personalizados.
![Ficha Diseño](/help/adaptive-forms/assets/emailinput_designformattab.png)

