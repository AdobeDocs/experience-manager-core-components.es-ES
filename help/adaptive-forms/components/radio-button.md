---
title: 'Componente principal de Formularios adaptables: botón de radio'
description: Uso o personalización del componente principal de botón de radio de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2135'
ht-degree: 98%

---


# Componente Botón de radio {#radio-button-adaptive-forms-core-component}

Un botón de radio de un formulario adaptable es un tipo de elemento de entrada que permite al usuario seleccionar una opción de un grupo de opciones relacionadas. Se representa mediante un pequeño botón circular que está relleno o vacío para indicar si la opción está seleccionada o no. Cuando un usuario selecciona un botón de radio, el resto del grupo deja de estar seleccionado. Los botones de radio suelen utilizarse cuando hay varias opciones mutuamente excluyentes y solo se puede seleccionar una a la vez.

{{traditional-aem}}

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/radio-button.png)

**Cuadro de diálogo Propiedades**

![ejemplo](/help/adaptive-forms/assets/radio-button-properties.png)

En este ejemplo, el elemento Opciones se utiliza para agrupar los botones de radio. El elemento **Mostrar texto** se utiliza para proporcionar una etiqueta para un elemento y **Valor de datos** se utiliza para especificar el valor que se envía al servidor cuando se envía el formulario.

Cada opción de botón de radio tiene un valor de datos y un atributo de texto mostrado. Si un usuario selecciona “1-10”, el valor de datos correspondiente se envía al servidor cuando se envía el formulario. Estos datos se pueden procesar mediante una secuencia de comandos del lado del servidor para determinar qué opciones ha seleccionado el usuario y se pueden utilizar para realizar diversas acciones, como actualizar otros campos del formulario o enviar los datos del formulario a una secuencia de comandos del lado del servidor para un procesamiento posterior.

Además, cada botón de radio se puede configurar para que tenga valores de procesamiento diferentes para cada opción, y esto se puede definir mediante el Editor de reglas de Formularios adaptables

## Uso {#reasons-to-use-radio-button}

Existen varias razones para utilizar botones de radio en un formulario, entre ellas:

- **Opciones limitadas**: los botones de radio se utilizan para proporcionar una lista de opciones predefinidas entre las que el usuario puede elegir y solo se puede seleccionar una opción a la vez. Esto resulta útil cuando el número de opciones es limitado y mutuamente excluyente.

- **Borrar representación**: los botones de radio son claros y fáciles de entender, lo que facilita que los usuarios sepan lo que están seleccionando.

- **Coherencia**: el uso de botones de radio garantiza una forma uniforme y estandarizada de presentar opciones a los usuarios, facilitando su comprensión e interacción con el formulario.

- **Más fácil de usar**: los botones de radio son fáciles de usar, especialmente para los usuarios que no estén familiarizados con la tecnología o que tengan la movilidad limitada.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Botón de opción de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y los componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posterior. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_es). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de botón de radio de Formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del botón de radio para los visitantes con el cuadro de diálogo Configurar. También puede definir las opciones de los botones de radio con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Opciones**: puede añadir valores de datos y mostrar pares de texto utilizando el botón **Añadir**.\
  Una vez añadida una nueva opción, se pueden realizar las acciones siguientes:
   - **Valor de datos**: esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   - **Mostrar texto**: esta opción permite introducir el contenido que se mostrará en un formulario adaptable.
   - **Eliminar**: pulse o haga clic para eliminar la opción de un botón de radio.
   - **Reorganizar**: pulse o haga clic y arrastre para reorganizar el orden de las opciones.
También puede dar formato a las opciones del grupo de botones de opción mediante **Permitir texto enriquecido en las opciones**.

  ![Compatibilidad del texto enriquecido con las opciones](/help/adaptive-forms/assets/richtext-for-options.png)

  Una vez seleccionada la casilla de verificación de **Permitir texto enriquecido en las opciones**, las opciones de formato se vuelven visibles para aplicar estilo a las opciones del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña `Fullscreen` ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido con las opciones](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Tipo de datos del valor enviado**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra un mensaje de error `Value type mismatch`.

- **Opciones predeterminadas**: esta opción le permite añadir valores predeterminados que están preseleccionados cuando se carga el formulario. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Opciones predeterminadas**, la pantalla muestra un mensaje de error `Value type mismatch`.

- **Opciones de visualización**: esta opción se utiliza para definir la alineación visual de los botones de radio en un formulario adaptable. Las dos opciones compatibles son las siguientes:
   - **Horizontal**: cuando se selecciona esta opción, los botones de radio se muestran de izquierda a derecha en un formulario adaptable.
   - **Vertical**: cuando se selecciona esta opción, los botones de radio se muestran de arriba a abajo en un formulario adaptable.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.
- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo del formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Botón de radio.


### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de botón de radio de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de botón de radio de Formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
