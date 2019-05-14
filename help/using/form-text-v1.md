---
title: Componente de texto de formulario (v 1)
seo-title: Componente de texto de formulario (v 1)
description: nulo
seo-description: El componente de texto de formulario de componente principal permite la entrada del texto del formulario para su envío.
uuid: 30123 aba -57 a 8-4 ed 4-93 cb -6 a 3 d 2 edff 9 a 7
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: bd 4 e 9930-4 d 81-49 ae-a 3 d 1-9 a 8740418 dae
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente de texto de formulario (v 1){#form-text-component-v}

El componente de texto de formulario de componente principal permite la entrada del texto del formulario para su envío.

## Uso {#usage}

El componente Texto de formulario permite enviar distintos tipos de texto y está pensado que se utilice junto con [el componente Contenedor de formulario](form-container.md).

El editor de contenido del cuadro de diálogo [de configuración puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda](form-text-v1.md#main-pars_title).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe v 1 del componente de texto de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v 1 del componente de texto de formulario.

| Versión de AEM | Componente de texto de formulario v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe v 1 del componente de texto de formulario.
>
>Para obtener más información sobre la versión actual del componente de texto de formulario, consulte [el documento Componente](form-text.md) de texto de formulario.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-22.png)

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
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el tipo de texto que se va a introducir como así también los valores y etiquetas predeterminados.

### Principal {#main}

![](assets/chlimage_1-23.png)

* **Restricción** : El tipo de texto que se va a introducir y se validará con

   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**

* **Líneas** de texto: Número de líneas que se mostrarán en el área de texto (solo se muestra cuando **la restricción** está definida como **Área de texto**)

* **Etiqueta** : la etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para que se muestre:** es necesario si la etiqueta solo es necesaria para fines de accesibilidad y no proporciona información visual adicional sobre el campo.
* **Nombre** del elemento: nombre del campo enviado con los datos del formulario
* **Valor** : valor predeterminado que se rellena previamente en el campo

### Acerca de {#about}

![](assets/chlimage_1-24.png)

* **Mensaje** de ayuda: Sugerencia al usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** : para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando esté vacío y no está enfocado

### Restricciones {#constraints}

![](assets/chlimage_1-25.png)

* **Mensaje de restricción**

   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para **los tipos de restricción Texto** y **Área** de texto

* **Obligatorio** : si se selecciona el usuario, debe rellenar un valor antes de enviar el formulario
* **Hacer solo lectura** : Si se selecciona el usuario no puede modificar el valor del campo

## Cuadro de diálogo de diseño {#design-dialog}

No hay un cuadro de diálogo de diseño para el componente Texto de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
