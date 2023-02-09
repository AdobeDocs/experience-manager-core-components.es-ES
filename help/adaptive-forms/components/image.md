---
title: 'Componente principal adaptable de Forms: imagen'
description: Uso o personalización del componente principal de imagen de Forms adaptable.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Imagen {#image-adaptive-forms-core-component}

Un componente Imagen en un formulario adaptable es una forma de incluir imágenes en un formulario. Estas imágenes se pueden utilizar para mejorar el diseño general del formulario, proporcionar información adicional o servir como ayuda visual para ayudar a los usuarios a comprender el propósito del formulario. El componente de imagen se puede utilizar para agregar un logotipo, una foto o un gráfico en el formulario.

Para la accesibilidad, es importante especificar **Texto alternativo** a la imagen para proporcionar una alternativa textual corta y descriptiva para la imagen, que describe la imagen para los usuarios que no pueden verla.


**Ejemplo**

![](/help/adaptive-forms/assets/image.png)


## Uso {#reasons-to-use-image-in-a-form}

Existen varias razones por las que resulta beneficioso incluir un componente Imagen en un formulario adaptable, entre ellas:

* **Marcas**: Se puede utilizar una imagen para mostrar el logotipo o el nombre de la organización que creó el formulario, lo que ayuda a establecer el reconocimiento y la credibilidad de la marca.

* **Ayudas visuales**: Una imagen puede ayudar a proporcionar un nivel adicional de información a los usuarios, al servir como ayuda visual para ayudar a los usuarios a comprender el propósito del formulario.

* **Decoración**: Se puede utilizar una imagen para mejorar el diseño general del formulario y hacerlo visualmente más atractivo.

* **Experiencia del usuario**: Se puede utilizar una imagen para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de imagen de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de imagen adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).


## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de imagen para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de imagen con facilidad para una experiencia de usuario perfecta.

![Pestaña Propiedades](/help/adaptive-forms/assets/image_properties.png)

* **Nombre** - Puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

* **Título** : con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

* **Documento de referencia de enlace de registro** - Esta opción le permite asociar un campo Formulario adaptable al campo Documento de registro. Cuando el usuario introduce cualquier valor en un campo vinculado de un formulario adaptable, ese valor también aparece en el campo vinculado del documento de registro correspondiente. Por ejemplo, se puede utilizar una referencia de enlace de documento de registro para mostrar el nombre y la dirección de un cliente en un documento de registro, en función del ID introducido en el formulario por el cliente. De este modo, AEM Forms le permite generar un documento de registro y ofrece una experiencia de usuario perfecta para recopilar y administrar datos.

* **Descripción** - Una descripción es una breve explicación de texto que proporciona información adicional o aclaración sobre el propósito de una imagen específica.

* **Coloque un recurso aquí o busque un archivo para cargar** : esta opción permite soltar un recurso como una imagen arrastrando y soltando el ratón. También puede cargar un archivo desde un sistema de archivos local utilizando la variable **Examinar** botón. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen:
   * **Editar** - Toque o haga clic **Editar** para administrar las representaciones del recurso en el Editor de recursos.
   * **Borrar** - Toque o haga clic **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * **Seleccionar** - Toque o haga clic **Seleccionar**  para seleccionar otra imagen de la carpeta Recursos.

* **Texto alternativo** - Esta opción se utiliza para introducir el texto que proporciona una alternativa textual corta y descriptiva para la imagen, que describe la imagen para usuarios con problemas de visión.

* **Ocultar componente** : seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

* **Solo lectura** - Seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS para el componente Imagen.

### Pestaña Estilos {#styles-tab}

El cuadro de diálogo Diseño se utiliza para definir y administrar estilos CSS de un componente. El componente principal de imagen de Forms adaptable es compatible con el AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Clases CSS predeterminadas**: Puede proporcionar una clase CSS predeterminada para el componente principal de imagen adaptable de Forms.

**Estilos permitidos**: Puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado &quot;texto en negrita&quot; y proporcionar la clase CSS &quot;font-weight: negrita&quot;. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de Forms adaptable. Para aplicar un estilo, en el editor de Forms adaptable, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en el **Estilos** lista desplegable. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la ficha Estilos y guarde los cambios.
