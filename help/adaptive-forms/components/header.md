---
title: 'Componente principal de formularios adaptables: encabezado'
description: Uso o personalización del componente principal de encabezado de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '672'
ht-degree: 100%

---


# Encabezado {#header-adaptive-forms-core-component}

El componente Encabezado de un Formulario adaptable es una sección de la parte superior del formulario que generalmente incluye el título, el logotipo o el nombre del formulario. El encabezado también puede incluir otras informaciones, como una breve descripción de la finalidad del formulario, el nombre de la organización que lo ha creado o la información de contacto para obtener ayuda. El encabezado se utiliza para proporcionar a los usuarios una descripción general del formulario y contexto para la información que están a punto de ingresar. Se utiliza para ayudar a los usuarios a conocer la finalidad del formulario y cómo rellenarlo correctamente.

{{traditional-aem}}

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/header.png)

## Uso {#reasons-to-use-header}

- **Personalización de marca**: se puede utilizar un encabezado para mostrar el logotipo o el nombre de la organización que ha creado el formulario, lo que ayuda a establecer el reconocimiento y la credibilidad de la marca.

- **Contexto**: un encabezado puede proporcionar una breve descripción de la finalidad del formulario, lo que ayuda a los usuarios a comprender el contexto en el que se utiliza el formulario.

- **Navegación**: un encabezado puede incluir vínculos o botones que permiten a los usuarios navegar a otras partes del sitio web o aplicación.

- **Información**: un encabezado puede incluir información de contacto o vínculos a recursos de ayuda, lo que facilita la obtención de asistencia, en caso de que la necesiten.

- **Experiencia del usuario**: se puede utilizar un encabezado para facilitar el uso del formulario, proporcionando una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de encabezado de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales, versión 2.0.4 para Cloud Service y los componentes principales, versión 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| v1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_es). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de encabezado de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del encabezado para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de encabezado con facilidad para que la experiencia del usuario sea óptima.

### Pestaña Imagen {#image-tab}

Esta parte del encabezado contiene el título y la imagen del encabezado.

![Pestaña Imágenes](/help/adaptive-forms/assets/header_image.png)

- **Recurso de imagen**: esta opción permite soltar un recurso como una imagen arrastrando y soltando con el ratón. También puede cargar un archivo desde un sistema de archivos local utilizando el botón **Examinar**. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen:
   - **Editar**: pulse o haga clic en **Editar** para administrar las representaciones del recurso en el Editor de recursos.
   - **Borrar**: pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   - **Elegir**: pulse o haga clic en **Elegir**  para seleccionar otra imagen de la carpeta Recursos.

- **Título**: esta opción se utiliza para añadir el título al encabezado. El texto predefinido se incluye en el cuadro de diálogo y el usuario lo puede modificar.
- **Vincular a**: puede vincular el encabezado a la carpeta mediante el icono de **Examinar**.
- **Descripción**: una descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre la finalidad de una imagen específica.
- **Tamaño (px)**: ayuda a ajustar la longitud y anchura de la imagen aumentando o disminuyendo los píxeles.

![accessibilitytab](/help/adaptive-forms/assets/header_accessibility.png)

- **Texto alternativo**: esta opción se utiliza para introducir el texto que proporciona una alternativa de texto breve y descriptivo de la imagen, que describe la imagen para las personas con discapacidad visual.

- **La imagen es decorativa**: compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.

### Pestaña Texto {#text-tab}

Esta sección permite introducir el texto que se incluirá en el encabezado.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
