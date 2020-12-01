---
title: Componente de texto de formulario
description: El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 7%

---


# Componente de texto de formulario{#form-text-component}

El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar distintos tipos de texto y está diseñado para utilizarse junto con el [componente de contenedor de formulario](form-container.md). El tipo de validación de texto, etiquetas y mensajes de ayuda puede ser definido por el editor de contenido en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Texto del formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_text).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se debe introducir, así como los valores y etiquetas predeterminados.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades](/help/assets/form-text-edit-properties.png)

* **Restricción** : tipo de texto que se va a introducir y se validará con
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas**  de texto: número de líneas que se mostrarán en el área de texto (solo se muestran cuando  **** Restricciones se definen como Área **de** texto)
* **Etiqueta** : la etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para que no se muestre** - Necesario si la etiqueta solo es necesaria para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre**  del elemento: el nombre del campo que se envía con los datos del formulario
* **Valor** : valor predeterminado que se rellena previamente en el campo
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Acerca de la ficha {#about-tab}

![Ficha Acerca de](/help/assets/form-text-edit-about.png)

* **Mensaje**  de ayuda: una sugerencia para el usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador**  de posición: para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacío y no está enfocado

### Ficha Restricciones {#constraints-tab}

![Ficha Restricciones](/help/assets/form-text-edit-constraints.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y **Área de texto**
* **Obligatorio** : si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
   * **Mensaje**  requerido: mensaje que se muestra como información sobre herramientas si el campo se deja vacío
* **Convertir en solo**  lectura: si se selecciona, el usuario no puede modificar el valor del campo

## Diálogo de diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Texto de formulario admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).
