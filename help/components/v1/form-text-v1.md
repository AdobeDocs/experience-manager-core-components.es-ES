---
title: Componente de texto del formulario (v1)
description: El componente Texto del formulario del componente principal permite introducir el texto del formulario para enviarlo.
index: n
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---


# Componente de texto de formulario (v1) {#form-text-component-v}

El componente Texto del formulario del componente principal permite introducir el texto del formulario para enviarlo.

## Uso {#usage}

El componente Texto de formulario permite enviar diferentes tipos de texto y está diseñado para utilizarse junto con el [componente contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda en el cuadro de diálogo [configurar](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Texto de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Texto de formulario.

| Versión de AEM | Componente de texto de formulario v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de texto del formulario.
>
>Para obtener más información sobre la versión actual del componente de texto del formulario, consulte el documento [Componente de texto del formulario](/help/components/forms/form-text.md).

## Salida de componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales v1](/help/versions.md) para obtener más información.

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se va a introducir, así como los valores predeterminados y las etiquetas.

### Principal {#main}

![](/help/assets/chlimage_1-23.png)

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

### Acerca de {#about}

![](/help/assets/chlimage_1-24.png)

* **Mensaje de ayuda** : una sugerencia para el usuario sobre lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** : para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando está vacía y no está enfocada

### Restricciones {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Mensaje de restricción**

   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Text** y **Text Area**

* **Requerido** : si está seleccionado, el usuario debe rellenar un valor antes de enviar el formulario
* **Convertir en solo lectura** : si está seleccionado, el usuario no puede modificar el valor del campo

## Diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Texto de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto del formulario [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
