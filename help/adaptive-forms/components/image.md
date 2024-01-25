---
title: 'Componente principal de Formularios adaptables: imagen'
description: Uso o personalización del componente principal de imagen de Formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 8388de05c86641d4887b48a9fd10901cb5a19998
workflow-type: tm+mt
source-wordcount: '1198'
ht-degree: 100%

---

# Imagen {#image-adaptive-forms-core-component}

Un componente Imagen de un Formulario adaptable es una forma de incluir imágenes en un formulario. Estas imágenes se pueden utilizar para mejorar el diseño general del formulario, proporcionar información adicional o servir como ayuda visual para que los usuarios comprendan la finalidad del formulario. El componente de imagen se puede utilizar para añadir un logotipo, una foto o un gráfico en el formulario.

Para la accesibilidad, es importante especificar un **Texto alternativo** para la imagen para proporcionar una alternativa de texto corto y descriptivo de la imagen, que describa la imagen para las personas que no pueden verla.


**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/image.png)


## Uso {#reasons-to-use-image-in-a-form}

Existen varias razones por las que resulta beneficioso incluir un componente Imagen en un Formulario adaptable, entre ellas:

- **Personalización de marca**: se puede utilizar una imagen para mostrar el logotipo o el nombre de la organización que ha creado el formulario, lo que ayuda a establecer el reconocimiento y la credibilidad de la marca.

- **Ayudas visuales**: una imagen puede ayudar a proporcionar un nivel adicional de información a los usuarios, al servir como ayuda visual para que comprendan la finalidad del formulario.

- **Decoración**: se puede utilizar una imagen para mejorar el diseño general del formulario y hacerlo visualmente más atractivo.

- **Experiencia del usuario**: se puede utilizar una imagen para que el formulario sea más fácil de usar, ya que proporciona una forma clara e intuitiva de que los usuarios accedan a los campos del formulario y los rellenen.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de imagen de Formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).


## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de la imagen para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de imagen con facilidad para que la experiencia del usuario sea óptima.

![Pestaña Propiedades](/help/adaptive-forms/assets/image_properties.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.

- **Referencia de vínculo de documento de registro**: esta opción le permite asociar un campo del formulario adaptable al campo Documento de registro. Cuando el usuario introduce cualquier valor en un campo vinculado de un formulario adaptable, ese valor también aparece en el campo vinculado del documento de registro correspondiente. Por ejemplo, se puede utilizar una referencia de vínculo de documento de registro para mostrar el nombre y la dirección de un cliente en un documento de registro, en función del ID introducido en el formulario por el cliente. De este modo, AEM Forms permite generar un documento de registro y ofrece una experiencia del usuario perfecta para recopilar y administrar datos.

- **Descripción**: una descripción es una explicación de texto breve que proporciona información adicional o aclaración sobre la finalidad de una imagen específica.

- **Coloque un recurso aquí o busque un archivo para cargar**: esta opción permite soltar un recurso como una imagen arrastrando y soltando con el ratón. También puede cargar un archivo desde un sistema de archivos local utilizando el botón **Examinar**. Después de añadir una imagen, aparecen tres botones en la parte inferior de la imagen:
   - **Editar**: pulse o haga clic en **Editar** para administrar las representaciones del recurso en el Editor de recursos.
   - **Borrar**: pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   - **Elegir**: pulse o haga clic en **Elegir** para seleccionar otra imagen de la carpeta Recursos.

- **Texto alternativo**: esta opción se utiliza para introducir el texto que proporciona una alternativa de texto corto y descriptivo de la imagen, que describa la imagen para las personas con discapacidad visual.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Imagen.

### Pestaña Estilos {#styles-tab}

La pestaña se utiliza para definir y administrar estilos CSS de un componente. El componente principal de imagen de Formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de imagen de Formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Vea también {#see-also}

{{see-also}}