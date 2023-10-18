---
title: 'Componente principal de formularios adaptables: botón'
description: Uso o personalización del componente principal de botón de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
source-git-commit: 0026734a2e43c51c7f5af2b37492d61e8f779ac7
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 100%

---

# Componente Botón  {#button-component-adaptive-forms-core-component}

El botón de un formulario adaptable es un elemento de la IU que permite a los usuarios iniciar una acción cuando hacen clic en él. El elemento botón puede usarse para enviar un formulario, restablecerlo o realizar otras acciones, como desplazarse a una página diferente o activar el código personalizado. El botón se puede crear con el componente principal de botón.

El editor de reglas de formularios adaptables permite a los usuarios establecer distintas acciones para el componente de botón. Estas acciones incluyen abrir un sitio web, mostrar u ocultar componentes de formulario, agregar una instancia de un panel o componente, enviar o restablecer un formulario, etc.

Los Formularios adaptables incorporan componentes independientes para el [botón Enviar](/help/adaptive-forms/components/submit-button.md) y el [botón Restablecer](/help/adaptive-forms/components/reset-button.md), lo que permite a los usuarios enviar o restablecer cómodamente un formulario. El componente Botón se puede configurar de forma flexible para ejecutar estas acciones según necesidades específicas.

Los usuarios pueden acceder a la lista completa de acciones compatibles con el componente de botón mediante el editor de reglas de formularios adaptables. El editor de reglas permite a los usuarios crear reglas que se activan mediante varios eventos, como cuando se hace clic en un botón, se carga un formulario o cambia un valor de campo. Estas reglas se pueden emplear para diversas acciones, como mostrar u ocultar componentes, configurar valores de campo o enviar el formulario.

## Uso {#reasons-to-use-button}

Existen varias razones por las que resulta beneficioso incluir un botón en un formulario adaptable, entre ellas, las siguientes:

* **Envío de formulario**: un botón suele utilizarse para enviar un formulario, lo que permite a los usuarios enviar los datos introducidos al servidor para su procesamiento.

* **Restablecimiento del formulario**: también se pueden aprovechar los botones para restablecer un formulario, lo que borra todos los datos introducidos por el usuario.

* **Navegación**: se pueden utilizar botones para desplazarse entre las diferentes secciones de un formulario o entre páginas diferentes de un sitio web.

* **Gestión de eventos**: los botones se pueden utilizar para activar diferentes eventos como abrir una página web, mostrar/ocultar componentes, añadir una instancia de un panel o componente al botón.

* **Interactividad**: los botones se pueden utilizar para crear formularios interactivos. Por ejemplo, se puede usar un botón para abrir un cuadro de diálogo modal o para alternar una sección del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de botón de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de botones para los visitantes con el cuadro de diálogo de configuración. También puede definir propiedades de botón con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/button_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Referencia de vínculo**: una referencia de vínculo es una referencia a un elemento de datos que se almacena en una fuente de datos externa y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

* **Referencia de vínculo de documento de registro**: esta opción le permite asociar un campo del formulario adaptable al campo Documento de registro. Cuando el usuario introduce cualquier valor en un campo vinculado de un formulario adaptable, ese valor también aparece en el campo vinculado del documento de registro correspondiente. Por ejemplo, se puede utilizar una referencia de vínculo de documento de registro para mostrar el nombre y la dirección de un cliente en un documento de registro, en función del ID introducido en el formulario por el cliente. De este modo, AEM Forms le permite generar un documento de registro y ofrece una experiencia del usuario perfecta para recopilar y administrar datos.

* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Contenido de ayuda {#help-content}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/button_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Accesibilidad {#accessibility}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/button_accessibilitytab.png)


* **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de botón.

### Pestaña Estilos {#styles-tab}

El componente principal de botón de formularios adaptables es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/button_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de botón de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

>[!MORELIKETHIS]
>
>* [Acordeón](/help/adaptive-forms/components/accordion.md)
>* [Grupo de casillas de verificación](/help/adaptive-forms/components/checkbox-group.md)
>* [Selector de fecha](/help/adaptive-forms/components/date-picker.md)
>* [Lista desplegable](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de correo electrónico](/help/adaptive-forms/components/email-input.md)
>* [Contenedor del formulario](/help/adaptive-forms/components/form-container.md)
>* [Archivo adjunto](/help/adaptive-forms/components/file-attachment.md)
>* [Pie de página](/help/adaptive-forms/components/footer.md)
>* [Encabezado](/help/adaptive-forms/components/header.md)
>* [Pestañas horizontales](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagen](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Contenedor de panel](/help/adaptive-forms/components/panel-container.md)
>* [Botón de opción](/help/adaptive-forms/components/radio-button.md)
>* [Botón Restablecer](/help/adaptive-forms/components/reset-button.md)
>* [Botón Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de teléfono](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Asistente](/help/adaptive-forms/components/wizard.md)


## Vea también {#see-also}

{{see-also}}

