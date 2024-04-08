---
title: 'Componente principal de formularios adaptables: lista desplegable'
description: Uso o personalización del componente principal de lista desplegable de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 9d59d0d2-d38f-4ed5-8b43-984c45f26f27
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '2011'
ht-degree: 98%

---


# Lista desplegable {#drop-down-list-adaptive-forms-core-component}

Una lista desplegable de un formulario adaptable permite a los usuarios seleccionar una o más opciones de una lista de opciones predefinidas. Las opciones pueden ser de tipo cadena, número o booleano. Además, el componente de lista desplegable se puede configurar para que tenga valores predeterminados y validaciones diferentes.

**Ejemplo**
![ejemplo](/help/adaptive-forms/assets/drop-down-list.png)

## Uso {#reasons-to-use-drop-down-list}

Existen varias razones por las que resulta beneficioso incluir una lista desplegable en un formulario adaptable, entre ellas:

- **Lista larga de opciones**: las listas desplegables son útiles para situaciones en las que hay una larga lista de opciones disponibles para un campo. Ocupan menos espacio en el formulario que una lista de botones de radio o casillas de verificación, y pueden resultar menos engorrosas para los usuarios.

- **Coherencia**: las listas desplegables proporcionan coherencia en el diseño y la presentación del formulario, lo que facilita la navegación y la intuición de los usuarios.

- **Claridad**: las listas desplegables pueden hacer que el formulario sea más claro y fácil de entender, ya que ofrecen una lista clara y concisa de opciones.

- **Experiencia del usuario**: las listas desplegables pueden utilizarse para que el formulario sea más fácil de usar, ya que ofrecen una forma clara e intuitiva para que los usuarios seleccionen las opciones.

- **Análisis de datos**: las listas desplegables pueden utilizarse para recopilar datos de varias fuentes y analizarlos, o bien para utilizarlos como entrada para un procesamiento posterior.


**Cuadro de diálogo Propiedades**

![cuadro de diálogo propiedades](/help/adaptive-forms/assets/drop-down-list-properties.png)

En este ejemplo, el elemento Opciones se utiliza para definir los elementos de la lista. El elemento **Mostrar texto** se utiliza para proporcionar una etiqueta para los elementos de lista y **Valor de datos** se utiliza para especificar el valor que se envía al servidor cuando se envía el formulario.

Cada opción de lista desplegable tiene un valor de datos único y un atributo de texto de visualización. Si un usuario selecciona la opción “Rojo”, el valor de datos correspondiente se envía al servidor cuando se envía el formulario. Estos datos se pueden procesar mediante una secuencia de comandos del lado del servidor para determinar qué opciones ha seleccionado el usuario y se pueden utilizar para realizar diversas acciones, como actualizar otros campos del formulario o enviar los datos del formulario a una secuencia de comandos del lado del servidor para un procesamiento posterior.

Además, la lista desplegable se puede configurar para que tenga diferentes valores de procesamiento en cada opción, y esto se puede definir mediante el Editor de reglas de los formularios adaptables.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de lista desplegable de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de la lista desplegable para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de la lista desplegable con facilidad para que la experiencia del usuario sea óptima.

![Pestaña Básicos](/help/adaptive-forms/assets/dropdown_basictab.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece encima del componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png) -->

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Permitir selección múltiple**: seleccione esta opción para seleccionar varias opciones en una lista desplegable.
- **Guardar valor como**: esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si **Guardar valor como** está establecido en `Number` y se agregan datos de cadena a **Valor de datos** en la pestaña **Opciones**, la pantalla muestra el mensaje de error `Value type mismatch`.

  En la pestaña **Opciones**, puede agregar valores de datos y mostrar pares de texto utilizando el botón **Agregar**. Una vez agregada una nueva opción, se realizan las acciones siguientes:

   - **Valor de datos**: esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   - **Mostrar texto**: esta opción permite introducir el contenido que se mostrará en el formulario adaptable.
   - **Eliminar**: pulse o haga clic para eliminar la opción de un menú desplegable.
   - **Reorganizar**: pulse o haga clic y arrastre para reorganizar el orden de la opción de un menú desplegable.

- **Opción predeterminada** : Esta opción le permite añadir valores predeterminados. Utilice el icono eliminar para eliminar la opción agregada. Si **Guardar valor como** está establecido en `Number` y se agregan datos de cadena a **Opciones predeterminadas**, la pantalla muestra un mensaje de error `Value type mismatch`.

- **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

- **Opciones** - Puede añadir valores de datos y mostrar pares de texto mediante el **Añadir** botón.  Después de añadir una nueva opción, se pueden realizar las siguientes acciones:
   - **Valor de datos**: esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   - **Mostrar texto**: esta opción permite introducir el contenido que se mostrará en el formulario adaptable.
   - **Eliminar**: pulse o haga clic para eliminar la opción de una casilla de verificación.
   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

- **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/dropdown_validationtab.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/dropdown_helptab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)


**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Lista desplegable.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de lista desplegable de formularios adaptables es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de lista desplegable de formularios adaptables.

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
