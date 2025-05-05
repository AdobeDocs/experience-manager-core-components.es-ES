---
title: 'Componente principal de formularios adaptables: título'
description: Uso o personalización del componente principal de título de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '866'
ht-degree: 100%

---

# Componente Título de formulario{#title-input-adaptive-forms-core-component}

En un formulario adaptable, un “título” hace referencia al texto que aparece en la parte superior del formulario, normalmente debajo del encabezado. El título se especifica mediante el componente de título. Este componente puede añadirse al diseño del formulario y su texto puede editarse para que coincida con el propósito o el tema del formulario. El título sirve como etiqueta o descripción breve del formulario para el usuario y ayuda a distinguirlo de otros.

**Ejemplo**

![ejemplo de título](/help/adaptive-forms/assets/title.png)

## Uso {#reasons-to-use-title-in-an-adaptive-form}

Hay varias razones por las que es recomendable utilizar un título en un formulario:

- **Claridad**: un título identifica claramente el propósito del formulario, lo que ayuda a los usuarios a comprender qué información necesitan proporcionar.

- **Organización**: un título puede ayudar a organizar los formularios por tema o propósito, lo que facilita a los usuarios encontrar el que necesitan.

- **Accesibilidad**: un título es un elemento clave para los usuarios con necesidades de accesibilidad, ya que los lectores de pantalla lo leen en voz alta, lo que ayuda a comprender el contexto del formulario.

- **Personalización de marca**: un título también se puede usar para mostrar el nombre de una empresa u organización, lo que ayuda a crear sensación de confianza y familiaridad con el usuario.

- **Navegación**: un título también puede resultar útil para desplazarse por el formulario, especialmente si es largo o complejo.

- **Optimización del motor de búsqueda (SEO)**: tener un título en el formulario también ayuda en SEO, ya que los motores de búsqueda se sirven del título para determinar la importancia de una página web en una consulta de búsqueda.

En general, el título es un aspecto importante de la experiencia del usuario y debe utilizarse para proporcionar una etiqueta clara y concisa que ayude a los usuarios a comprender el contexto y la finalidad del formulario.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de mosaico de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales, versión 2.0.4 para Cloud Service y los componentes principales, versión 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_es). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de título de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de títulos para los visitantes con el cuadro de diálogo de configuración. También puede definir opciones de títulos con facilidad para una experiencia del usuario perfecta.

![Pestaña Básicos](/help/adaptive-forms/assets/title_properties.png)

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Tipo/tamaño**: define el nivel de encabezado del título.
- **ID**: esta opción permite controlar el identificador único del componente del HTML y de la capa de datos.
   - Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   - Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   - Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

La pestaña Diseño se utiliza para definir y administrar estilos CSS para el componente de título de formulario.

### Título

La pestaña Título permite a los autores de plantillas definir elementos de encabezado de HTML predeterminados y permitidos para los autores de formularios:

![Pestaña Título del cuadro de diálogo de diseño](/help/adaptive-forms/assets/title_heading.png)

- **Elementos de encabezado permitidos**: una lista con varias opciones que permite al autor de la plantilla elegir los elementos de encabezado que el autor puede utilizar para el título.

- **Elemento de encabezado predeterminado**: una lista desplegable que establece el elemento de encabezado predeterminado para el componente de título.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de selector de fecha de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Pestaña Título del cuadro de diálogo de diseño](/help/adaptive-forms/assets/title_styles.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de título de formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Formatos {#format-tab}

La pestaña Formatos permite especificar formatos de fecha predeterminados y personalizados.

![Pestaña Formato](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)

-->

## Artículos relacionados {#related-articles}


{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}