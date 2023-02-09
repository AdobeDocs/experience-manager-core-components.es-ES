---
title: 'Componente principal de Forms adaptable: grupo de casillas de verificación'
description: Uso o personalización del componente principal del grupo de casillas de verificación de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 2%

---


# Grupo de casillas {#button-component-adaptive-forms-core-component}

Un grupo de casillas de verificación de un formulario adaptable es un conjunto de casillas de verificación relacionadas que permiten a los usuarios seleccionar una o más opciones de una lista. Cada casilla de verificación está representada por un valor de datos (valor utilizado para procesar elementos de un grupo de casillas de verificación) y un valor de visualización (etiqueta para cada elemento de casilla de verificación que describe su propósito)

**Ejemplo**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Cuadro de diálogo Propiedades**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

En este ejemplo, el elemento Opciones se utiliza para agrupar las casillas de verificación. La variable **Mostrar texto** se utiliza para proporcionar una etiqueta para un elemento y **Valor de datos** se utiliza para especificar el valor que se envía al servidor cuando se envía el formulario.

Cada opción o elemento de casilla de verificación tiene un valor de datos único y un atributo de texto de visualización . Si un usuario selecciona las casillas de verificación &quot;Hijo&quot; e &quot;Hija&quot;, el valor de datos correspondiente se envía al servidor cuando se envía el formulario. Estos datos se pueden procesar mediante una secuencia de comandos del lado del servidor para determinar qué opciones seleccionó el usuario y se pueden utilizar para realizar diversas acciones, como actualizar otros campos del formulario o enviar los datos del formulario a una secuencia de comandos del lado del servidor para un procesamiento posterior.

Además, el grupo de casillas de verificación se puede configurar para que tenga valores de procesamiento diferentes para cada opción, y esto se puede establecer mediante el Editor de reglas de Forms adaptable.

## Uso {#reasons-to-use-check-box-group}

Existen varias razones por las que resulta beneficioso incluir un grupo de casillas de verificación en un formulario adaptable, entre ellas:

* **Múltiples selecciones**: Un grupo de casillas de verificación permite a los usuarios seleccionar varias opciones de una lista, lo que puede resultar útil en situaciones en las que se permiten o requieren varias selecciones.

* **Experiencia del usuario**: El grupo de casillas de verificación se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de que los usuarios seleccionen varias opciones.

* **Análisis de datos**: El grupo de casillas de verificación se puede utilizar para recopilar datos de varias fuentes y analizarlos, o para utilizarlos como entrada para un procesamiento posterior.

* **Encuestas**: El grupo de casillas de verificación se puede usar en los estudios para seleccionar varias opciones para una pregunta.

* **Preferencias de usuario**: El grupo de casillas de verificación se puede usar para recopilar las preferencias de usuario para las distintas opciones.

* **Valor de datos**: El grupo de casillas de verificación también se puede utilizar para procesar elementos de un grupo de casillas de verificación.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del grupo de casillas de verificación de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service |
|--- |--- |---|---|
| Versión 1 | Compatible  con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del grupo de casillas de verificación de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las casillas de verificación para los visitantes con el cuadro de diálogo Configurar . También puede definir opciones de casilla de verificación con facilidad para que la experiencia de usuario sea perfecta.


### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Nombre** - El nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Opciones** - Puede agregar valores de datos y mostrar pares de texto usando la variable **Agregar** botón. Una vez añadida una nueva opción, se pueden realizar las siguientes acciones:

   * **Valor de datos** - Esta opción permite introducir el contenido que se enviará cuando se seleccione una opción.
   * **Mostrar texto** - Esta opción permite introducir el contenido que se mostrará en un formulario adaptable.
   * **Eliminar** - Toque o haga clic para eliminar la opción de una casilla de verificación .
   * **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.

* **Tipo de datos del valor enviado** - Esta opción especifica el tipo de datos del valor enviado cuando se selecciona cualquier opción. Si la variable **tipo de datos del valor enviado** está configurado como `Number` y se agregan datos de cadena a **Valor de datos** &#x200B; de &#x200B; en el **Opciones** , la pantalla muestra un `Value type mismatch` mensaje de error.

* **Opciones de visualización** - Esta opción se utiliza para establecer la alineación visual de las casillas de verificación en un formulario adaptable. Las dos opciones admitidas son:
   * **Horizontal** - Cuando se selecciona esta opción, las casillas de verificación se muestran de izquierda a derecha en un formulario adaptable.
   * **Vertical** - Cuando se selecciona esta opción, las casillas de verificación se muestran de arriba a abajo en un formulario adaptable.

* **Opciones predeterminadas** - Esta opción le permite agregar valores predeterminados preseleccionados cuando se carga el formulario. Utilice el icono eliminar para eliminar las opciones añadidas. Si la variable **tipo de datos del valor enviado** está configurado como `Number` y se agregan datos de cadena a **Opciones predeterminadas**, la pantalla muestra un `Value type mismatch` mensaje de error.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo de formulario se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Ficha Contenido de ayuda {#helpcontent-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad](/help/adaptive-forms/assets/checkbox_accessibility.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

   En el **Accesibilidad** , los valores se establecen para [Accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) etiquetas para el componente. Hay varias opciones disponibles para usar el texto del lector de pantalla:

* **Texto personalizado**: Seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado . Puede agregar información relevante en el cuadro de diálogo Texto personalizado.

* **Título**: Seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Grupo de casillas de verificación.

### Pestaña Estilos {#styles-tab}

El componente principal del grupo de casillas de verificación de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del grupo de casillas de verificación adaptables de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

