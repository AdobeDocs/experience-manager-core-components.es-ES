---
title: 'Componente principal de Formularios adaptables: selector de fecha'
description: Uso o personalización del componente principal de selector de fecha de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2154'
ht-degree: 99%

---

# Componente de selector de fechas{#date-picker-adaptive-forms-core-component}

Un componente de selector de fecha de un Formulario adaptable es un elemento de la interfaz de usuario que permite a los usuarios seleccionar una fecha de un calendario o introduciendo manualmente una fecha en un formato específico. El componente de selector de fecha se puede configurar para que tenga valores de formato, validación y predeterminados diferentes.

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/date-picker.png)

## Uso {#reasons-to-use-drop-date-picker}

Existen varias razones por las que resulta beneficioso incluir un selector de fecha en un Formulario adaptable, entre ellas, las siguientes:

- **Comodidad**: un componente de selector de fecha permite a los usuarios seleccionar fácilmente una fecha de un calendario sin tener que introducirla manualmente un campo de texto. Esto puede ahorrar tiempo y reducir errores.

- **Experiencia del usuario**: el componente de selector de fecha se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva para que los usuarios seleccionen la fecha.

- **Análisis de datos**: el componente de selector de fecha se puede utilizar para recopilar datos de varias fuentes y analizarlos, o para utilizarlos como entrada para un procesamiento posterior.

- **Administración de eventos**: el componente de selector de fecha se puede utilizar en sitios web de administración de eventos para seleccionar la fecha del evento.

- **Reservas**: el componente de selector de fecha se puede utilizar en los sitios web de reservas para seleccionar las fechas de entrada y salida.

- **Formato de fecha**: el componente de selector de fecha se puede utilizar para corregir el formato en el que se muestra e introduce la fecha. Asegúrese de que el formato de fecha sea uniforme en todo el formulario para garantizar que la experiencia de usuario sea consistente.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de selector de fecha de Formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del selector de fecha para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de selector de fecha con facilidad para que el usuario disfrute de una experiencia óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/datepicker_basictab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: el título es una cadena que aparece en la parte superior de un componente en un Formulario adaptable. El título identifica de forma exclusiva el componente en la estructura de árbol de un formulario adaptable. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione esta opción para ocultar el título del tipo de componente en un Formulario adaptable.

- **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.
- **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Fecha predeterminada**: esta opción permite añadir una fecha al campo del formulario. La fecha introducida aparece de forma predeterminada en el lugar del componente. Si el usuario no introduce ninguna fecha, este valor se envía en el momento del envío del formulario. En caso de que se seleccione **Componente desactivado** o **Componente de solo lectura**, la fecha predeterminada se muestra en la pantalla y se envía en el momento del envío del formulario.


### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/datepicker_validation.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básicos** cuando esta opción está seleccionada.

- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo del formulario se deja en blanco.

- **Mensaje de validación de la secuencia de comandos**: esta opción permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

- **Fecha mínima**: esta opción permite introducir la fecha mínima requerida. Si introduce una fecha anterior a la fecha especificada en Fecha mínima, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error mínimo** permite añadir un mensaje de error personalizado.

- **Mensaje de error mínimo**: el cuadro de diálogo **Mensaje de error mínimo** permite añadir un mensaje de error personalizado para mostrar, si introduce una fecha anterior a la fecha especificada en la opción **Fecha mínima**.
- **Excluir fecha mínima**: esta opción permite omitir la fecha mínima en un intervalo o conjunto de fechas determinados.

- **Fecha máxima**: esta opción permite introducir la fecha máxima requerida. Si introduce una fecha posterior a la fecha especificada en Fecha máxima, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error máximo** permite añadir un mensaje de error personalizado.

- **Mensaje de error máximo**: el cuadro de diálogo **Mensaje de error máximo** permite añadir un mensaje de error personalizado para mostrar, si introduce una fecha posterior a la fecha especificada en la opción **Fecha máxima**.

- **Excluir fecha máxima**: esta opción permite omitir la fecha máxima en un intervalo o conjunto de fechas determinados.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarle a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.


### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

### Pestaña Formatos {#format-tab}

![Pestaña Formatos](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Formato de visualización**: representa el formato de fecha que se muestra al usuario. La opción **Tipo** permite al usuario seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la opción **Personalizado** en el menú desplegable **Tipo**.

- **Editar formato**: representa un formato de fecha en el que el usuario puede editar la fecha. La opción **Tipo** permite seleccionar el formato de fecha. También puede personalizar el formato de fecha utilizando la opción **Personalizado** en el menú desplegable **Tipo**.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente de selector de fechas.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de selector de fecha de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilo](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de selector de fecha de Formularios adaptables.

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

![Pestaña Formato](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}


