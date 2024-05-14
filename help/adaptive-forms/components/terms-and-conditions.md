---
title: Términos y condiciones del Componente principal de Formularios adaptables
description: Usar o personalizar el Componente principal de los Términos y condiciones de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: c3401da271efd930d1a2711bcab25c29f763f38e
workflow-type: tm+mt
source-wordcount: '3115'
ht-degree: 99%

---

# Componente Términos y condiciones

<span class="preview"> Este artículo incluye contenido sobre  **Permitir texto enriquecido en el título**  y  **Permitir texto enriquecido en las opciones**  funciones, funciones previas al lanzamiento. La función previa al lanzamiento solo es accesible a través de nuestro [canal previo al lanzamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=es#new-features).</span>

Un componente **Términos y condiciones** hace referencia a una sección de un formulario que describe los términos, las reglas y las condiciones que los usuarios deben aceptar o cumplir al utilizar un servicio o acceder al contenido.

El componente **Términos y condiciones** es un componente compuesto que consta de componentes Texto, Casilla de verificación y Vínculo. El componente de texto contiene un título junto con una breve descripción del propósito y el alcance de los términos y condiciones. También incluye una casilla de verificación utilizada para obtener el consentimiento explícito del usuario. También puede reemplazar un texto de consentimiento con vínculos.

>[!NOTE]
>
> Para AEM 6.5 Forms, este componente se introdujo con el Service Pack 19 (6.5.19.0) de AEM 6.5 Forms. Para habilitar este componente, asegúrese de que están instaladas las versiones necesarias de los componentes principales de Forms y de WCM. Para obtener información detallada sobre las versiones de los componentes principales de Adaptive Forms, consulte [Lanzamientos de componentes principales de Adaptive Forms](/help/adaptive-forms/version.md)

**Ejemplo**

![términos y condiciones](/help/adaptive-forms/assets/terms-and-conditions.png)

Consulte la sección [Subcomponentes del componente Términos y condiciones](#sub-component) para obtener más información sobre las distintas partes del componente Términos y condiciones.

## Uso {#reasons-to-use-termsandconditions}

- **Acuerdo de usuario**: el componente sirve como acuerdo entre el proveedor de servicios y el usuario. Los usuarios deben reconocer y aceptar los términos antes de acceder al servicio o contenido.

- **Cumplimiento legal**: garantiza el cumplimiento y la protección legales para el proveedor de servicios al delinear los derechos, responsabilidades y obligaciones de ambas partes.

- **Procesos de registro**: los formularios de registro incluyen el componente **Términos y condiciones**, que requiere que los usuarios acepten explícitamente los términos antes de crear una cuenta o utilizar un servicio.

- **Transacciones de comercio electrónico**: los sitios web en línea incluyen el componente **Términos y condiciones** para que los usuarios acepten los términos y condiciones como parte del proceso de cierre de compra antes de realizar compras en línea.

- **Acuerdos de seguridad y privacidad**: el componente **Términos y condiciones** incluye detalles sobre cómo se recopilan, almacenan y utilizan los datos del usuario, a menudo complementados por una política de privacidad independiente

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales, versión 2.0.62 para Cloud Service y componentes principales, versión 1.1.28 para AEM 6.5.16.0 Forms o versiones posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.62](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.28](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de términos y condiciones de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del componente de términos y condiciones para los visitantes con el cuadro de diálogo Configurar. También puede definir las opciones de términos y condiciones con facilidad para una experiencia de usuario optimizada.

### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Mostrar opción de aprobación**: seleccione la opción para mostrar la casilla de verificación de consentimiento utilizada para obtener el consentimiento explícito del usuario.

- **Mostrar como elemento emergente**: seleccione la opción para mostrar el componente términos y condiciones en una ventana emergente.

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

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
- **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Términos y condiciones.


### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El Componente principal de Términos y condiciones de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal Términos y condiciones de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Subcomponentes del componente Términos y condiciones {#sub-component}

El componente **Términos y condiciones** es un componente compuesto que consta de los siguientes subcomponentes:
- [Componente Vínculo](#link)
- [Componente de texto](#text)
- [Componente Casilla de verificación](#checkbox)

### Componente Vínculo{#link}

Este componente reemplaza un texto de consentimiento con un vínculo o vínculos web. Se utiliza en un escenario en el que el usuario intenta ofrecer referencias a secciones concretas, información adicional o documentos externos. Puede personalizar fácilmente el componente **Vínculo** individualmente para visitantes con el cuadro de diálogo de configuración.

#### Pestaña Básicos

![Pestaña Básicos](/help/adaptive-forms/assets/link-basic-tab.png)

- **Nombre**: el nombre identifica de forma exclusiva el componente en el editor de reglas. No se permiten caracteres especiales ni espacios en las cadenas de nombre.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos mediante opciones como negrita, cursiva, estilos de fuente, colores y alineación, lo que mejora la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Vínculos**: especifique el vínculo y el texto para mostrar correspondiente que se utiliza en lugar del texto de consentimiento. Para añadir varios vínculos, haga clic en el botón **Añadir**.
Una vez añadida una nueva opción, se pueden realizar las acciones siguientes:
   - **Vincular**: esta opción permite introducir la URL que se redirigirá cuando se seleccione una opción.
   - **Mostrar texto**: esta opción permite introducir el contenido que se mostrará en un formulario adaptable.
   - **Eliminar**: pulse o haga clic para eliminar la opción de un botón de radio.
   - **Reorganizar**: pulse o haga clic y arrastre para reorganizar el orden de las opciones.

  También puede dar formato a las opciones del grupo de casillas de verificación mediante **Permitir texto enriquecido en las opciones**. Una vez seleccionada la casilla de verificación de **Permitir texto enriquecido en las opciones**, las opciones de formato se vuelven visibles para aplicar estilo a las opciones del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña `Fullscreen` ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido con las opciones](/help/adaptive-forms/assets/link-options.png)

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar o bloquear el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
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

El componente de **Texto** muestra el contenido textual que proporciona información a los usuarios. Este componente incluye los términos y condiciones reales, el idioma legal o cualquier otra información textual relevante.

Puede personalizar fácilmente el [Componente de texto](/help/adaptive-forms/components/text.md) individualmente para los visitantes con el cuadro de diálogo de configuración. Para definir las opciones de texto con facilidad para una experiencia de usuario perfecta, utilice el [cuadro de diálogo de configuración del componente texto](/help/adaptive-forms/components/text.md#configure-dialog).


### Componente Casilla de verificación {#checkbox}

Se utiliza una casilla de verificación para obtener el consentimiento o el reconocimiento del usuario. Sirve como indicador visual de que el usuario ha leído y aceptado los términos descritos. Es obligatorio seleccionar la casilla de verificación para indicar el consentimiento del usuario.

Puede personalizar fácilmente el [Componente de las casillas de verificación](/help/adaptive-forms/components/checkbox.md) individualmente para los visitantes con el Cuadro de diálogo de configuración. Para definir las propiedades de la casilla de verificación para una experiencia de usuario optimizada, utilice el [cuadro de diálogo de configuración del componente casilla de verificación](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
