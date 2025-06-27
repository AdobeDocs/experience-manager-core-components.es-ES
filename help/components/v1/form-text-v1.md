---
title: Componente Texto de formulario (versión 1)
description: El componente principal Texto de formulario permite introducir el texto del formulario para enviarlo.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Texto de formulario (versión 1) {#form-text-component-v}

El componente principal Texto de formulario permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar diferentes tipos de texto y está diseñado para utilizarse junto con el [componente Contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el [cuadro de diálogo de configuación](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Texto de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de la versión 1 del componente Texto de formulario.

| Versión de AEM | Componente Texto de formulario (versión 1) |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Texto de formulario.
>
>Para obtener más información sobre la versión actual del componente Texto de formulario, consulte el documento [Componente Texto de formulario](/help/components/forms/form-text.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
  </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se va a introducir, así como los valores predeterminados y las etiquetas.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

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

### Acerca de {#about}

![](/help/assets/chlimage_1-24.png)

* **Mensaje de ayuda**: una sugerencia al usuario sobre lo que se puede introducir en el campo
* **Mostrar el mensaje de ayuda como marcador de posición**: si desea mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacía y no seleccionada

### Restricciones {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Mensaje de restricción**

   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y **Área de texto**

* **Obligatorio**: si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
* **Hacer de solo lectura**: si está seleccionado, el usuario no puede modificar el valor del campo

## Cuadro de diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Texto de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente [Texto de formulario se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
