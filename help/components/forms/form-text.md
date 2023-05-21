---
title: Componente Texto de formulario
description: El componente principal Texto de formulario permite introducir el texto del formulario para enviarlo.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 100%

---

# Componente Texto de formulario {#form-text-component}

El componente principal Texto de formulario permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar diferentes tipos de texto y está diseñado para utilizarse junto con el [componente contenedor de formulario](form-container.md). El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el [cuadro de diálogo de configuación](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto de formulario es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| Versión 2 | Compatible  con la <br>[versión 2.17.4](/help/versions.md) y anterior | Compatible | Compatible |
| [Versión 1](/help/components/v1/form-text-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Texto de formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_text_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [Texto de formulario se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se va a introducir, así como los valores predeterminados y las etiquetas.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades](/help/assets/form-text-edit-properties.png)

* **Restricción**: tipo de texto que se va a introducir y que servirá para validar
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas de texto**: número de líneas que se mostrarán en el área de texto (solo se muestran cuando **Restricción** se establezca en **Área de texto**)
* **Etiqueta**: la etiqueta que se mostrará para el campo.
* **Ocultar la etiqueta para que no se muestre**: necesario si la etiqueta es necesaria solo para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre elemento**: el nombre del campo, que se envía con los datos del formulario
* **Valor**: valor predeterminado que se rellena previamente en el campo
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Acerca de {#about-tab}

![Pestaña Acerca de](/help/assets/form-text-edit-about.png)

* **Mensaje de ayuda**: una sugerencia al usuario sobre lo que se puede introducir en el campo
* **Mostrar el mensaje de ayuda como marcador de posición**: si desea mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacía y no seleccionada

### Pestaña Restricciones {#constraints-tab}

![Pestaña Restricciones](/help/assets/form-text-edit-constraints.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y **Área de texto**
* **Obligatorio**: si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
   * **Mensaje obligatorio**: mensaje mostrado como información sobre herramientas si el campo se deja vacío
* **Hacer de solo lectura**: si está seleccionado, el usuario no puede modificar el valor del campo

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Texto de formulario es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
