---
title: 'Componente principal de Forms adaptable: fichas verticales'
description: Uso o personalización del componente principal Pestañas verticales de Forms adaptable.
role: Architect, Developer, Admin, User
exl-id: d5cd1c18-6840-4f2f-a767-a69b803e6075
source-git-commit: 4ca65f93e223fdd0b0a701ef335ed5be1fbab7fe
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 65%

---

# Componente Pestañas verticales{#vertical-tabs-adaptive-forms-core-component}

Las pestañas verticales de un formulario adaptable hacen referencia a un patrón de diseño en el que varias secciones de un formulario se agrupan y se muestran como pestañas independientes, alineadas verticalmente. Se puede pasar de una pestaña a otra para acceder a diferentes secciones del formulario. Cada pestaña actúa como un activador para mostrar y ocultar el contenido del formulario relacionado. Las pestañas verticales ayudan a organizar los formularios largos en secciones manejables y mejorar la experiencia del usuario. Las pestañas pueden ayudar a que un formulario sea más accesible para las personas con discapacidades, ya que pueden cambiar entre secciones con la navegación mediante el teclado.

Cuando se hace clic en una pestaña, el contenido del formulario se actualiza de forma dinámica para mostrar la sección correspondiente.

![ejemplo](/help/adaptive-forms/assets/horizontal-example.png)

## Uso {#reasons-to-use-vertical-tabs}

Los motivos comunes para utilizar pestañas verticales en un formulario adaptable son:

- **Usabilidad mejorada**: Las pestañas verticales facilitan a los usuarios la navegación por el formulario, especialmente si este tiene varias secciones o un gran número de campos.

- **Administración de espacio**: las pestañas verticales ayudan a conservar el espacio de pantalla al agrupar secciones de formulario relacionadas en pestañas y mostrar solo una sección a la vez.

- **Mejor organización**: las pestañas proporcionan una estructura clara y organizada para un formulario, lo que facilita la comprensión y cumplimentación del formulario.

- **Mayor participación del usuario**: las pestañas verticales pueden hacer que un formulario sea más atractivo visualmente y atractivo para los usuarios, lo que puede mejorar la tasa de finalización del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de las pestañas verticales de Forms adaptable se publicó como parte de los componentes principales 2.0.18. AEM Esta es una tabla que muestra todas las versiones compatibles, la compatibilidad de la y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.18](/help/versions.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de las pestañas verticales de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).


## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las pestañas verticales para los visitantes con el Cuadro de diálogo de configuración. También puede definir las opciones de pestañas verticales con facilidad para una experiencia de usuario perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

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

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Repetir tabulación vertical {#repeat-tabs-on-top}

![Pestaña Repetir](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

Puede utilizar las opciones de repetibilidad para duplicar el componente Pestañas verticales y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente Pestañas verticales y acceder a su configuración, se presentan las siguientes opciones:

- **Hacer que las tabulaciones verticales sean repetibles**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
- **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el componente Tabulaciones verticales. El valor cero indica que el componente Tabulaciones verticales no se repite; el valor predeterminado es cero.
- **Máximo de repeticiones**: establece el número máximo de veces que se puede repetir el componente Tabulaciones verticales. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro de las pestañas verticales, siga los pasos que se proporcionan en la [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=es) artículo.

### Pestaña Elementos {#items-tab}

![Pestaña Elementos](/help/adaptive-forms/assets/vertical-tab-items.png)

El botón **Agregar** permite seleccionar un componente para añadirlo como un panel en la ventana de selección de componentes. Después de añadir el componente, podrá ver las siguientes opciones:

- **Icono**: el icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información sobre herramientas.
- **Descripción**: la descripción utilizada como texto del panel. De forma predeterminada, el nombre del componente seleccionado para el panel.
- **Eliminar** : toque o haga clic para eliminar el panel del componente Pestañas verticales.
- **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/vertical-tab-help.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/vertical-tab-accessibility.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

- **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente de pestañas verticales de Forms adaptable, puede establecer lo siguiente:

- Los componentes principales que un creador de formularios puede agregar a las pestañas verticales en el editor de Forms adaptable
- Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente Pestañas verticales en el editor de Forms adaptable.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña Componentes permitidos](/help/adaptive-forms/assets/tabs-allowed-component.png)

El **Componentes permitidos** permite al editor de plantillas establecer los componentes que se pueden añadir como elementos a los paneles del componente Pestañas verticales en el editor de Forms adaptable.

### Pestaña Estilos {#styles-tab}

![Pestaña Estilos](/help/adaptive-forms/assets/tabs-styles-tab.png)

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de las pestañas verticales de Forms AEM adaptable admite el uso de la [Sistema de estilos](/help/get-started/authoring.md#component-styling).

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal Pestañas verticales de Forms adaptable.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Propiedades personalizadas

![Pestaña Propiedades personalizadas](/help/adaptive-forms/assets/tabs-custom-properties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de agregar el grupo de propiedades personalizadas, puede ver las siguientes opciones:

   - **Pares de clave-valor**: Puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Vea también {#see-also}

{{see-also}}
