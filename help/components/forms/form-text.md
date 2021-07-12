---
title: Componente de texto de formulario
description: El componente Texto del formulario del componente principal permite introducir el texto del formulario para enviarlo.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 7%

---

# Componente de texto de formulario{#form-text-component}

El componente Texto del formulario del componente principal permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar diferentes tipos de texto y está diseñado para utilizarse junto con el [componente contenedor de formulario](form-container.md). El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el cuadro de diálogo [configurar](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Texto del formulario, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_text).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto del formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se va a introducir, así como los valores predeterminados y las etiquetas.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades](/help/assets/form-text-edit-properties.png)

* **Restricción** : Tipo de texto que se va a introducir y se validará con
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas de texto** : número de líneas que se mostrarán en el área de texto (solo se muestran cuando se  **** establezca Restricciones en Área de  **texto**)
* **Etiqueta** : la etiqueta que se mostrará para el campo.
* **Ocultar la etiqueta para que no se muestre** : Necesario si la etiqueta es necesaria solo para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre del elemento** : el nombre del campo que se envía con los datos del formulario.
* **Valor** : valor predeterminado que se rellena previamente en el campo
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### Acerca de la pestaña {#about-tab}

![Ficha Acerca de](/help/assets/form-text-edit-about.png)

* **Mensaje de ayuda** : una sugerencia para el usuario sobre lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** : para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacía y no está enfocada

### Ficha Restricciones {#constraints-tab}

![Pestaña Restricciones](/help/assets/form-text-edit-constraints.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Text** y **Text Area**
* **Requerido** : si está seleccionado, el usuario debe rellenar un valor antes de enviar el formulario
   * **Mensaje obligatorio** : Mensaje mostrado como información sobre herramientas si el campo se deja vacío
* **Convertir en solo lectura** : si está seleccionado, el usuario no puede modificar el valor del campo

## Cuadro de diálogo Diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Texto de formulario es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
