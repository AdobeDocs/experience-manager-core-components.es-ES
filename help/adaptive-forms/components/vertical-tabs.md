---
title: 'Componente principal de formularios adaptables: pestañas verticales'
description: Uso o personalización del componente principal de pestañas verticales de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: d5cd1c18-6840-4f2f-a767-a69b803e6075
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2173'
ht-degree: 100%

---


# Componente Pestañas verticales{#vertical-tabs-adaptive-forms-core-component}

Las pestañas verticales de un Formulario adaptable hacen referencia a un patrón de diseño en el que varias secciones de un formulario se agrupan conjuntamente y se muestran como pestañas independientes, alineadas horizontalmente. Se puede pasar de una pestaña a otra para acceder a diferentes secciones del formulario. Cada pestaña actúa como un activador para mostrar y ocultar el contenido del formulario relacionado. Las pestañas horizontales ayudan a organizar formularios largos en secciones manejables y mejoran la experiencia del usuario. Las pestañas pueden ayudar a que un formulario sea más accesible para las personas con discapacidades, ya que pueden cambiar entre secciones con la navegación mediante el teclado.
Cuando se hace clic en una pestaña, el contenido del formulario se actualiza de forma dinámica para mostrar la sección correspondiente.

>[!NOTE]
>
> Para AEM 6.5 Forms, este componente se introdujo con AEM 6.5 Forms Service Pack 19 (6.5.19.0). Para habilitar este componente, asegúrese de que están instaladas las versiones necesarias de los componentes principales de Forms y de WCM. Para obtener información detallada sobre las versiones de los componentes principales de Formularios adaptables, consulte [Lanzamientos de componentes principales de Adaptive Forms](/help/adaptive-forms/version.md)

![ejemplo](/help/adaptive-forms/assets/horizontal-example.png)

{{traditional-aem}}

## Uso {#reasons-to-use-vertical-tabs}

Las razones más comunes para utilizar pestañas verticales en un Formulario adaptable son las siguientes:

- **Uso mejorado**: las pestañas verticales facilitan a los usuarios el desplazamiento por el formulario, especialmente si este tiene varias secciones o un gran número de campos.

- **Administración del espacio**: las pestañas verticales conservan espacio en la pantalla al agrupar las secciones de formulario relacionadas en pestañas y muestran solo una sección a la vez.

- **Mejor organización**: las pestañas proporcionan una estructura clara y organizada para un formulario, lo que facilita la comprensión y cumplimentación del formulario.

- **Mayor participación del usuario**: las pestañas verticales pueden hacer que un formulario sea visualmente más atractivo y atrayente para los usuarios, lo que puede mejorar la tasa de finalización del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Pestañas verticales de los formularios adaptables se publicó como parte de los componentes principales, versión 2.0.18. A continuación, se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatible con la <br>[versión 2.0.18](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el Componente principal de pestañas verticales de Formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/verticaltabs/v1/verticaltabs). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de las pestañas verticales para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de pestañas verticales con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/vertical-tab-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación de **Permitir texto enriquecido en el título**, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

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

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Repetir pestaña vertical {#repeat-tabs-on-top}

![Repetir pestaña](/help/adaptive-forms/assets/vertical-tab-repeat-vertical-tab.png)

Puede utilizar las opciones de repetibilidad para duplicar el componente Pestañas verticales y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente Pestañas verticales y acceder a su configuración, se presentan las siguientes opciones:

- **Hacer que las pestañas verticales sean repetibles**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
- **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el componente pestañas verticales. Un valor de cero indica que el componente de pestañas verticales no se repite; el valor predeterminado es cero.
- **Máximo de repeticiones**: establece el número máximo de veces que se puede repetir el componente pestañas verticales. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro de las pestañas verticales, siga los pasos que se proporcionan en el artículo [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=es).

### Pestaña Elementos {#items-tab}

![Pestaña Elementos](/help/adaptive-forms/assets/vertical-tab-items.png)

El botón **Agregar** permite seleccionar un componente para añadirlo como un panel en la ventana de selección de componentes. Después de añadir el componente, podrá ver las siguientes opciones:

- **Icono**: el icono identifica el componente del panel en la lista. Puede pasar el ratón sobre el icono para ver el nombre completo del componente como información sobre herramientas.
- **Descripción**: la descripción utilizada como texto del panel. De forma predeterminada, el nombre del componente seleccionado para el panel.
- **Eliminar**: toque o haga clic para eliminar el panel del componente de pestañas verticales.
- **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de los paneles.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/vertical-tab-help.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/vertical-tab-accessibility.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

- **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente Pestañas verticales de formularios adaptables, puede establecer lo siguiente:

- Los componentes principales que un creador de formularios puede añadir a las pestañas verticales del editor de formularios adaptables
- Nombres simples para estilos (clases CSS) que pueden aplicarse en el cuadro de diálogo de propiedades del componente Pestañas verticales en el editor de formularios adaptables.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña Componentes permitidos](/help/adaptive-forms/assets/tabs-allowed-component.png)

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente de pestañas verticales del editor de formularios adaptables.

### Pestaña Estilos {#styles-tab}

![Pestaña Estilos](/help/adaptive-forms/assets/tabs-styles-tab.png)

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de las pestañas verticales de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el Componente principal de las pestañas verticales de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Propiedades personalizadas

![Pestaña Propiedades personalizadas](/help/adaptive-forms/assets/tabs-custom-properties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
