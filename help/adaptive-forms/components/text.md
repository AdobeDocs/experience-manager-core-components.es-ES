---
title: 'Componente principal de Forms adaptable: texto '
description: Uso o personalización del componente principal de texto de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 3%

---


# Texto {#text-adaptive-forms-core-component}

En un formulario adaptable, el texto hace referencia al contenido que se muestra en el formulario para que el usuario lo lea. Esto puede incluir el texto que se utiliza para etiquetar un grupo de elementos de formulario, como campos de texto, así como cualquier instrucción o información adicional que se proporcione al usuario.

Esto también puede ayudar a dividir la estructura de un formulario en secciones lógicas, facilitando a los usuarios la comprensión y la finalización del formulario. Además, podría utilizarse con fines de accesibilidad para proporcionar una breve descripción del elemento al que está asociado. Este campo de texto suele mostrarse cerca de los componentes del formulario, como antes o después de él.

**Ejemplo**

![](/help/adaptive-forms/assets/text.png)

## Uso {#reasons-to-use-text-label}

Hay varias razones para utilizar texto en un formulario:

* **Proporcionar instrucciones**: Se puede utilizar el texto para proporcionar instrucciones sobre cómo rellenar el formulario o qué información se necesita.

* **Proporcionar contexto**: El texto se puede utilizar para proporcionar contexto al formulario, como explicar el propósito del formulario o la organización que recopila la información.

* **Dividir el formulario en secciones lógicas**: El texto se puede utilizar para dividir un formulario en secciones lógicas, lo que facilita a los usuarios comprender y completar el formulario.

* **Marcas e identidad**: El texto se puede utilizar con fines de marca e identidad, como incluir el nombre de la organización en el formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de texto de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service |
|--- |--- |---|---|
| Versión 1 | Compatible  con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de texto adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de texto para los visitantes con el cuadro de diálogo Configurar . También puede definir opciones de texto con facilidad para una experiencia de usuario perfecta.

![Ficha Básico](/help/adaptive-forms/assets/text_properties.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Referencia de enlace** - Una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados del origen de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar el origen de datos con los datos introducidos en el formulario. De este modo, AEM Forms permite crear formularios que interactúen con orígenes de datos externos, lo que proporciona una experiencia de usuario perfecta para recopilar y administrar datos.
* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Texto.


### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de texto de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de texto de Forms adaptable.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.
