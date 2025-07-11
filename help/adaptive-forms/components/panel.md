---
title: 'Componente principal de formularios adaptables: contenedor de panel'
description: Uso o personalización del componente principal del contenedor de panel de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Panel{#panel-container-adaptive-forms-core-component}

En un formulario adaptable, un panel es un elemento contenedor que se puede utilizar para agrupar elementos de formularios relacionados. Permite agrupar y organizar distintos elementos de un formulario de una forma lógica y significativa. Esto puede mejorar la estructura general y la legibilidad del formulario, así como facilitar la comprensión y navegación a los usuarios.

Los paneles también se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, y mantener así el formulario simple y fácil de usar. También le permite incluir otros componentes, como texto, casilla de verificación, botón, etc.

También se puede utilizar para configurar diferentes acciones basadas en reglas, tales como enviar formularios, abrir un sitio web, mostrar u ocultar componentes o agregar una instancia de un panel.

{{traditional-aem}}

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Existen varias razones para utilizar un panel en un formulario, entre ellas, las siguientes:

- **Organización de elementos de formulario**: se puede utilizar un panel para agrupar los elementos de formularios relacionados, lo que facilita a los usuarios la comprensión y navegación.

- **Mejora de la estructura del formulario**: al agrupar los elementos del formulario en paneles, se puede mejorar la estructura general, la legibilidad y la comprensión del formulario.

- **Creación de secciones contraíbles**: los paneles se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, y mantenerlo de una forma simple y fácil de usar.

- **Mejora de la capacidad de uso**: al utilizar paneles para organizar los elementos de formulario, se puede utilizar de forma más sencilla y manejable, lo que puede generar tasas de finalización más altas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del contenedor de panel de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación, se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_es). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del contenedor de panel de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor del panel para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones del contenedor de panel con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/basic-panel.png)

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

- **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Repetir panel {#repeat-panel}

![pestaña repetir](/help/adaptive-forms/assets/repeat-panel.png)

Puede utilizar las opciones de repetibilidad para duplicar el contenedor de panel y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente contenedor de panel y acceder a su configuración, se presentan las siguientes opciones:

- **Hacer repetible el panel**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
- **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el contenedor de panel. El valor cero indica que el panel Asistente no se repite; el valor predeterminado es cero.
- **Máximo de repeticiones**: define el número máximo de veces que se puede repetir el contenedor de panel. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro del contenedor de panel, siga los pasos que se proporcionan en el artículo [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=es).

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/helpcontent-panel.png)

- **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.
   - **Texto personalizado**: seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado. Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   - **Descripción**: seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   - **Título**: seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   - **Nombre**: seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   - **Ninguno**: seleccione esta opción si no desea añadir etiquetas de accesibilidad de ARIA.

- **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de panel.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña de componentes permitidos del cuadro de diálogo Diseño](/help/adaptive-forms/assets/panel-container-allowed-component.png)

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente del editor de formularios adaptables.

### Pestaña Componentes predeterminados {#default-components-tab}

![Pestaña de componente predeterminada del cuadro de diálogo Diseño](/help/adaptive-forms/assets/panel-container-default-component.png)

La pestaña **Componentes predeterminados** facilita al editor de plantillas especificar los componentes visibles de forma predeterminada como elementos en el componente contenedor de formulario del editor de Formularios adaptables.

### Pestaña Configuración adaptable {#responsive-tab}

![Pestaña Configuración adaptable del cuadro de diálogo Diseño](/help/adaptive-forms/assets/panel-container-responsive-style-tab.png)

La pestaña **Configuración adaptable** permite al editor de plantillas especificar el número de columnas de la cuadrícula dentro del componente contenedor de formulario en el editor de Formularios adaptables.

### Pestaña Configuración de contenedor

![Pestaña Configuración de contenedor](/help/adaptive-forms/assets/panel-container-container-settings.png)

- **Diseño**: puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en su sitio, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear el Nombre, Segundo nombre y Apellido en un formulario en una sola fila.

- **Deshabilitar diseño**: seleccione esta opción para deshabilitar la selección de diseño en el cuadro de diálogo de edición de un componente.

- **Habilitar imagen de fondo**: esta opción permite al usuario configurar los ajustes del panel para incluir un fondo visual para mejorar el atractivo visual.

- **Habilitar el color de fondo**: esta opción le permite establecer o cambiar el color de fondo del panel. Esta función se utiliza comúnmente en el diseño de interfaz de usuario para personalizar el aspecto de los paneles dentro de una interfaz más grande. Al seleccionar la opción **Habilitar el color de fondo**, aparece la opción **Solo muestras**. La opción **Solo muestras** permite especificar o elegir colores para el fondo, el texto u otros elementos visuales dentro del panel utilizando el botón **Añadir**

### Pestaña Estilos {#styles-tab}

El componente principal de los archivos adjuntos de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/panel-container-styles-tab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal del contenedor de panel de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/panel-container-custom-properties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}