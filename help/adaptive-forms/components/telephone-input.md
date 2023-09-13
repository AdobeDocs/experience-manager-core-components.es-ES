---
title: 'Componente principal de formularios adaptables: entrada de teléfono'
description: Uso o personalización del componente principal de entrada del teléfono de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: d06179ac-04bd-4af4-b6ac-c4c78086058c
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: ht
source-wordcount: '1793'
ht-degree: 100%

---

# Entrada de teléfono {#telephone-input-adaptive-forms-core-component}

El componente principal de entrada de teléfono del formulario adaptable permite a los usuarios introducir un número de teléfono. El campo de entrada de teléfono muestra teclados en dispositivos móviles que son relevantes para números de teléfono. Se puede personalizar con atributos adicionales como “patrón” y “marcador de posición” para especificar el formato y la descripción del número de teléfono.

El campo de entrada de teléfono se utiliza comúnmente en formularios de contacto, de registro y otros formularios en los que se requiere un número de teléfono como medio de contacto. El campo de entrada telefónica también puede utilizarse para garantizar que el usuario introduzca un número de teléfono válido, ya que el explorador puede imponer ciertas restricciones, como la longitud y el formato del número de teléfono, según el atributo “patrón”.

## Uso {#reasons-to-use-telephone-input}

Los motivos comunes para utilizar un campo de entrada de teléfono en un formulario adaptable son los siguientes:

* **Información de contacto**: un campo de entrada de teléfono se utiliza comúnmente para recopilar el número de teléfono de un usuario como medio de contacto.

* **Precisión de datos mejorada**: al usar un campo de entrada telefónica, el formulario puede imponer ciertas restricciones en el formato del número de teléfono, lo que puede ayudar a garantizar que los datos introducidos sean precisos y completos.

* **Mejor experiencia del usuario**: el campo de entrada telefónica proporciona una manera clara e intuitiva para que los usuarios introduzcan su número de teléfono y puede mejorar la experiencia del usuario al permitir que los usuarios escriban su información de contacto rápida y fácilmente.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de entrada del teléfono del formulario adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de entrada de teléfono para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de entrada de teléfono con facilidad para una experiencia del usuario sin problemas.

![Pestaña Básicos](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Texto del marcador de posición**: el texto del marcador de posición de un componente de formulario hace referencia a una etiqueta o solicitud corta que aparece dentro de un campo de entrada como una sugerencia al usuario sobre qué tipo de información se espera que se introduzca en ese campo. El texto del marcador de posición desaparece cuando el usuario empieza a escribir en el campo y vuelve a aparecer si el campo se deja vacío. Proporciona una pista visual al usuario, pero no actúa como etiqueta o valor permanente para el campo.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.

* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

* **Valor predeterminado**: esta opción le permite agregar un valor predeterminado en un campo de formulario. Si **Componente desactivado** o **Componente de solo lectura** está seleccionado, el valor predeterminado se muestra en la pantalla. Si el usuario no introduce ningún valor en el campo del formulario, este valor se envía en el momento del envío del formulario.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básico** cuando se selecciona esta opción.

* **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo se deja en blanco.

* **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Número máximo de caracteres**: esta opción le permite especificar el número máximo de caracteres permitidos en el componente. Si introduce caracteres superiores al valor especificado en **Número máximo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado.

* **Mensaje de error de número máximo de caracteres**: el cuadro de diálogo **Mensaje de error del número máximo de caracteres** permite añadir un mensaje de error personalizado si introduce más caracteres que el valor especificado en **Número máximo de caracteres**.

* **Número mínimo de caracteres**: esta opción permite especificar el número mínimo de caracteres permitidos en el campo. Si introduce menos caracteres que el valor especificado en **Número mínimo de caracteres**, aparecerá un mensaje de error en la pantalla. El cuadro de diálogo **Mensaje de error de caracteres mínimos** permite agregar un mensaje de error personalizado.

* *Mensaje de error de caracteres mínimos**: el cuadro de diálogo **Mensaje de error de caracteres mínimos** le permite agregar un mensaje de error personalizado si introduce caracteres menores que el valor especificado en la opción **Número mínimo de caracteres**.

La opción **Patrón de validación** permite introducir un patrón para validar el número de teléfono escrito. El número de teléfono introducido se valida según el valor introducido en la opción **Patrón**. En el caso de que el número de teléfono no se valide con el valor introducido en la opción **Patrón**, el mensaje de error aparece en pantalla.

* **Patrón**: esta opción le permite introducir los patrones de verificación permitidos para el número de teléfono. También se permiten expresiones regulares.

* **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra en la pantalla si el número de teléfono introducido no se valida con el valor introducido en la opción **Patrón**

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active la opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: el texto de ayuda hace referencia a información o directrices adicionales que se proporcionan para ayudar a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

**Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente de entrada de teléfono.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de entrada de teléfono de formularios adaptables admite el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de entrada de teléfono de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Formatos {#format-tab}

La pestaña Formatos permite especificar formatos de número predeterminados y personalizados.

![Pestaña Formato](/help/adaptive-forms/assets/telephoneinput_format.png)

## Artículo relacionado {#related-article}

* [Creación de un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=es)

* [Creación de un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)


## Vea también {#see-also}

* [Acordeón](/help/adaptive-forms/components/accordion.md)
* [Botón](/help/adaptive-forms/components/button.md)
* [Casilla de verificación Grupo](/help/adaptive-forms/components/checkbox-group.md)
* [Selector de fecha](/help/adaptive-forms/components/date-picker.md)
* [Lista desplegable](/help/adaptive-forms/components/drop-down.md)
* [Entrada de correo electrónico](/help/adaptive-forms/components/email-input.md)
* [Contenedor del formulario](/help/adaptive-forms/components/form-container.md)
* [Archivo adjunto](/help/adaptive-forms/components/file-attachment.md)
* [Pie de página](/help/adaptive-forms/components/footer.md)
* [Encabezado](/help/adaptive-forms/components/header.md)
* [Pestañas horizontales](/help/adaptive-forms/components/horizontal-tabs.md)
* [Imagen](/help/adaptive-forms/components/image.md)
* [Entrada de número](/help/adaptive-forms/components/number-input.md)
* [Contenedor de panel](/help/adaptive-forms/components/panel-container.md)
* [Botón de opción](/help/adaptive-forms/components/radio-button.md)
* [Botón Restablecer](/help/adaptive-forms/components/reset-button.md)
* [Botón Enviar](/help/adaptive-forms/components/submit-button.md)
* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
* [Texto](/help/adaptive-forms/components/text.md)
* [Título](/help/adaptive-forms/components/title.md)
* [Asistente](/help/adaptive-forms/components/wizard.md)