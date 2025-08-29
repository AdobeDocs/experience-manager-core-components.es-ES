---
title: 'Componente principal de Forms adaptable: fecha y hora'
description: Usar o personalizar el componente principal Fecha y hora de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 74%

---


# Componente de fecha y hora

Un componente de fecha y hora de un formulario adaptable es un elemento de interfaz de usuario que permite a los usuarios seleccionar **fecha y hora** mediante una interfaz de calendario y reloj, o introduciendo manualmente valores en un formato específico. Garantiza una entrada precisa y estandarizada para casos de uso en los que tanto la fecha como la hora son esenciales.

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/date-time-picker.png)

## Uso {#reasons-to-use-date-time-picker}

Existen varias razones por las que es beneficioso incluir un selector de fecha y hora en un formulario, entre ellas:

- **Comodidad**: permite a los usuarios elegir fácilmente una fecha y una hora sin necesidad de escribir valores manualmente.
- **Coherencia**: Aplica un formato estándar para las entradas de fecha y hora en todo el formulario.
- **Experiencia del usuario mejorada**: Proporciona una interfaz de usuario intuitiva con selectores de calendario y hora.
- **Programación de eventos**: útil en la reserva de citas, entrevistas o formularios de programación de reuniones.
- **Viajes y reservas**: permite a los usuarios seleccionar las fechas y horas de llegada y salida.
- **Precisión de datos**: reduce los errores de entrada en comparación con la entrada de texto libre.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Fecha y hora de Forms adaptable se publicó en **agosto de 2025** como parte de **Componentes principales 2.24.6** para Cloud Service y versiones posteriores.

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| v1 | Compatible con la <br>[versión 2.24.6](/help/adaptive-forms/version.md) y posteriores | |

Para obtener más información sobre las versiones, consulte [Versiones de componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga los detalles técnicos más recientes sobre el componente principal Fecha y hora de Forms adaptable en [GitHub](https://github.com/adobe/aem-core-forms-components). Para obtener más información sobre el desarrollo de componentes principales, consulte [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite personalizar la fecha y la hora.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/datetime_basictab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: el título es una cadena que aparece en la parte superior de un componente en un Formulario adaptable. El título identifica de forma exclusiva el componente en la estructura de árbol de un formulario adaptable. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione esta opción para ocultar el título del tipo de componente en un Formulario adaptable.

- **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o indicación corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Fecha y hora predeterminadas**: esta opción le permite agregar una fecha y una hora al campo de formulario. La fecha introducida aparece de forma predeterminada en el lugar del componente. Si el usuario no introduce ninguna fecha u hora, este valor se envía en el momento del envío del formulario. En caso de que se seleccione **Componente deshabilitado** o **Componente de solo lectura**, la fecha y la hora predeterminadas se mostrarán en la pantalla y se enviarán en el momento del envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/datetime_validation.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básicos** cuando esta opción está seleccionada.

- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo del formulario se deja en blanco.

- **Mensaje de validación de la secuencia de comandos**: esta opción permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

- **Fecha mínima**: esta opción permite introducir la fecha mínima requerida. Si introduce una fecha anterior a la especificada en Fecha y hora mínimas, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error mínimo** permite añadir un mensaje de error personalizado.

- **Mensaje de error mínimo** - El cuadro de diálogo **Mensaje de error mínimo** le permite agregar un mensaje de error personalizado para que se muestre si escribe una fecha u hora anterior a la fecha u hora especificada en la opción **Fecha mínima**.

- **Fecha máxima**: esta opción le permite especificar la fecha y la hora máximas requeridas. Si introduce una fecha u hora posterior a la especificada en Fecha máxima, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error máximo** permite añadir un mensaje de error personalizado.

- **Mensaje de error máximo** - El cuadro de diálogo **Mensaje de error máximo** le permite agregar un mensaje de error personalizado para que se muestre si escribe una fecha u hora posterior a la fecha u hora especificada en la opción **Fecha máxima**.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/datetime_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarle a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.


### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Fecha y hora.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de fecha y hora de Forms adaptable es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de fecha y hora de Forms adaptable.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/datepicker_customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}


