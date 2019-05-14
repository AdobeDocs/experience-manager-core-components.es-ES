---
title: Componente Opciones de formulario (v 1)
seo-title: Componente Opciones de formulario (v 1)
description: nulo
seo-description: El componente de opciones Formulario principal permite la selección de opciones predefinidas en varios formatos.
uuid: a 22 ed 77 c-c 9 f 3-46 f 4-8 afe-e 478383 c 1251
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: e 1975 bfe -2 bda -409 a -998 e -1 ff 4 f 9 f 23 b 94
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


# Componente Opciones de formulario (v 1){#form-options-component-v}

El componente de opciones Formulario principal permite la selección de opciones predefinidas en varios formatos.

## Uso {#usage}

El componente Opciones de formulario de componente principal permite enviar distintos tipos de opciones presentadas de muchas formas diferentes y se pretende utilizar junto con [el componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el cuadro de diálogo [de configuración](form-options-v1.md#main-pars_title).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Opciones de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de la versión 1 del componente Opciones de formulario.

| Versión del componente | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatible | Compatible |
| v1 | Compatible | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Opciones de formulario.
>
>Para obtener más información sobre la versión actual del componente Opciones de formulario, consulte [el documento Componente](form-options.md) Opciones de formulario.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![](assets/chlimage_1-90.png)

* **Tipos**
de opciones para presentar

   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**

* **Título** : El título que se mostrará como etiqueta para las opciones
* **Nombre** : nombre del campo enviado con los datos del formulario
* **Fuente** : donde se definen las opciones

   * **Local** - Definido dentro del componente
      * Toque o haga clic en el botón **Agregar** para agregar un valor, **Eliminar** para eliminar un valor
      * **Valor** : valor guardado cuando se selecciona esa opción cuando se envía el formulario
      * **Texto** : la etiqueta de la opción mostrada en el formulario
      * **Activo** : la opción se marca como seleccionada cuando se carga el formulario
      * **Deshabilitado** : la opción no se puede seleccionar pero aún se muestra
      * **Lista** : Se utiliza una lista estática definida en AEM para la opción
         * **Lista** : Ruta de la lista estática de AEM
            * Utilice el botón Examinar para localizar el recurso de lista
      * **Fuente** de datos: Se utiliza un origen de datos para las opciones
         * **Fuente** de datos: tipo de recurso del origen de datos
* **Mensaje** de ayuda: Sugerencia para el usuario de lo que se puede introducir en el campo

## Cuadro de diálogo de diseño {#design-dialog}

No hay un cuadro de diálogo de diseño para el componente Opciones de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
