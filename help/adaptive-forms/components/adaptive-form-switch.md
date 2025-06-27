---
title: 'Componente principal de formularios adaptables: componente de cambio'
description: Uso o personalización del componente principal de cambio de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Cambio de formulario adaptable{#switch-adaptive-forms-core-component}

El componente de cambio es una interfaz gráfica de usuario que se utiliza en formularios y permite que los usuarios elijan entre dos opciones. Normalmente, alterna entre dos estados y permite que los usuarios los escojan, por lo que se habilita o deshabilita una característica, configuración o funcionalidad. El componente de cambio está diseñado para representar visualmente el estado actual y mostrar si una funcionalidad en particular está activada o desactivada.

El componente de cambio es un elemento de control booleano que establece el valor en verdadero o falso. Por ejemplo, se utiliza para activar o desactivar una funcionalidad, como silenciar o reactivar el sonido, o habilitar o deshabilitar la conexión Bluetooth o wifi.

![Ejemplo del componente de cambio](/help/adaptive-forms/assets/switch-example.png)

{{traditional-aem}}

## Uso {#reasons-to-use-switch}

Las razones más comunes para utilizar el componente de cambio en un formulario adaptable son las siguientes:

- **Interacción con el usuario**: los usuarios pueden interactuar con el componente de cambio al hacer clic o pulsar en él.

- **Estados**: el componente de cambio tiene dos estados: activado y desactivado. El estado inicial del componente de cambio depende de la configuración predeterminada o del estado actual de la funcionalidad que controla.

- **Representación visual**: el componente de cambio refleja visualmente su estado actual al cambiar el color o la posición.

- **Funcionalidad de control**: el componente de cambio se utiliza para habilitar o deshabilitar la característica específica en un formulario de AEM. Por ejemplo, permite a los usuarios activar o desactivar una funcionalidad.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de cambio de formularios adaptables se publicó como parte de los componentes principales, versión 2.0.64. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.64](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de cambio de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del componente de cambio para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones del componente de cambio con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/switch-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con este puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, el componente no se muestra.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Conservar valor del estado Desmarcar**: al seleccionar esta opción, puede especificar el valor que se devolverá cuando el componente de cambio no esté seleccionado.
- **Opciones**: especifique el valor de los datos y muestre el texto de cada opción.
   - **Opción Valor de datos activada**: especifique el valor que se enviará cuando el componente de cambio esté habilitado en un formulario adaptable.
   - **Opción Mostrar texto activada**: especifique el texto que se mostrará como etiqueta cuando el componente de cambio esté habilitado en un formulario adaptable.
   - **Opción Valor de datos desactivada**: especifique el valor que se enviará cuando el componente de cambio no esté habilitado en un formulario adaptable. Esta opción solo está visible si el componente de cambio **Conservar valor del estado Desmarcar** está habilitado.
   - **Opción Mostrar texto desactivada**: especifique el texto que se mostrará como etiqueta cuando el componente de cambio no esté habilitado en un formulario adaptable. Esta opción solo está visible si el componente de cambio **Conservar valor del estado Desmarcar** está habilitado.

  También puede dar formato a las opciones del componente de conmutador mediante **Permitir texto enriquecido en las opciones**.

  ![Compatibilidad del texto enriquecido con las opciones](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

  Una vez seleccionada la casilla de verificación de **Permitir texto enriquecido para las opciones**, las opciones de formato se vuelven visibles para aplicar estilo a las opciones del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña `Fullscreen` ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido con las opciones](/help/adaptive-forms/assets/switch-richtext-for-display.png)

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.
- **Tipo de datos del valor enviado**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra un mensaje de error `Value type mismatch`.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar o bloquear el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Valor predeterminado**: esta opción permite añadir un valor predeterminado en un campo de formulario. Si se selecciona **Componente desactivado** o **Componente de solo lectura**, aparece en pantalla el valor predeterminado. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/switch-validation.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo del formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/switch-help.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/switch-accessibility.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

### Pestaña Estilos {#styles-tab}

![Pestaña Estilos](/help/adaptive-forms/assets/switch-styles.png)

- **Ocultar etiquetas**: seleccione esta opción para ocultar las etiquetas del componente de cambio.

- **Mostrar etiquetas**: seleccione esta opción para mostrar las etiquetas del componente de cambio.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente de cambio.

### Pestaña Estilos {#styles-design-tab}

El componente principal de cambio de formularios adaptables es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal Cambio de los formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.
- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
