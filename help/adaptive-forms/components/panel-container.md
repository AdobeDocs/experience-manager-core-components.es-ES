---
title: 'Componente principal de Forms adaptable: contenedor de panel'
description: Uso o personalización del componente principal del contenedor del panel adaptable de Forms.
role: Architect, Developer, Admin, User
source-git-commit: 77ff7425be1e591b8f5b973a344d7def8191c033
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 2%

---


# Contenedor de panel {#panel-container-adaptive-forms-core-component}

En un formulario adaptable, un panel es un elemento contenedor que se puede utilizar para agrupar elementos de formulario relacionados. Permite agrupar y organizar distintos elementos de formulario de una forma lógica y significativa. Esto puede ayudar a mejorar la estructura general y la legibilidad del formulario, facilitando a los usuarios su comprensión y navegación.

Los paneles también se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, lo que mantiene el formulario sencillo y fácil de usar. También le permite incluir otros componentes, como texto, casilla de verificación, botón, etc.

También se puede utilizar para configurar diferentes acciones basadas en reglas, como enviar formularios, abrir un sitio web, mostrar u ocultar componentes o agregar una instancia de un panel.

**Ejemplo**

![](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Existen varias razones para utilizar un panel en un formulario, entre ellas:

* **Organización de elementos de formulario**: Se puede utilizar un panel para agrupar elementos de formulario relacionados, lo que facilita a los usuarios la comprensión y navegación del formulario.

* **Mejora de la estructura del formulario**: Al agrupar los elementos de formulario en paneles, se puede mejorar la estructura general y la legibilidad del formulario, facilitando su comprensión.

* **Creación de secciones contraídas**: Los paneles se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, lo que mantiene el formulario sencillo y fácil de usar.

* **Mejora del uso**: Al utilizar paneles para organizar los elementos de formulario, el formulario se puede utilizar de forma más sencilla y sencilla, lo que puede generar tasas de finalización más altas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del contenedor del panel adaptable de Forms se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service |
|--- |--- |---|---|
| Versión 1 | Compatible  con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del contenedor del panel adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor del panel para los visitantes con el cuadro de diálogo Configurar . También puede definir opciones de contenedor de panel con facilidad para que la experiencia de usuario sea perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/panelcontainer_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Ajustar datos en objeto** - Seleccione &quot;Ajuste de datos en un objeto&quot; para colocar los datos de campo del asistente dentro de un objeto JSON. Si no se elige, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño** - Puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en el lugar, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear &quot;Nombre&quot;, &quot;Nombre central&quot; y &quot;Apellido&quot; en un formulario en una sola fila.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Ficha Contenido de ayuda {#help-content}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/panelcontainer_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Ficha Accesibilidad](/help/adaptive-forms/assets/panelcontainer_accessibilitytab.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

* **función de HTML para que anuncie el lector de pantalla** - La función de HTML es un atributo utilizado para especificar el propósito de un elemento HTML para tecnologías de asistencia, como lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función &quot;etiqueta&quot; y su campo de entrada puede tener la función &quot;cuadro de texto&quot;. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarla correctamente al usuario.

## Cuadro de diálogo de diseño {#design-dialog}



