---
title: 'Componente principal de Forms adaptable: botón'
description: Uso o personalización del botón Forms adaptable Componente principal.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 2%

---


# Componente Botón  {#button-component-adaptive-forms-core-component}

Un botón de un formulario adaptable es un elemento de la interfaz de usuario que permite a los usuarios iniciar una acción cuando hacen clic en él. El elemento de botón puede utilizarse para enviar un formulario, restablecer un formulario o realizar otras acciones, como desplazarse a una página diferente o activar el código personalizado. El botón se puede crear con el componente principal de botón.

El Editor de reglas de Forms adaptable permite a los usuarios establecer distintas acciones para el componente de botón. Estas acciones incluyen abrir un sitio web, mostrar u ocultar componentes de formulario, agregar una instancia de un panel o componente, enviar o restablecer un formulario, etc.

Adaptive Forms también proporciona componentes de botón independientes para enviar o restablecer un formulario, pero el componente de botón también se puede configurar para realizar estas acciones si es necesario.

Los usuarios pueden acceder a la lista completa de acciones compatibles con el componente de botón mediante el Editor de reglas de Forms adaptable. El Editor de reglas permite a los usuarios crear reglas que se activan mediante varios eventos, como cuando se hace clic en un botón, cuando se carga un formulario o cuando cambia un valor de campo. Estas reglas se pueden utilizar para realizar diversas acciones, como mostrar u ocultar componentes, configurar valores de campo o enviar el formulario.

## Uso {#reasons-to-use-button}

Existen varias razones por las que resulta beneficioso incluir un botón en un formulario adaptable, entre ellas:

* **Envío de formulario**: Un botón suele utilizarse para enviar un formulario, lo que permite a los usuarios enviar los datos introducidos al servidor para su procesamiento.

* **Restablecimiento del formulario**: También se pueden utilizar botones para restablecer un formulario, borrando todos los datos introducidos por el usuario.

* **Navegación**: Se pueden utilizar botones para desplazarse entre las diferentes secciones de un formulario o entre páginas diferentes de un sitio web.

* **Gestión de eventos**: Los botones se pueden utilizar para almacenar en déclencheur distintos eventos, como abrir un sitio web, mostrar u ocultar componentes, agregar una instancia de un panel o componente al botón.

* **Interactividad**: Los botones se pueden utilizar para crear formularios interactivos. Por ejemplo, se puede utilizar un botón para abrir un cuadro de diálogo modal o para alternar una sección del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del botón adaptable de Forms v1 se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del botón adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia con los botones para los visitantes con el cuadro de diálogo Configurar . También puede definir propiedades de botón con facilidad para que la experiencia de usuario sea perfecta.

### Ficha básica {#basic-tab}

![Ficha básica](/help/adaptive-forms/assets/button_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.

* **Documento de referencia de enlace de registro** - Esta opción le permite asociar un campo Formulario adaptable al campo Documento de registro. Cuando el usuario introduce cualquier valor en un campo vinculado de un formulario adaptable, ese valor también aparece en el campo vinculado del documento de registro correspondiente. Por ejemplo, se puede utilizar una referencia de enlace de documento de registro para mostrar el nombre y la dirección de un cliente en un documento de registro, en función del ID introducido en el formulario por el cliente. De este modo, AEM Forms le permite generar un documento de registro y ofrece una experiencia de usuario perfecta para recopilar y administrar datos.

* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Ficha Contenido de ayuda {#help-content}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/button_helptab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Accesibilidad {#accessibility}

![Ficha Accesibilidad](/help/adaptive-forms/assets/button_accessibilitytab.png)


En el **Accesibilidad** , los valores se establecen para [Accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) etiquetas para el componente. Hay varias opciones disponibles para usar el texto del lector de pantalla:

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.


   * **Texto personalizado**: Seleccione esta opción para utilizar el texto personalizado para las etiquetas de accesibilidad de ARIA. Al seleccionar esta opción, aparece el cuadro de diálogo Texto personalizado . Puede agregar información relevante en el cuadro de diálogo Texto personalizado.
   * **Descripción**: Seleccione esta opción para utilizar la descripción para las etiquetas de accesibilidad de ARIA.
   * **Título**: Seleccione esta opción para utilizar el título para las etiquetas de accesibilidad de ARIA.
   * **Nombre**: Seleccione esta opción para utilizar el nombre para las etiquetas de accesibilidad de ARIA.
   * **Ninguna**: Seleccione esta opción si no desea agregar para etiquetas de accesibilidad de ARIA.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de botón.

### Pestaña Estilos {#styles-tab}

El componente principal del botón Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del botón adaptable de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.
