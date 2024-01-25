---
title: 'Componente principal de Forms adaptable: componente de conmutador'
description: Uso o personalización del componente principal del conmutador de Forms adaptable.
role: Architect, Developer, Admin, User
hide: true
hidefromToC: true
source-git-commit: d172e019c5621d950a94cbdd8d27e4834dbabe3b
workflow-type: tm+mt
source-wordcount: '1689'
ht-degree: 67%

---


# Cambiar componente{#switch-adaptive-forms-core-component}

El componente de conmutador es una interfaz gráfica de usuario utilizada en los formularios que permite a los usuarios seleccionar entre dos opciones. Normalmente, se trata de una opción de dos estados que permite a los usuarios elegir entre dos estados y habilitar o deshabilitar una característica, configuración o funcionalidad. El componente del conmutador está diseñado para representar visualmente el estado actual y mostrar si una función en particular está activada o desactivada.

El componente switch es un elemento de control booleano que establece el valor en true o false. Por ejemplo, se utiliza para activar o desactivar una función, como silenciar o reactivar el sonido, o activar o desactivar Bluetooth o WiFi.

![Ejemplo del componente Cambiar](/help/adaptive-forms/assets/switch-example.png)

## Uso {#reasons-to-use-switch}

Las razones comunes para utilizar el conmutador en un formulario adaptable son las siguientes:

- **Interacción del usuario**: los usuarios pueden interactuar con el componente de conmutador al hacer clic o pulsar en él.

- **Estados Unidos**: el componente del interruptor tiene dos estados: ON y OFF. El estado inicial del componente de conmutador depende de la configuración predeterminada o del estado actual de la función que controla.

- **Representación visual**: el componente del conmutador refleja visualmente su estado actual al cambiar el color o la posición.

- **Funcionalidad de control** AEM : el componente de conmutador se utiliza para habilitar o deshabilitar la funcionalidad específica en un formulario de. Por ejemplo, permite a los usuarios activar o desactivar una función.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del conmutador de Forms adaptable se publicó como parte de los componentes principales 2.0.64. AEM Esta es una tabla que muestra todas las versiones compatibles, la compatibilidad de la y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.64](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del conmutador Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del componente Switch para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de los componentes de conmutador con facilidad para lograr una experiencia de usuario perfecta.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/switch-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con este puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, el componente no se muestra.

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Conservar valor de estado de desactivación** - Al seleccionar esta opción, puede especificar el valor que se devolverá cuando el componente de conmutador no esté seleccionado.
- **Opciones** : especifique el valor de los datos y muestre el texto de cada opción.
   - **En valor de datos** - Especifique el valor que se enviará cuando el conmutador esté habilitado en un formulario adaptable.
   - **Texto en pantalla** - Especifique el texto que se mostrará como etiqueta cuando el conmutador esté habilitado en un formulario adaptable.
   - **Valor de datos desactivado** - Especifique el valor que se enviará cuando el conmutador no esté habilitado en un formulario adaptable. Esta opción solo está visible si la variable **Conservar valor de estado de desactivación** está activado.
   - **Texto para mostrar desactivado** - Especifique el texto que se mostrará como etiqueta cuando el conmutador no esté habilitado en un formulario adaptable. Esta opción solo está visible si la variable **Conservar valor de estado de desactivación** está activado.

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Tipo de datos del valor enviado**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra un mensaje de error `Value type mismatch`.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar o bloquear el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Valor predeterminado**: esta opción permite añadir un valor predeterminado en un campo de formulario. Si se selecciona **Componente desactivado** o **Componente de solo lectura**, aparece en pantalla el valor predeterminado. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento de envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/switch-validation.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/switch-help.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/switch-accessibility.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

### Pestaña Estilos {#styles-tab}

![Pestaña Estilos](/help/adaptive-forms/assets/switch-styles.png)

- **Ocultar etiquetas** - Seleccione esta opción para ocultar las etiquetas del componente del conmutador.

- **Mostrar etiquetas** - Seleccione esta opción para mostrar las etiquetas del componente del conmutador.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Switch.

### Pestaña Estilos {#styles-design-tab}

El componente principal del conmutador de Forms AEM adaptable es compatible con la función de [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal del grupo de conmutadores de Forms adaptable.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Vea también {#see-also}

{{see-also}}









