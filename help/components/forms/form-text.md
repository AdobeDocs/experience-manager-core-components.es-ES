---
title: Componente de texto de formulario
description: El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 7%

---


# Componente de texto de formulario{#form-text-component}

El componente Texto del formulario de componente principal permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto del formulario permite enviar distintos tipos de texto y está diseñado para utilizarse junto con el componente [contenedor del](form-container.md)formulario. El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el cuadro de diálogo [](#configure-dialog)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de texto del formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_text)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Texto del formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

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
* **Líneas** de texto: número de líneas que se van a mostrar en el área de texto (solo se muestran cuando **Restricción** se define como Área **de** texto)
* **Etiqueta** : la etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para que no se muestre** : Necesario si la etiqueta solo es necesaria para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre** del elemento: el nombre del campo que se envía con los datos del formulario
* **Valor** : valor predeterminado que se rellena previamente en el campo
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Ficha Acerca de {#about-tab}

![Ficha Acerca de](/help/assets/form-text-edit-about.png)

* **Mensaje** de ayuda: una sugerencia para el usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** : para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacío y no está centrado

### Ficha Restricciones {#constraints-tab}

![Ficha Restricciones](/help/assets/form-text-edit-constraints.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y Área **de texto**
* **Obligatorio** : si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
   * **Mensaje** requerido: mensaje que se muestra como información sobre herramientas si el campo se deja vacío
* **Convertir en solo** lectura: si se selecciona, el usuario no puede modificar el valor del campo

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente de texto de formulario admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
