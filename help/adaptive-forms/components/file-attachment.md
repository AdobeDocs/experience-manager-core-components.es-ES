---
title: 'Componente principal de Forms adaptable: archivo adjunto'
description: Uso o personalización del componente principal del archivo adjunto de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Archivo adjunto {#file-attachment-adaptive-forms-core-component}

Un componente de archivo adjunto en un formulario adaptable permite a los usuarios seleccionar y cargar archivos desde su equipo o dispositivo local. El componente de archivo adjunto se puede configurar para permitir tipos de archivo específicos, límites de tamaño y varios archivos adjuntos.

**Ejemplo**

![](/help/adaptive-forms/assets/upload-image.png)


## Uso {#reasons-to-use-file-attachment}

Existen varias razones por las que resulta beneficioso incluir un componente de archivo adjunto en un formulario adaptable, entre ellas:

* **Recopilación de información adicional**: Un componente de archivo adjunto permite a los usuarios cargar documentos, imágenes, vídeos u otros tipos de archivos como parte del envío del formulario. Esto puede resultar útil para recopilar información adicional como resúmenes, portafolios o documentación de apoyo.

* **Uso compartido sencillo de archivos grandes**: El componente de archivo adjunto permite a los usuarios compartir archivos de gran tamaño fácilmente, sin tener que depender de servicios externos de uso compartido de archivos.

* **Conveniencia**: El componente de archivo adjunto permite a los usuarios cargar archivos desde su equipo local, sin tener que desplazarse fuera del formulario ni utilizar otras herramientas.

* **Análisis de datos**: El componente de archivo adjunto se puede utilizar para recopilar datos de varias fuentes y analizarlos, o para utilizarlo como entrada para un procesamiento posterior.

* **Experiencia del usuario**: El componente de archivo adjunto se puede utilizar para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de cargar archivos.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de los archivos adjuntos adaptables de Forms se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de los archivos adjuntos de Forms adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de archivo adjunto para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de archivo adjunto con facilidad para que el usuario pueda disfrutar de una experiencia óptima.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Ocultar título** - Seleccione la opción para ocultar el título del componente.

* **Título del botón** - Esta opción se utiliza para definir la etiqueta del botón mostrado en un formulario adaptable.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Deshabilitar componente** - Seleccione la opción para desactivar el componente. El componente deshabilitado no está activo ni puede editarlo el usuario final. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.
* **Permitir varios archivos adjuntos** - Seleccione esta opción para cargar varios archivos adjuntos mediante el **Archivo adjunto** botón.

### Ficha Validación {#validation-tab}

![Ficha Validación](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Requerido** - Seleccione esta opción si desea mostrar el componente en un formulario adaptable. No puede seleccionar la variable **Ocultar componente** o **Deshabilitar componente**  en el **Básico** cuando se selecciona esta opción.

* **Mensaje de error** - Esta opción le permite introducir un mensaje que se muestra si la variable **Requerido** está activada y el campo se deja en blanco.

* **Mensaje de validación de secuencia de comandos** - Esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

* **Mensaje de error mínimo de archivos** - Esta opción se utiliza para introducir un mensaje de error que se muestra si se cargan archivos que no sean el número mínimo especificado de archivos.

* **Mensaje de error máximo de archivos** - Esta opción se utiliza para introducir un mensaje de error que se muestra si se cargan archivos buenos al número máximo especificado de archivos.

* **Tamaño máximo del archivo (MB)** - Esta opción permite especificar un tamaño máximo de archivo. Los tamaños de archivo se especifican en MB.

* **Mensaje de error de tamaño máximo de archivo** - Esta opción se utiliza para introducir un mensaje de error que se muestra si se cargan archivos de tamaño superior al tamaño de archivo especificado en **Tamaño máximo del archivo (MB)** .

* **Tipos de archivo permitidos** : varios tipos de archivos que se pueden cargar mediante el **Archivo adjunto** se añaden aquí. También permite añadir un nuevo formato de archivo haciendo clic en el **Agregar** botón. Los formatos de archivo admitidos son: audio, vídeo, imagen, texto o PDF. También puede eliminar o reorganizar los tipos de archivo permitidos mediante:
   * **Eliminar** - Toque o haga clic para eliminar tipos de archivos específicos.
   * **Reorganizar** - Toque o haga clic y arrastre para reorganizar el orden de los tipos de archivo permitidos.

* **Mensaje de error de tipo de archivo** - Esta opción le permite introducir un mensaje de error que se muestra al cargar los formatos de archivo distintos de los que aparecen en la **Tipos de archivo permitidos** .

### Ficha Contenido de ayuda {#help-content-tab}

![Ficha Contenido de ayuda](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Descripción breve** : una breve descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de un campo de formulario específico. Ayuda al usuario a comprender qué tipo de datos se deben introducir en el campo y puede proporcionar directrices o ejemplos para garantizar que la información introducida sea válida y cumpla los criterios deseados. De forma predeterminada, las descripciones cortas permanecen ocultas. Active la variable **Mostrar siempre una descripción breve** para mostrarlo debajo del componente.

* **Mostrar siempre una descripción breve** - Active la opción para mostrar la breve descripción debajo del componente.

* **Texto de ayuda** - El texto de ayuda hace referencia a información o directrices adicionales que se proporcionan al usuario para ayudarles a rellenar correctamente un campo de formulario. Aparece cuando el usuario hace clic en el icono de ayuda (i) situado junto al componente. El texto de ayuda proporciona información más detallada que la etiqueta de un campo de formulario o el texto del marcador de posición, y está diseñado para ayudar al usuario a comprender los requisitos o restricciones del campo. También puede ofrecer sugerencias o ejemplos para que el formulario sea más fácil y preciso.

![Ficha Accesibilidad](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texto para lectores de pantalla** - El texto para lectores de pantalla se refiere a texto adicional que está específicamente diseñado para ser leído por tecnologías de asistencia, como lectores de pantalla, utilizadas por personas con deficiencias visuales. Este texto proporciona una descripción en audio del propósito del campo de formulario y puede incluir información sobre el título, la descripción, el nombre y cualquier mensaje relevante (texto personalizado) del campo. El texto del lector de pantalla ayuda a garantizar que el formulario sea accesible para todos los usuarios, incluidos los que tengan deficiencias visuales, y les ofrece una comprensión completa del campo del formulario y de sus requisitos.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Archivo adjunto.

### Pestaña Estilos {#styles-tab}

El componente principal de los archivos adjuntos de Forms adaptables es compatible con la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de los archivos adjuntos adaptables de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.
