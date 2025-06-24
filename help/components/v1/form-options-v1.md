---
title: Componente Opciones de formulario (versión 1)
description: El componente principal Opciones de formulario permite seleccionar entre las opciones predefinidas en distintos formatos.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 100%

---


# Componente Opciones de formulario (versión 1) {#form-options-component-v}

El componente principal Opciones de formulario permite seleccionar entre las opciones predefinidas en distintos formatos.

## Uso {#usage}

El componente principal Opciones de formulario permite enviar diferentes tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el [componente Contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Opciones de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de la versión 1 del componente Opciones de formulario.

| Versión del componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| Versión 2 | Compatible | Compatible |
| Versión 1 | Compatible | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Opciones de formulario.
>
>Para obtener más información sobre la versión actual del componente Opciones de formulario, consulte el documento [Componente Opciones de formulario](/help/components/forms/form-options.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![](/help/assets/chlimage_1-90.png)

* **Tipos**
Presentación de las opciones

   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**

* **Título**: el título que se mostrará como etiqueta para las opciones
* **Nombre**: el nombre del campo, que se envía con los datos del formulario
* **Origen**: donde se definen las opciones

   * **Local**: se define dentro del componente
      * Pulse o haga clic en el botón **Añadir** para añadir un valor y en **Eliminar** para eliminarlo
      * **Valor**: el valor guardado cuando se selecciona esa opción cuando se envía el formulario
      * **Texto**: etiqueta de la opción que se muestra en el formulario.
      * **Activo**: la opción se marca como seleccionada cuando se carga el formulario
      * **Desactivado**: la opción no se puede seleccionar pero se sigue mostrando
      * **Lista**: se utiliza una lista estática definida en otra parte de AEM para la opción
         * **Lista**: la ruta de la lista estática de AEM
            * Utilice el botón Examinar para localizar el recurso de la lista
      * **Fuente de datos**: se utiliza una fuente de datos para las opciones
         * **Fuente de datos**: tipo de recurso de la fuente de datos
* **Mensaje de ayuda**: una sugerencia al usuario sobre lo que se puede introducir en el campo

## Cuadro de diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Opciones de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
