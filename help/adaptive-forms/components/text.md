---
title: 'Componente principal de formularios adaptables: texto'
description: Uso o personalización del componente principal de texto de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 100%

---

# Texto {#text-adaptive-forms-core-component}

En un formulario adaptable, el texto hace referencia al contenido que se muestra en el formulario para que el usuario lo lea. Esto puede incluir el texto que se utiliza para etiquetar un grupo de elementos de formulario, como los campos de texto, así como cualquier instrucción o información adicional que se proporcione al usuario.

Esto también puede ayudar a dividir la estructura de un formulario en secciones lógicas, facilitando a los usuarios la comprensión y la cumplimentación del formulario. Además, podría utilizarse con fines de accesibilidad para proporcionar una breve descripción del elemento al que está asociado. Este campo de texto suele mostrarse cerca de los componentes del formulario, como antes o después de él.

**Ejemplo**

![](/help/adaptive-forms/assets/text.png)

## Uso {#reasons-to-use-text-label}

Hay varias razones para utilizar texto en un formulario:

* **Proporcionar instrucciones**: se puede utilizar el texto para proporcionar instrucciones sobre cómo rellenar el formulario o qué información se necesita.

* **Proporcionar contexto**: el texto se puede utilizar para proporcionar contexto al formulario, como explicar la finalidad del formulario o la organización que recopila la información.

* **Dividir el formulario en secciones lógicas**: el texto se puede utilizar para dividir un formulario en secciones lógicas, facilitando a los usuarios su comprensión y cumplimentación.

* **Personalización de marca e identidad**: el texto se puede utilizar para la personalización de la marca y la identidad, como incluir el nombre de la organización en el formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de texto de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de texto para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones de texto con facilidad para que la experiencia del usuario sea óptima.

![Pestaña Básicos](/help/adaptive-forms/assets/text_properties.png)

* **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Referencia de enlace**: una referencia de enlace es una referencia a un elemento de datos que se almacena en un origen de datos externo y se utiliza en un formulario. La referencia de enlace permite enlazar datos de forma dinámica a campos de formulario, de modo que el formulario pueda mostrar los datos más actualizados de la fuente de datos. Por ejemplo, se puede utilizar una referencia de enlace para mostrar el nombre y la dirección de un cliente en un formulario, según el ID introducido en el formulario por el cliente. La referencia de enlace también se puede utilizar para actualizar la fuente de datos con los datos del formulario. De este modo, AEM Forms permite crear formularios que interactúen con fuentes de datos externas, lo que proporciona al usuario una experiencia óptima para recopilar y administrar datos.
* **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.
* **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.


## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Texto.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de texto de formularios adaptables es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/reset_designdialog.png)

* **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de texto de formularios adaptables.

* **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase de CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.
