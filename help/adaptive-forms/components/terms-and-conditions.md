---
title: Términos y condiciones del componente principal de Forms adaptable
description: Usar o personalizar el componente principal de los términos y condiciones de Forms adaptable.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '2639'
ht-degree: 66%

---

# Componente Términos y condiciones

A **Términos y condiciones** componente hace referencia a una sección de un formulario que describe los términos, las reglas y las condiciones que los usuarios deben aceptar o cumplir al utilizar un servicio o acceder al contenido.

El **Términos y condiciones** es un componente compuesto que consta de componentes Texto, Casilla de verificación y Vínculo. El componente de texto contiene un título junto con una breve descripción del propósito y el alcance de los términos y condiciones. También incluye una casilla de verificación utilizada para obtener el consentimiento explícito del usuario. También puede reemplazar un texto de consentimiento con vínculos.

**Ejemplo**

![términos y condiciones](/help/adaptive-forms/assets/terms-and-conditions.png)

Consulte [Subcomponentes del componente Términos y condiciones](#sub-component) para obtener más información sobre los distintos componentes del componente Términos y condiciones.

## Uso {#reasons-to-use-termsandconditions}

- **Acuerdo de usuario**: el componente sirve como acuerdo entre el proveedor de servicios y el usuario. Los usuarios deben reconocer y aceptar los términos antes de acceder al servicio o contenido.

- **Cumplimiento legal**: Garantiza el cumplimiento y la protección legales para el proveedor de servicios al delinear los derechos, responsabilidades y responsabilidades de ambas partes.

- **Procesos de registro**: Los formularios de registro o registro incluyen lo siguiente **Términos y condiciones** , que requiere que los usuarios acepten explícitamente los términos antes de crear una cuenta o utilizar un servicio.

- **Transacciones de comercio electrónico**: Los sitios web en línea incluyen **Términos y condiciones** para que los usuarios acepten los términos y condiciones como parte del proceso de cierre de compra antes de realizar compras en línea.

- **Acuerdos de seguridad y privacidad**: La **Términos y condiciones** Este componente incluye detalles sobre cómo se recopilan, almacenan y utilizan los datos del usuario, a menudo complementados por una política de privacidad independiente

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.62 para Cloud Service y componentes principales 1.1.28 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.62](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.28](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal Grupo de casillas de verificación de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de los componentes de términos y condiciones para los visitantes con el Cuadro de diálogo de configuración. También puede definir las opciones de términos y condiciones con facilidad para lograr una experiencia de usuario perfecta.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Mostrar opción de aprobación** - Seleccione la opción para mostrar la casilla de verificación de consentimiento utilizada para obtener el consentimiento explícito del usuario.

- **Mostrar como elemento emergente** : seleccione la opción para mostrar el componente Términos y condiciones en una ventana emergente.

- **Reemplazar el texto de consentimiento por vínculos web**: seleccione la opción para reemplazar un texto de consentimiento con un vínculo web.  Si la opción está desmarcada, el texto de consentimiento se muestra de forma predeterminada.

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Agrupar datos de componentes secundarios al enviar el formulario (ajustar datos en objeto)**: cuando se selecciona la opción, los datos de sus componentes secundarios se anidan dentro del objeto JSON del componente principal. Sin embargo, si la opción no está seleccionada, los datos JSON enviados tienen una estructura plana, sin ningún objeto para el componente principal. Por ejemplo:

   - Cuando la opción está seleccionada, los datos de los componentes secundarios (por ejemplo, calle, ciudad y código postal) se anidan dentro del componente principal (dirección) como un objeto JSON. Esto crea una estructura jerárquica y los datos se organizan bajo el componente principal.

     Estructura de los datos enviados:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Cuando la opción no está seleccionada, los datos JSON enviados tienen una estructura plana sin ningún objeto para el componente principal (dirección). Todos los datos se encuentran al mismo nivel, sin ninguna organización jerárquica.

     Estructura de los datos enviados:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad

![Pestaña Accesibilidad](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El Cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Términos y condiciones.


### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de los términos y condiciones de Forms AEM adaptable admite el uso de los siguientes elementos [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de grupo de casillas de verificación de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de agregar el grupo de propiedades personalizadas, puede ver las siguientes opciones:

   - **Pares de clave-valor**: Puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Subcomponentes del componente Términos y condiciones {#sub-component}

**Términos y condiciones** el componente es un componente compuesto que consta de los siguientes subcomponentes:
- [Componente Vínculo](#link)
- [Componente de texto](#text)
- [Componente Casilla](#checkbox)

### Componente Vínculo{#link}

Este componente reemplaza un texto de consentimiento con un vínculo web o vínculos. Se utiliza en un escenario en el que el usuario intenta ofrecer referencias a secciones concretas, información adicional o documentos externos. Puede personalizar fácilmente la variable **Vínculo** Componente individualmente para visitantes con el cuadro de diálogo de configuración.

#### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Vínculos** : especifique el vínculo y el texto para mostrar correspondiente que se utiliza en lugar del texto de consentimiento. Para añadir varios vínculos, haga clic en **Añadir** botón.

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar el origen de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente** : seleccione la opción para deshabilitar o bloquear el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

#### Pestaña Validación

![Pestaña Validación](/help/adaptive-forms/assets/link-validation-tab.png)

- **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. Después de seleccionar la opción, debe realizar una selección antes de continuar con el envío de un formulario. No puede seleccionar **Ocultar componente** o **Deshabilitar componente** en la pestaña **Básico** cuando se selecciona esta opción.

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

### Pestaña Contenido de ayuda {#helpcontent-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/link-help-tab.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad

![Pestaña Accesibilidad](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

### Componente de texto {#text}

**Texto** componente muestra el contenido textual que proporciona información a los usuarios. Este componente incluye los términos y condiciones reales, el idioma legal o cualquier otra información textual relevante.

Puede personalizar fácilmente la variable [Componente Texto](/help/adaptive-forms/components/text.md) individualmente para los visitantes con el cuadro de diálogo de configuración. Para definir las opciones de texto con facilidad para una experiencia de usuario perfecta, utilice el [cuadro de diálogo de configuración del componente texto](/help/adaptive-forms/components/text.md#configure-dialog).


### Componente Casilla {#checkbox}

Se utiliza una casilla de verificación para obtener el consentimiento o el reconocimiento del usuario. Sirve como indicador visual de que el usuario ha leído y aceptado los términos descritos. Es obligatorio seleccionar la casilla de verificación para indicar el consentimiento del usuario.

Puede personalizar fácilmente la variable [Componente Casilla](/help/adaptive-forms/components/checkbox.md) individualmente para los visitantes con el cuadro de diálogo de configuración. Para definir las propiedades de la casilla de verificación para una experiencia de usuario perfecta, utilice el [cuadro de diálogo de configuración del componente casilla de verificación](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Artículos relacionados {#related-articles}

{{more-like-this}}

## Vea también {#see-also}

{{see-also}}