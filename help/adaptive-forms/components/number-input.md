---
title: 'Componente principal de formularios adaptables: entrada de número'
description: Uso o personalización del componente principal de entrada de número de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 98%

---

# Entrada de número {#number-input-adaptive-forms-core-component}

Un componente de Entrada de número de un Formulario adaptable es un tipo de campo de formulario que permite a los usuarios introducir valores numéricos. El componente se suele representar mediante un campo de texto con una flecha hacia arriba y hacia abajo para incrementar y reducir el número.

También se puede utilizar con atributos como mín., máx., paso, valor, etc. Estos atributos se pueden utilizar para establecer los valores mínimo y máximo permitidos en el campo, el intervalo de paso para incrementar o reducir el número y el valor predeterminado del campo.

Este componente se puede utilizar para recopilar datos numéricos como la edad, cantidad, etc. También se puede usar para realizar operaciones matemáticas como sumas y restas. Este componente también se puede utilizar para validar los datos numéricos introducidos por el usuario.

Para la accesibilidad, es importante especificar “etiqueta” que describe la finalidad del campo de entrada de número y qué tipo de entrada se espera.

**Ejemplo**

![](/help/adaptive-forms/assets/numeric-stepper.png)

## Uso {#reasons-to-use-number-input-numeric-stepper}

Existen varias razones por las que resulta beneficioso incluir un componente de entrada numérico en un Formulario adaptable, entre ellas, las siguientes:

* **Operaciones matemáticas**: los campos numéricos se pueden utilizar para realizar operaciones matemáticas como sumas, restas, multiplicaciones y divisiones.

* **Intervalo de datos**: los campos numéricos pueden utilizarse para establecer un rango de valores válidos mediante los atributos mín., máx. y paso.

* **Contenido dinámico**: el componente numérico se puede utilizar para mostrar datos dinámicos basados en los campos del formulario.


## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de entrada de número de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de números para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de entrada numérica con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/numberinput_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Tipo de número**: esta opción permite seleccionar el tipo de valores numéricos permitidos en el campo del formulario. Puede seleccionar los tipos Decimal o Entero en el menú desplegable.
* **Valor predeterminado**: esta opción le permite agregar un valor predeterminado en un campo de formulario. Si **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/numberinput_validationtab.png)

* **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básico** cuando se selecciona esta opción.

* **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo se deja en blanco.

* **Mensaje de validación de la secuencia de comandos**: esta opción le permite escribir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número más bajo/número más pequeño**: utilice esta opción para seleccionar el número mínimo permitido que se debe introducir en el campo de formulario. Si el valor más pequeño que el número especificado en la opción **Número menor/número más pequeño** se introduce en el campo de formulario, aparece el mensaje de error.

* **Mensaje de error mínimo**: esta opción le permite introducir un mensaje de error que se muestra cuando el usuario introduce un valor menor que el valor especificado en la opción **Número mínimo/número mínimo**.

* **Excluir valor mínimo**: seleccione esta casilla de verificación si no desea que el valor mínimo especificado en la opción **Número más bajo/número más pequeño** se incluya en el rango de valores que se introducirá en el campo de formulario.

* **Número más alto/Número mayor**: utilice esta opción para seleccionar el número máximo permitido que se debe introducir en el campo de formulario. Si el número mayor que el especificado en la opción **Número más alto/Número mayor** se introduce en el campo de formulario, aparece el mensaje de error.

* **Mensaje de error máximo**: esta opción le permite introducir un mensaje de error que se muestra cuando el usuario introduce un valor más alto que el especificado en **Número más alto/Número mayor**.

* **Excluir valor máximo**: seleccione esta casilla de verificación si no desea que el valor máximo especificado en la opción **Número más alto/Número más grande** se incluya en el rango de valores que se van a introducir en el campo de formulario.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/numberinput_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/numberinput_accessibility.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

### Pestaña Formatos {#formats-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/numberinput_formattab.png)

* **Formato de visualización**: esta opción le permite seleccionar la opción de diferentes formatos numéricos enteros para su visualización. Cuando el usuario selecciona cualquier opción del menú desplegable **Tipo**, la variable **Formato** aparece en el panel. Puede elegir un formato específico en el que se muestren los números al usuario.

* **Número de dígitos antes del separador decimal (1234.000)**: utilice esta opción para especificar el número de dígitos que se mostrarán antes del punto decimal.

* **Número de dígitos después del separador decimal (1234.000)**: utilice esta opción para especificar el número de dígitos que se mostrarán después del punto decimal.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de entrada de número.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de entrada de número de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

**Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de entrada del número de formularios adaptables.

**Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en formularios adaptables. Para aplicar un estilo, en el editor de formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que quiera en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Formatos {#format-tab}

La pestaña Formatos permite especificar formatos de número predeterminados y personalizados.
![Pestaña Diseño](/help/adaptive-forms/assets/emailinput_designformattab.png)

## Artículo relacionado {#related-article}

* [Crear un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Crear un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)
