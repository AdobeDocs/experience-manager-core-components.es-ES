---
title: 'Componente principal de formularios adaptables: adjuntar archivos'
description: Uso o personalización del componente principal para adjuntar archivos de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1580'
ht-degree: 100%

---

# Adjuntar archivos {#file-attachment-adaptive-forms-core-component}

El componente para adjuntar archivos de un Formulario adaptable permite a los usuarios seleccionar y cargar archivos desde su equipo o dispositivo local. El componente para adjuntar archivos se puede configurar para permitir tipos y límites de archivo de tamaño específicos y varios adjuntos de archivos.

**Ejemplo**

![](/help/adaptive-forms/assets/upload-image.png)


## Uso {#reasons-to-use-file-attachment}

Existen varias razones por las que resulta beneficioso incluir un componente para adjuntar archivos en un Formulario adaptable, entre ellas, las siguientes:

* **Recopilación de información adicional**: un componente para adjuntar archivos permite a los usuarios cargar documentos, imágenes, vídeos u otros tipos de archivos como parte del envío del formulario. Esto puede resultar útil para recopilar información adicional como resúmenes, portafolios o documentación de soporte.

* **Compartir fácilmente archivos grandes**: el componente para adjuntar archivos permite a los usuarios compartir fácilmente archivos de gran tamaño, sin tener que depender de servicios de uso compartido de archivos externos.

* **Comodidad**: el componente de archivo adjunto permite a los usuarios cargar archivos desde su equipo local, sin tener que desplazarse fuera del formulario ni utilizar otras herramientas.

* **Análisis de datos**: el componente de archivo adjunto se puede utilizar para recopilar datos de varias fuentes y analizarlos, o utilizarlo como entrada para un procesamiento posterior.

* **Experiencia del usuario**: el componente de archivo adjunto se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de cargar archivos.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de archivos adjuntos de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de archivo adjunto para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de archivo adjunto con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título**: seleccione la opción para ocultar el título del componente.

* **Título del botón**: esta opción se utiliza para definir la etiqueta del botón mostrado en un Formulario adaptable.

* **Referencia de enlace**: es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Permitir varios archivos adjuntos**: seleccione esta opción para cargar varios archivos adjuntos con el botón **Archivo adjunto**.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Obligatorio**: seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar **Ocultar componente** o **Desactivar componente** en la pestaña **Básico** cuando se selecciona esta opción.

* **Mensaje de error**: esta opción permite introducir un mensaje que se muestra si se marca la casilla **Obligatorio** y el campo se deja en blanco.

* **Mensaje de validación de la secuencia de comandos**: esta opción le permite escribir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Mensaje de error de archivos mínimo**: esta opción se utiliza para escribir un mensaje de error que se muestra si se cargan archivos por debajo de la cantidad mínima especificada de archivos.

* **Mensaje de error de archivos máximo**: esta opción se utiliza para escribir un mensaje de error que se muestra si se cargan archivos por encima de la cantidad mínima especificada de archivos.

* **Tamaño máximo del archivo (MB)**: esta opción permite especificar un tamaño máximo de archivo. Los tamaños de archivo se especifican en MB.

* **Mensaje de error de tamaño de archivo máximo**: esta opción se utiliza para escribir un mensaje de error que se muestra si se cargan archivos de tamaño superior al tamaño de archivo especificado en la opción de **Tamaño máximo del archivo (MB)**.

* **Tipos de archivo permitidos**: aquí se pueden cargar varios tipos de archivos mediante el botón de **Adjuntar archivo**. También permite agregar un nuevo formato de archivo haciendo clic en el botón de **Agregar**. Los formatos de archivo admitidos son: audio, vídeo, imagen, texto o PDF. También puede eliminar o reorganizar los tipos de archivo permitidos mediante:
   * **Eliminar**: pulse o haga clic para eliminar tipos de archivos específicos.
   * **Reorganizar**: pulse o haga clic y arrastre para reorganizar el orden de los tipos de archivo permitidos.

* **Mensaje de error de tipo de archivo**: esta opción le permite introducir un mensaje de error que se muestra al cargar los formatos de archivo distintos de los que aparecen en la opción de **Tipos de archivo permitidos**.

### Pestaña Contenido de ayuda {#help-content-tab}

![Pestaña Contenido de ayuda](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Descripción breve**: una descripción breve es una explicación de texto corta que proporciona información adicional o aclaraciones acerca del propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben escribir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la opción **Mostrar siempre una descripción breve** para mostrarla debajo del componente.

* **Mostrar siempre una descripción breve**: active esta opción para mostrar la descripción breve debajo del componente.

* **Texto de ayuda**: este hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarle a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

### Pestaña Accesibilidad {#accessibility-tab}


![Pestaña Accesibilidad](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texto para lectores de pantalla**: el texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para que lo lean tecnologías de asistencia, como lectores de pantalla, que utilizan personas con deficiencias visuales. Este texto proporciona una descripción del audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrezca una comprensión completa del campo del formulario y de sus requisitos.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Archivo adjunto.

### Pestaña Estilos {#styles-tab}

El componente principal de los archivos adjuntos de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño de archivos adjuntos](/help/adaptive-forms/assets/fileattachment_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar clases CSS predeterminadas para el componente principal de los archivos adjuntos de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

## Artículo relacionado {#related-article}

* [Creación de un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=es)

* [Creación de un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)


>[!MORELIKETHIS]
>
>* [Acordeón](/help/adaptive-forms/components/accordion.md)
>* [Botón](/help/adaptive-forms/components/button.md)
>* [Grupo de casillas de verificación](/help/adaptive-forms/components/checkbox-group.md)
>* [Selector de fecha](/help/adaptive-forms/components/date-picker.md)
>* [Lista desplegable](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de correo electrónico](/help/adaptive-forms/components/email-input.md)
>* [Contenedor del formulario](/help/adaptive-forms/components/form-container.md)
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