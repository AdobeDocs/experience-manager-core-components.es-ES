---
title: Componente principal de Forms adaptable - Asistente
description: Uso o personalización del componente principal del asistente de Forms adaptable.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1847'
ht-degree: 2%

---

# Asistente {#wizard-adaptive-forms-core-component}

Una presentación del Asistente de un formulario adaptable hace referencia a un formulario dividido en varios pasos o páginas, y el usuario se mueve por el formulario de un paso a la vez. Este diseño se denomina &quot;asistente&quot; porque guía al usuario a través del formulario en un proceso paso a paso.

Cada paso del asistente suele contener un grupo de campos de formulario relacionados y un mecanismo de navegación, como los botones &quot;Siguiente&quot; y &quot;Atrás&quot;, para moverse entre los pasos. El usuario solo puede continuar con el paso siguiente una vez que se haya completado el paso actual y se hayan rellenado todos los campos obligatorios.

La presentación del asistente resulta útil para los formularios que tienen muchos campos o información que se deben recopilar, ya que desglosa el formulario en fragmentos más pequeños y manejables. También ayuda a los usuarios a centrarse en un conjunto de campos a la vez, lo que puede hacer que el proceso de rellenado de formularios sea menos abrumador.

Sin embargo, también puede aumentar la complejidad del formulario, ya que el usuario tiene que pasar por varias páginas para completar el formulario. Por lo tanto, es necesario evaluar los requisitos del formulario y las necesidades del usuario antes de decidir utilizar una presentación del asistente.

Puede utilizar la presentación del asistente Componente principal en un formulario adaptable para crear la presentación del asistente.


**Ejemplo**

![](/help/adaptive-forms/assets/wizard.png)

## Uso {#reasons-to-use-wizard-in-an-adaptive-form}

Existen varias razones por las que puede resultar beneficioso utilizar una presentación del Asistente en un formulario adaptable:

* **Simplicidad**: Desglosar un formulario en varios pasos puede facilitar a los usuarios la comprensión y la cumplimentación, ya que pueden centrarse en un conjunto de campos a la vez.

* **Organización**: Una presentación del asistente puede ayudar a organizar los formularios por tema o propósito, y también puede agrupar los campos relacionados, lo que puede hacer que el proceso de rellenado de formularios sea más lógico y eficiente.

* **Validación**: Una presentación del asistente permite la validación paso a paso, lo que puede ayudar a los usuarios a identificar y corregir los errores a medida que van, en lugar de esperar hasta el final del formulario.

* **Indicador de progreso**: Una presentación del asistente puede mostrar el progreso del formulario, lo que puede ayudar al usuario a comprender cuánto queda para completar el formulario.

* **Formularios largos**: Si el formulario tiene muchos campos, puede resultar abrumador que el usuario los vea a la vez, por lo que dividirlos en trozos más pequeños y manejables puede hacerlo menos intimidante.

* **Evitar el abandono**: Una presentación del asistente también puede ayudar a reducir el abandono del formulario, ya que es más probable que los usuarios completen un formulario si pueden ver el progreso y comprender cuánto queda por hacer.

* **Experiencia móvil**: Un diseño de asistente también puede ser beneficioso para los formularios a los que se accede desde dispositivos móviles, ya que permite que las páginas más pequeñas se carguen más rápido y sea más fácil navegar.

En general, una presentación del asistente puede hacer que el proceso de cumplimentación de formularios sea más manejable y eficaz para los usuarios, pero es importante tener en cuenta la complejidad del formulario y las necesidades del usuario antes de decidir utilizar este tipo de presentación.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de diseño del asistente de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posterior |
|---|---|---|
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/adaptive-forms/version.md) y posterior | Compatible con<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posterior pero inferior a 2.0.0. |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/adaptive-forms/version.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del título adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del asistente para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones del asistente con facilidad para una experiencia de usuario perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/wizard_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Ajuste de datos en un objeto** - Seleccione &quot;Ajuste de datos en un objeto&quot; para colocar los datos de campo del asistente dentro de un objeto JSON. Si no se elige, el JSON de datos de envío tiene una estructura plana para los campos del asistente.

* **Diseño** - Puede tener un diseño fijo (simple) o flexible (cuadrícula adaptable) para el asistente. El diseño simple mantiene todo fijo en el lugar, mientras que la cuadrícula interactiva le permite ajustar la posición de los componentes para adaptarlos a sus necesidades. Por ejemplo, utilice Cuadrícula interactiva para alinear &quot;Nombre&quot;, &quot;Nombre central&quot; y &quot;Apellido&quot; en un formulario en una sola fila.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.

* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Ficha Ayuda {#help-tab}

![Ficha Ayuda](/help/adaptive-forms/assets/wizard_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.


### Pestaña Accesibilidad {#accessibility}

![Ficha Básico](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.

* **función de HTML para que anuncie el lector de pantalla** - La función de HTML es un atributo utilizado para especificar el propósito de un elemento HTML para tecnologías de asistencia, como lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función &quot;etiqueta&quot; y su campo de entrada puede tener la función &quot;cuadro de texto&quot;. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarla correctamente al usuario.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño permite a los creadores de plantillas controlar cómo se muestran las cosas de forma predeterminada. Para el componente Asistente para Forms adaptable , puede establecer lo siguiente:

* Componentes principales que un creador de formularios puede agregar al asistente en el editor de Forms adaptable
* Nombres simples para estilos (clases CSS) que se pueden aplicar en el cuadro de diálogo de propiedades del componente Asistente del editor de Forms adaptable.

Esto ayuda a que el proceso de creación y personalización de formularios sea más sencillo y eficaz.

### Pestaña Componentes permitidos {#allowed-components-tab}

La variable **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden agregar como elementos a los paneles en el componente Asistente del editor de Forms adaptable.

![Pestañas Componentes permitidos](/help/adaptive-forms/assets/panel_allowedcomponent.png)

### Pestaña Componentes predeterminados {#default-component-tab}

Esta pestaña permite al editor de plantillas asignar los componentes que se pueden añadir como elementos a los paneles en el componente del asistente en el editor de Forms adaptable.

![Componente predeterminado del panel](/help/adaptive-forms/assets/panel_defaultcomponent.png)

### Configuración interactiva {#responsive-settings}

Esta pestaña permite que el editor de plantillas defina el número de columnas que se mostrarán en la cuadrícula interactiva.

![Cuadrícula interactiva](/help/adaptive-forms/assets/panel_responsivesettings.png)

### Pestaña Configuración de contenedor {#container-setting-tab}

La pestaña de configuración del contenedor permite establecer la posición de los componentes en el editor de Forms adaptable.

![Configuración del contenedor](/help/adaptive-forms/assets/panel_settings.png)

* **Diseño**: El diseño Simple mantiene todo fijo en el lugar, mientras que la Cuadrícula interactiva le permite cambiar la posición de los componentes para adaptarlos a sus necesidades.
* **Deshabilitar diseño**: También puede desactivar la selección de diseño en el cuadro de diálogo de edición seleccionando la opción **Deshabilitar diseño** casilla de verificación.
* **Habilitar imagen de fondo**: Esta pestaña permite establecer la imagen de fondo y el color en el editor de plantillas.
* **Habilitar color de fondo**: Esta pestaña permite establecer el color de fondo en el editor de plantillas.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar los estilos CSS de un componente. El componente principal del Asistente para Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Ficha Estilo](/help/adaptive-forms/assets/panel_style.png)

* **Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente Asistente.

* **Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

