---
title: 'Componente principal de formularios adaptables: contenedor de panel'
description: Uso o personalización del componente principal del contenedor de panel de formularios adaptables.
role: Architect, Developer, Admin, User
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 87%

---

# Contenedor de panel {#panel-container-adaptive-forms-core-component}

En un formulario adaptable, un panel es un elemento contenedor que se puede utilizar para agrupar elementos de formularios relacionados. Permite agrupar y organizar distintos elementos de un formulario de una forma lógica y significativa. Esto puede mejorar la estructura general y la legibilidad del formulario, así como facilitar la comprensión y navegación a los usuarios.

Los paneles también se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, y mantener así el formulario simple y fácil de usar. También le permite incluir otros componentes, como texto, casilla de verificación, botón, etc.

También se puede utilizar para configurar diferentes acciones basadas en reglas, tales como enviar formularios, abrir un sitio web, mostrar u ocultar componentes o agregar una instancia de un panel.

**Ejemplo**

![](/help/adaptive-forms/assets/panel-container.png)

## Uso {#reasons-to-use-panel-container}

Existen varias razones para utilizar un panel en un formulario, entre ellas, las siguientes:

* **Organización de elementos de formulario**: se puede utilizar un panel para agrupar los elementos de formularios relacionados, lo que facilita a los usuarios la comprensión y navegación.

* **Mejora de la estructura del formulario**: al agrupar los elementos del formulario en paneles, se puede mejorar la estructura general, la legibilidad y la comprensión del formulario.

* **Creación de secciones contraíbles**: los paneles se pueden utilizar para crear secciones contraíbles, lo que puede resultar útil para ocultar campos de formulario complejos o utilizados con menos frecuencia, y mantenerlo de una forma simple y fácil de usar.

* **Mejora de la capacidad de uso**: al utilizar paneles para organizar los elementos de formulario, se puede utilizar de forma más sencilla y manejable, lo que puede generar tasas de finalización más altas.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del contenedor de panel de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación, se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/versions.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del contenedor de panel de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor del panel para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones del contenedor de panel con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/basic-panel.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Ajustar datos en objeto**: seleccione “Ajustar los datos en un objeto” para colocar los datos del asistente dentro de un objeto JSON. Si no se selecciona, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño**: puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en su sitio, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear el Nombre, Segundo nombre y Apellido en un formulario en una sola fila.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Repetir panel {#repeat-panel}

![pestaña repetir](/help/adaptive-forms/assets/repeat-panel.png)

Puede utilizar las opciones de repetibilidad para duplicar el contenedor de panel y sus componentes secundarios, definir un recuento de repetición mínimo y máximo y facilitar la replicación de secciones similares dentro de un formulario. Al interactuar con el componente contenedor de panel y acceder a su configuración, se presentan las siguientes opciones:

* **Hacer que el asistente sea repetible**: función de alternancia que permite a los usuarios habilitar o deshabilitar la funcionalidad de repetibilidad.
* **Repeticiones mínimas**: establece el número mínimo de veces que se puede repetir el contenedor de panel. El valor cero indica que el panel Asistente no se repite; el valor predeterminado es cero.
* **Máximo de repeticiones**: define el número máximo de veces que se puede repetir el contenedor de panel. De forma predeterminada, este valor es ilimitado.

Para administrar de forma eficaz las secciones repetibles dentro del contenedor de panel, siga los pasos que se proporcionan en la [Crear formularios con secciones repetibles](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artículo.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/helpcontent-panel.png)


* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/accessibilty-panel.png)


* **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

* **Función de HTML para el anuncio del lector de pantalla**: la función de HTML es un atributo que se utiliza para especificar la finalidad de un elemento HTML para tecnologías de asistencia, como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

## Artículo relacionado {#related-article}

* [Crear un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Crear un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)
