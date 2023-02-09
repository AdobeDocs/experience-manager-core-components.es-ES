---
title: 'Componente principal de Forms adaptable: encabezado'
description: Uso o personalización del componente principal del encabezado adaptable de Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 7%

---


# Encabezado {#header-adaptive-forms-core-component}

Un componente Encabezado de un formulario adaptable es una sección de la parte superior del formulario que generalmente incluye el título, el logotipo o el nombre del formulario. El encabezado también puede incluir otra información, como una breve descripción de la finalidad del formulario, el nombre de la organización que lo creó o información de contacto para obtener ayuda con el formulario. El encabezado se utiliza para proporcionar a los usuarios una descripción general del formulario y proporcionar contexto para la información que están a punto de rellenar. Se utiliza para ayudar a los usuarios a comprender el propósito del formulario y cómo rellenarlo correctamente.

**Ejemplo**

![](/help/adaptive-forms/assets/header.png)

## Uso {#reasons-to-use-header}

* **Marcas**: Se puede utilizar un encabezado para mostrar el logotipo o el nombre de la organización que creó el formulario, lo que ayuda a establecer el reconocimiento y la credibilidad de la marca.

* **Contexto**: Un encabezado puede proporcionar una breve descripción del propósito del formulario, lo que ayuda a los usuarios a comprender el contexto en el que se utiliza el formulario.

* **Navegación**: Un encabezado puede incluir vínculos o botones que permiten a los usuarios navegar a otras partes del sitio web o aplicación.

* **Información**: Un encabezado puede incluir información de contacto o vínculos a recursos de ayuda, lo que facilita a los usuarios la asistencia si la necesitan.

* **Experiencia del usuario**: Se puede utilizar un encabezado para facilitar el uso del formulario, ya que proporciona una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del encabezado adaptable de Forms se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |
Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del encabezado adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del encabezado para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de encabezado con facilidad para que la experiencia de usuario sea perfecta.

### Pestaña Imagen {#image-tab}

Esta parte del encabezado contiene el título y la imagen del encabezado.

![Ficha de imágenes](/help/adaptive-forms/assets/header_image.png)

* **Recurso de imagen** : esta opción permite soltar un recurso como una imagen arrastrando y soltando el ratón. También puede cargar un archivo desde un sistema de archivos local utilizando la variable **Examinar** botón. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen:
   * **Editar** - Toque o haga clic **Editar** para administrar las representaciones del recurso en el Editor de recursos.
   * **Borrar** - Toque o haga clic **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * **Seleccionar** - Toque o haga clic **Seleccionar**  para seleccionar otra imagen de la carpeta Recursos.

* **Título** - Esta opción se utiliza para añadir el encabezado al encabezado. El texto predefinido se incluye en el cuadro de diálogo y el usuario puede modificarlo.
* **Vincular a** - Puede vincular el encabezado a la carpeta mediante la función **Examinar** icono.
* **Descripción** - Una descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de una imagen específica.
* **Tamaño (px)** - Ayuda a ajustar la longitud y anchura de la imagen aumentando o disminuyendo los píxeles.

![accessibilitytab](/help/adaptive-forms/assets/header_accessibility.png)

* **Texto alternativo** - Esta opción se utiliza para introducir el texto que proporciona una alternativa textual corta y descriptiva para la imagen, que describe la imagen para usuarios con problemas de visión.

* **La imagen es decorativa**: compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.

### Ficha Texto {#text-tab}

Esta sección permite introducir el texto que se incluirá en el encabezado.



