---
title: Componente de texto de formulario
description: El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente de texto de formulario{#form-text-component}

El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar distintos tipos de texto y está diseñado para utilizarse junto con el componente [contenedor de](form-container.md)formulario. El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el cuadro de diálogo [](#configure-dialog)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de texto del formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_text)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Texto del formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se debe introducir, así como los valores y etiquetas predeterminados.

### Ficha Principal {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Restricción** El tipo de texto que se va a introducir y se validará con
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas** de texto Número de líneas que se mostrarán en el área de texto (solo se muestran cuando **Restricción** se establece en Área **de** texto)
* **Etiqueta** Etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para que no se muestre** Necesario si la etiqueta es necesaria solo para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre** del elemento El nombre del campo que se envía con los datos del formulario
* **Valor** predeterminado que se rellena previamente en el campo

### Ficha Acerca de {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Mensaje** de ayuda Una sugerencia para el usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** Para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando esté vacío y no esté centrado

### Ficha Restricciones {#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y Área **de texto**
* **Obligatorio** Si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
* **Convertir en solo** lectura Si se selecciona, el usuario no puede modificar el valor del campo

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Texto de formulario.