---
title: 'Componente principal de Formularios adaptables: asistente'
description: Uso o personalización del componente principal del asistente de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: c3401da271efd930d1a2711bcab25c29f763f38e
workflow-type: tm+mt
source-wordcount: '2101'
ht-degree: 99%

---

# Componente Asistente{#wizard-adaptive-forms-core-component}

Un diseño de asistente de un formulario adaptable hace referencia a un formulario dividido en varios pasos o páginas, con el usuario moviéndose por el formulario paso a paso. Este diseño se denomina “asistente” porque guía al usuario a través del formulario en un proceso paso a paso.

Cada paso del asistente suele contener un grupo de campos de formulario relacionados y un mecanismo de navegación, como los botones “Siguiente” y “Atrás”, para moverse entre los pasos. El usuario solo puede continuar con el paso siguiente una vez que se haya completado el paso actual y se hayan rellenado todos los campos obligatorios.

El diseño de asistente resulta útil para los formularios que tienen muchos campos o información que se deben recopilar, ya que desglosa el formulario en fragmentos más pequeños y manejables. También ayuda a los usuarios a centrarse en un conjunto de campos a la vez, lo que puede hacer que el proceso de rellenado de formularios sea menos engorroso.

Sin embargo, también puede aumentar la complejidad del formulario, ya que el usuario tiene que pasar por varias páginas para completar el formulario. Por lo tanto, es necesario evaluar el requisito del formulario y las necesidades del usuario antes de decidir utilizar un diseño de asistente.
Puede utilizar el componente principal de diseño de asistente en un formulario adaptable para crear el diseño del asistente.

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/wizard.png)

## Uso {#reasons-to-use-wizard-in-an-adaptive-form}

Existen varias razones por las que puede resultar beneficioso utilizar un diseño de asistente en un formulario adaptable:

- **Simplicidad**: desglosar un formulario en varios pasos puede facilitar a los usuarios su comprensión y cumplimentación, dado que pueden centrarse en un conjunto de campos a la vez.

- **Organización**: un diseño de asistente puede ayudar a organizar los formularios por tema o propósito, y también puede agrupar los campos relacionados, lo que puede hacer que el proceso de rellenado de formularios sea más lógico y eficiente.

- **Validación**: un diseño de asistente permite la validación paso a paso, lo que puede ayudar a los usuarios a identificar y corregir los errores sobre la marcha, en lugar de esperar hasta el final del formulario.

- **Indicador de progreso**: un diseño de asistente puede mostrar el progreso del formulario, lo que puede ayudar al usuario a comprender cuánto queda para completarlo.

- **Formularios largos**: si el formulario tiene muchos campos, puede resultar agobiante para el usuario verlos todos a la vez; por consiguiente, dividirlos en fragmentos más pequeños y manejables puede hacerlo más simple.

- **Evitar el abandono**: un diseño de asistente también puede ayudar a reducir el abandono del formulario, ya que es más probable que los usuarios completen un formulario si pueden ver el progreso y comprender cuánto queda por hacer.

- **Experiencia móvil**: un diseño de asistente también puede ser beneficioso para los formularios a los que se accede desde dispositivos móviles, ya que permite que las páginas más pequeñas se carguen más rápido y sean más fáciles de recorrer.

En general, un diseño de asistente puede hacer que el proceso de cumplimentación de formularios sea más manejable y eficaz para los usuarios, pero es importante tener en cuenta la complejidad del formulario y las necesidades del usuario antes de decidir utilizar este tipo de diseño.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de diseño de asistente de Formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de título de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del asistente para los visitantes con el cuadro de diálogo Configurar. También puede definir las opciones del asistente con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/wizard-basic.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece encima del componente.

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

<!--   **Wrap data in an object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

-   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row.  -->

- **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Asistente de repetición {#repeat-wizard-tab}

![Asistente de repetición](/help/adaptive-forms/assets/wizard-repeat.png)

Puede utilizar las opciones de repetibilidad para duplicar el asistente y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente Asistente y acceder a su configuración, se presentan las siguientes opciones:

- **Hacer que el asistente sea repetible**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
- **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el panel Asistente. El valor cero indica que el panel Asistente no se repite; el valor predeterminado es cero.
- **Máximo de repeticiones**: define el número máximo de veces que se puede repetir el panel Asistente. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro del asistente, siga los pasos que se proporcionan en el artículo [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=es).

### Pestaña Elementos {#items-tab}

![Pestaña Elementos](/help/adaptive-forms/assets/wizard_itemstab.png)

Esta opción le permite agregar componentes de formulario adaptable al hacer clic en el botón Agregar, que aparece de forma predeterminada cuando el asistente se agrega en modo de edición.

### Pestaña Ayuda {#help-tab}

![Pestaña Ayuda](/help/adaptive-forms/assets/wizard_helptab.png)

- **Descripción breve**: una breve descripción es una corta explicación de texto que proporciona información o aclaración adicionales sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

- **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

- **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.


### Pestaña Accesibilidad {#accessibility}

![Pestaña de accesibilidad](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

- **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

- **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente Asistente de Formularios adaptables, puede establecer lo siguiente:

- Los componentes principales que un creador de formularios puede añadir al asistente en el editor de formularios adaptables
- Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente Asistente del editor de formularios adaptables.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña Componentes permitidos](/help/adaptive-forms/assets/tabs-allowed-component.png)

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente Asistente del editor de formularios adaptables.

### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El Componente principal Asistente de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Estilos](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal del asistente de Formularios adaptables.

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