---
title: 'Componente principal de formularios adaptables: casilla de verificación'
description: Uso o personalización del Componente principal de la casilla de verificación de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 97%

---

# Componente Casilla de verificación{#checkbox-component}

Una casilla de verificación es un elemento gráfico de interfaz de usuario que se utiliza comúnmente en aplicaciones de software y formularios para permitir a los usuarios realizar una elección binaria entre dos opciones: activada (seleccionada) o desactivada (no seleccionada).

Una casilla de verificación suele representarse como un pequeño cuadrado que se puede activar o desactivar haciendo clic en ella o pulsándola. Cuando se marca una casilla de verificación, esta muestra una marca de verificación para indicar que la opción o función asociada está activa o habilitada.

>[!NOTE]
>
> Para AEM 6.5 Forms, este componente se introdujo con el Service Pack 19 (6.5.19.0) de AEM 6.5 Forms. Para habilitar este componente, asegúrese de que están instaladas las versiones necesarias de los componentes principales de Forms y de WCM. Para obtener información detallada sobre las versiones de los componentes principales de Adaptive Forms, consulte [Lanzamientos de componentes principales de Adaptive Forms](/help/adaptive-forms/version.md)

**Ejemplo**

![grupo de casillas de verificación](/help/adaptive-forms/assets/checkbox-example.png)

## Uso {#reasons-to-use-checkbox}

Las razones más comunes para utilizar una casilla de verificación en un Formulario adaptable son las siguientes:

- **Facilidad de uso**: las casillas de verificación son visualmente claras y proporcionan una forma directa de realizar elecciones binarias. Son intuitivas y fáciles de entender, por lo que son fáciles de usar.

- **Consentimiento y acuerdo**: las casillas de verificación se utilizan para obtener el consentimiento del usuario para varios fines, por ejemplo, aceptar términos y condiciones, suscribirse a boletines informativos o confirmar la verificación de la edad. Dejan claro que el usuario está aceptando algo activamente.

- **Confirmación visual**: las casillas de verificación marcadas proporcionan una confirmación visual a los usuarios de que su selección se ha registrado. Estos comentarios ayudan a evitar errores de usuarios y garantizan que sepan que sus opciones se han registrado.

- **Prevención de errores**: las casillas de verificación reducen la probabilidad de que se produzcan errores al permitir que los usuarios revisen y confirmen las opciones antes del envío del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Casilla de verificación de formularios adaptables se publicó como parte de los componentes principales, versión 2.0.52. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.52](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el Componente principal Casillas de verificación de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las Casillas de verificación para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de la Casilla de verificación con facilidad para que la experiencia del usuario sea óptima.

![Pestaña Básicos](/help/adaptive-forms/assets/checkbox-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con este puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, el componente no se muestra.

<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png) -->

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Tipo de datos del valor enviado**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si el **tipo de datos del valor enviado** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra un mensaje de error `Value type mismatch`.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar o bloquear el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
  <!-- - **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->
- **Cuando se selecciona, se devuelve el valor**: seleccione esta opción para especificar qué valor debe asociarse a la casilla de verificación cuando está activada o seleccionada. Es la acción que se produce cuando un usuario marca o usted marca la casilla de verificación.
- **Conservar valor de estado de desactivación**: seleccione esta opción para especificar el valor que se devolverá cuando el componente Casilla de verificación no esté seleccionado. If **Conservar valor de estado de desactivación** está activada o configurada como verdadera, **Cuando no está marcada, devuelve un valor** aparece la opción.
- **Cuando no está marcada, devuelve un valor**: la opción le permite especificar qué valor debe asociarse con la casilla de verificación cuando está en un estado sin marcar o sin seleccionar.

- **Valor predeterminado**: esta opción permite añadir un valor predeterminado en un campo de formulario. Si se selecciona **Componente desactivado** o **Componente de solo lectura**, aparece en pantalla el valor predeterminado. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento de envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/checkbox-validation.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.
- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/checkbox-help.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se emplea para definir y administrar estilos CSS para el componente de Casilla de verificación.

### Pestaña Estilos {#styles-tab}

El Componente principal de Casillas de verificación de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de la casilla de verificación de formularios adaptables.

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
