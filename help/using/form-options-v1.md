---
title: Componente Opciones de formulario (v1)
seo-title: Componente Opciones de formulario (v1)
description: nulo
seo-description: El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.
uuid: a22ed77c-c9f3-46f4-8afe-e478383c1251
content-type: referencia
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: e1975bfe-2bda-409a-998e-1ff4f9f23b94
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
noindex: verdadero
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Form Options Component (v1){#form-options-component-v}

El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.

## Uso {#usage}

El componente Opciones de formulario de componentes principales permite enviar distintos tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el componente [contenedor de](form-container.md)formularios.

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el cuadro de diálogo [de](form-options-v1.md#main-pars_title)configuración.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Opciones de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Opciones de formulario.

| Versión del componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatible | Compatible |
| v1 | Compatible | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Opciones de formulario.
>
>Para obtener más información sobre la versión actual del componente Opciones de formulario, consulte el documento Componente [Opciones de](form-options.md) formulario.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-89.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![](assets/chlimage_1-90.png)

* **Tipos** Cómo se presentarán las opciones

   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**

* **Título** : el título que se mostrará como la etiqueta de las opciones
* **Nombre** : el nombre del campo enviado con los datos del formulario
* **Origen** : donde se definen las opciones

   * **Local** : definido dentro del componente
      * Toque o haga clic en el botón **Agregar** para agregar un valor, **Eliminar** para eliminarlo
      * **Valor** : valor guardado cuando se selecciona esa opción al enviar el formulario
      * **Texto** : la etiqueta de la opción que se muestra en el formulario
      * **Activo** : la opción se marca como seleccionada cuando se carga el formulario
      * **Deshabilitada** : la opción no se puede seleccionar pero se muestra
      * **Lista** : se utiliza una lista estática definida en otra parte de AEM para la opción
         * **Lista** : la ruta de la lista estática en AEM
            * Utilice el botón Examinar para localizar el recurso de lista
      * **Fuente** de datos: se utiliza una fuente de datos para las opciones
         * **Fuente** de datos: tipo de recurso de la fuente de datos
* **Mensaje** de ayuda: una sugerencia para el usuario sobre lo que se puede introducir en el campo

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Opciones de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.
