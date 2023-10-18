---
title: 'Componente principal de formularios adaptables: grupo de casillas de verificación'
description: Uso o personalización del componente principal del grupo de casillas de verificación de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
source-git-commit: 0026734a2e43c51c7f5af2b37492d61e8f779ac7
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 100%

---

# Grupo de casillas de verificación {#button-component-adaptive-forms-core-component}

Un grupo de casillas de verificación de un formulario adaptable es un conjunto de casillas de verificación relacionadas que permiten a los usuarios seleccionar una o más opciones de una lista. Cada casilla de verificación está representada por un valor de datos (valor utilizado para procesar elementos de un grupo de casillas de verificación) y un valor de visualización (etiqueta para cada elemento de casilla de verificación que describe su propósito).

**Ejemplo**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Cuadro de diálogo Propiedades**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

En este ejemplo, el elemento Opciones se utiliza para agrupar las casillas de verificación. El elemento **Mostrar texto** se utiliza para proporcionar una etiqueta para un elemento y **Valor de datos** se utiliza para especificar el valor que se envía al servidor cuando se envía el formulario.

Cada opción o elemento de casilla de verificación tiene un valor de datos único y un atributo de texto de visualización. Si un usuario selecciona las casillas de verificación “Hijo” e “Hija”, el valor de datos correspondiente se envía al servidor cuando se envía el formulario. Estos datos se pueden procesar mediante una secuencia de comandos del lado del servidor para determinar qué opciones ha seleccionado el usuario y se pueden utilizar para realizar diversas acciones, como actualizar otros campos del formulario o enviar los datos del formulario a una secuencia de comandos del lado del servidor para un procesamiento posterior.

Además, el grupo de casillas de verificación se puede configurar para que tenga valores de procesamiento diferentes para cada opción, y esto se puede definir mediante el Editor de reglas de los formularios adaptables.

## Uso {#reasons-to-use-check-box-group}

Existen varias razones por las que resulta beneficioso incluir un grupo de casillas de verificación en un formulario adaptable, entre ellas:

* **Múltiples selecciones**: un grupo de casillas de verificación permite a los usuarios seleccionar varias opciones de una lista, lo que puede resultar útil en situaciones en las que se permiten o requieren varias selecciones.

* **Experiencia del usuario**: el grupo de casillas de verificación se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva para que los usuarios seleccionen varias opciones.

* **Análisis de datos**: el grupo de casillas de verificación se puede utilizar para recopilar datos de varias fuentes y analizarlos, o para utilizarlos como entrada para un procesamiento posterior.

* **Encuestas**: el grupo de casillas de verificación se puede utilizar en encuestas para seleccionar varias opciones para una pregunta.

* **Preferencias de usuario**: el grupo de casillas de verificación se puede utilizar para recopilar las preferencias de usuario para las distintas opciones.

* **Valor de datos**: el grupo de casillas de verificación también se puede utilizar para procesar elementos de un grupo de casillas de verificación.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal Grupo de casillas de verificación de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las casillas de verificación para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones de casilla de verificación con facilidad para que la experiencia del usuario sea óptima.


### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece encima del componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Opciones**: puede agregar valores de datos y mostrar pares de texto utilizando el botón **Agregar**. Una vez agregada una nueva opción, se pueden realizar las acciones siguientes:

   * **Valor de datos**: esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   * **Mostrar texto**: esta opción permite introducir el contenido que se mostrará en el formulario adaptable.
   * **Eliminar**: pulse o haga clic para eliminar la opción de una casilla de verificación.
   * **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

* **Tipo de datos del valor enviado**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra un mensaje de error `Value type mismatch`.

* **Opciones de visualización**: esta opción se utiliza para establecer la alineación visual de las casillas de verificación en un formulario adaptable. Las dos opciones compatibles son las siguientes:
   * **Horizontal**: cuando se selecciona esta opción, las casillas de verificación se muestran de izquierda a derecha en un formulario adaptable.
   * **Vertical**: cuando se selecciona esta opción, las casillas de verificación se muestran de arriba a abajo en un formulario adaptable.

* **Opciones predeterminadas**: esta opción le permite agregar valores predeterminados preseleccionados cuando se carga el formulario. Utilice el icono eliminar para eliminar las opciones añadidas. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Opciones predeterminadas**, la pantalla muestra un mensaje de error `Value type mismatch`.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

* **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

* **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/checkbox_accessibility.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

    ## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se emplea para definir y administrar estilos CSS para el componente de grupo de casillas de verificación.

### Pestaña Estilos {#styles-tab}

El componente principal de grupo de casillas de verificación de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de grupo de casillas de verificación de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

>[!MORELIKETHIS]
>
>* [Acordeón](/help/adaptive-forms/components/accordion.md)
>* [Botón](/help/adaptive-forms/components/button.md)
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
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Asistente](/help/adaptive-forms/components/wizard.md)

## Vea también {#see-also}

{{see-also}}