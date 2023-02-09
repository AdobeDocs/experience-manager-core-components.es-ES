---
title: 'Componente principal de Forms adaptable: selector de fechas'
description: Uso o personalización del componente principal del selector de fechas de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 1%

---


# Selector de fecha {#date-picker-adaptive-forms-core-component}

Un componente selector de fechas de un formulario adaptable es un elemento de la interfaz de usuario que permite a los usuarios seleccionar una fecha de un calendario o introduciendo manualmente una fecha en un formato específico. El componente del selector de fechas se puede configurar para que tenga valores predeterminados, de validación y de formato diferentes.

**Ejemplo**

![](/help/adaptive-forms/assets/date-picker.png)

## Uso {#reasons-to-use-drop-date-picker}

Existen varias razones por las que resulta beneficioso incluir un selector de fechas en un formulario adaptable, entre ellas:

* **Conveniencia**: Un componente selector de fechas permite a los usuarios seleccionar fácilmente una fecha de un calendario sin tener que introducir manualmente la fecha en un campo de texto. Esto puede ahorrar tiempo y reducir los errores.

* **Experiencia del usuario**: El componente Selector de fecha se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva para que los usuarios seleccionen la fecha.

* **Análisis de datos**: El componente Selector de fecha se puede utilizar para recopilar datos de varias fuentes y analizarlos, o para utilizarlos como entrada para un procesamiento posterior.

* **Gestión de eventos**: El componente Selector de fecha se puede utilizar en sitios web de administración de eventos para seleccionar la fecha del evento.

* **Reservas**: El componente Selector de fecha se puede utilizar en los sitios web de reservas y reservas para seleccionar las fechas de entrada y salida.

* **Formato de fecha**: El componente Selector de fecha se puede utilizar para corregir el formato en el que se muestra e introduce la fecha. Asegúrese de que el formato de fecha sea uniforme en todo el formulario para garantizar una experiencia de usuario uniforme.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del selector de fechas de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del selector de fechas de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del selector de fechas para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones del selector de fechas con facilidad para que la experiencia del usuario sea perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Nombre** : El nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

* **Título** - El título es una cadena que aparece en la parte superior de un componente en un formulario adaptable. El título identifica de forma exclusiva el componente en la estructura de árbol de un formulario adaptable. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione esta opción para ocultar el título del tipo de componente en un formulario adaptable.

* **Texto del marcador de posición** : el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Fecha predeterminada** - Esta opción le permite añadir una fecha al campo de formulario. La fecha introducida aparece de forma predeterminada en el lugar del componente. Si el usuario no introduce ninguna fecha, este valor se envía en el momento del envío del formulario. En el caso **Componente desactivado** o **Componente de solo lectura** está seleccionada, la fecha predeterminada se muestra en la pantalla y se envía en el momento del envío del formulario.


### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/datepicker_validation.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente** en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo de formulario se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Fecha mínima** - Esta opción le permite introducir la fecha mínima requerida. Si introduce una fecha anterior a la fecha especificada en Fecha mínima, aparecerá un mensaje de error en la pantalla. La variable **Mensaje de error mínimo** permite agregar un mensaje de error personalizado.

* **Mensaje de error mínimo** - El **Mensaje de error mínimo** El cuadro de diálogo le permite agregar un mensaje de error personalizado para mostrar, si introduce una fecha anterior a la fecha especificada en la variable **Fecha mínima** .

* **Fecha máxima** - Esta opción le permite introducir la fecha máxima requerida. Si introduce una fecha posterior a la fecha especificada en Fecha máxima, aparece un mensaje de error en la pantalla. La variable **Mensaje de error máximo** permite agregar un mensaje de error personalizado.

* **Mensaje de error máximo** - El **Mensaje de error máximo** El cuadro de diálogo le permite agregar un mensaje de error personalizado para mostrar, si introduce una fecha posterior a la fecha especificada en la variable **Fecha máxima** .


### Ficha Contenido de ayuda {#help-content-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve**- Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.


### Pestaña Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

En el **Accesibilidad** , los valores se establecen para [Accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) etiquetas para el componente. Hay varias opciones disponibles para usar el texto del lector de pantalla:

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.


   * **Texto personalizado**: Seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado . Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   * **Descripción**: Seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   * **Título**: Seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   * **Nombre**: Seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   * **Ninguna**: Seleccione esta opción si no desea agregar para etiquetas de accesibilidad de ARIA.



### Ficha Formatos {#format-tab}

![Ficha Formatos](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Formato de visualización** : representa el formato de fecha que se muestra al usuario. La variable **Tipo** permite al usuario seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la variable **Personalizado** en la **Tipo** menú desplegable.

* **Editar formato** : representa un formato de fecha en el que el usuario puede editar la fecha. La variable **Tipo** permite al usuario seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la variable **Personalizado** en la **Tipo** menú desplegable.

* **Formato de visualización** : representa el formato de fecha que se muestra al usuario. La opción Tipo permite al usuario seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la variable **Personalizado** en la **Tipo** menú desplegable.

* **Editar formato** : representa un formato de fecha en el que el usuario edita la fecha. La opción Tipo permite al usuario seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la variable **Personalizado** en la **Tipo** menú desplegable.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Selector de fechas.


### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal del selector de fechas de Forms adaptable es compatible con la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del selector de fechas de Forms adaptable.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

### Ficha Formatos {#formats-tab}

La pestaña format permite especificar formatos de fecha predeterminados y personalizados.
