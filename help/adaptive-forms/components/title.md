---
title: 'Componente principal de Forms adaptable: título '
description: Uso o personalización del componente principal del título adaptable de Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 15%

---


# Título {#title-input-adaptive-forms-core-component}

En un formulario adaptable, un &quot;título&quot; hace referencia al texto que aparece en la parte superior del formulario, normalmente debajo del encabezado. El título se especifica mediante el componente Título . Este componente se puede agregar a la presentación del formulario y su texto se puede editar para que coincida con el propósito o el tema del formulario. El título sirve como etiqueta o descripción breve del formulario para el usuario, y ayuda a distinguir el formulario de otros.

**Ejemplo**

![](/help/adaptive-forms/assets/title.png)

## Uso {#reasons-to-use-title-in-an-adaptive-form}

Hay varias razones por las que es recomendable utilizar un título en un formulario:

* **Claridad**: Un título identifica claramente el propósito del formulario, lo que ayuda a los usuarios a comprender qué información necesitan proporcionar.

* **Organización**: Un título puede ayudar a organizar los formularios por tema o propósito, lo que facilita a los usuarios encontrar el formulario que necesitan.

* **Accesibilidad**: Un título es un elemento clave para los usuarios con necesidades de accesibilidad, ya que los lectores de pantalla lo leen en voz alta, lo que ayuda a los usuarios a comprender el contexto del formulario.

* **Marcas**: Un título también se puede utilizar para mostrar el nombre de una empresa u organización, lo que ayuda a crear una sensación de confianza y familiaridad con el usuario.

* **Navegación**: Un título también puede resultar útil para desplazarse por el formulario, especialmente si el formulario es largo o complejo.

* **Optimización del motor de búsqueda (SEO)**: Tener un título en el formulario también ayuda en SEO, ya que los motores de búsqueda utilizan el título para determinar la importancia de una página web para una consulta de búsqueda.

En general, el título de un formulario es un aspecto importante de la experiencia del usuario y debe utilizarse para proporcionar una etiqueta clara y concisa para el formulario que ayude a los usuarios a comprender el contexto y la finalidad del mismo.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del título de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del título adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de título para los visitantes con el cuadro de diálogo Configurar . También puede definir opciones de título con facilidad para una experiencia de usuario perfecta.

![Ficha Básico](/help/adaptive-forms/assets/title_properties.png)

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
* **Tipo / Tamaño**: define el nivel de encabezado del título.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la capa de datos.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Selector de fechas.

### Título

La ficha Título permite a los autores de plantillas definir elementos de encabezado de HTML predeterminados y permitidos para los autores de formularios:

![Ficha Título del cuadro de diálogo Diseño](/help/assets/accordion-design-properties.png)

* **Elementos de encabezado permitidos**: Una lista con varias opciones que permite al autor de la plantilla elegir los elementos de encabezados que el autor puede utilizar para el título.

* **Elemento Encabezado predeterminado**: Lista desplegable que establece el elemento Encabezado predeterminado para el componente Título.


### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal del selector de fechas de Forms adaptable es compatible con la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal del selector de fechas de Forms adaptable.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.

### Ficha Formatos {#format-tab}

La pestaña format permite especificar formatos de fecha predeterminados y personalizados.

