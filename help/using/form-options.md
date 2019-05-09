---
title: Componente Opciones de formulario
seo-title: Componente Opciones de formulario
description: El componente de opciones Formulario principal permite la selección de opciones predefinidas en varios formatos.
seo-description: El componente de opciones Formulario principal permite la selección de opciones predefinidas en varios formatos.
uuid: 7 e 8714 df -75 d 1-4 bb 0-b 1 ee-b 7 c 7450 d 806 a
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 42289 c 2 b -1671-463 a-ac 1 d -457 aa 9 aefa 2 a
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente Opciones de formulario{#form-options-component}

El componente Opciones de formulario de componente principal permite la selección de opciones predefinidas en varios formatos.

## Uso {#usage}

El componente Opciones de formulario de componente principal permite enviar distintos tipos de opciones presentadas de muchas formas diferentes y está previsto que se utilicen junto con [el componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el cuadro de diálogo [de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Opciones de formulario es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-options-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/screen_shot_2018-01-12at113648.png)

### HTML {#html}

```
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-66464844" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-858231075" name="hidden">

</div>
<div class="hidden aem-GridColumn aem-GridColumn--default--12">
<input type="hidden" id="form-hidden-862566768" name="hidden">

</div>
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">

    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container/container">
    
    <div class="options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="cmp-form-options">
        
            <legend class="cmp-form-options__legend">What is your favorite type of toast?</legend>
            <label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="dryToast">
                Plain dry toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="frenchToast">
                French Toast
            </label>
<label class="cmp-form-options__field-label">
                <input class="cmp-form-options__field cmp-form-options__field--radio" type="radio" name="favToast" value="texasToast">
                Texas Toast
            </label>

    </fieldset>

</div>

</div></form>
```

### JSON {#json}

```
"container":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           "columnCount":12,
                           "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
                           ":items":{  
                              "options_816658469":{  
                                 "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                                 "id":"form-options-269951232",
                                 "title":"What is your favorite type of toast?",
                                 "name":"favToast",
                                 "type":"RADIO",
                                 "items":[  
                                    {  
                                       "value":"dryToast",
                                       "text":"Plain dry toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"frenchToast",
                                       "text":"French Toast",
                                       "selected":false,
                                       "disabled":false
                                    },
                                    {  
                                       "value":"texasToast",
                                       "text":"Texas Toast",
                                       "selected":false,
                                       "disabled":false
                                    }
                                 ],
                                 ":type":"core/wcm/sandbox/components/form/options/v2/options"
                              }
                           },
                           ":itemsOrder":[  
                              "options_816658469"
                           ],
                           ":type":"core/wcm/sandbox/components/form/container/v2/container"
                        }
```

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![](assets/screen_shot_2018-01-12at113153.png)

* **Tipos** : cómo se presentarán las opciones
   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**
* **Títuloel título**
que se mostrará como etiqueta para las opciones
* **Nombre**
del campo enviado con los datos del formulario
* **Origen**
donde se definen las opciones
   * **Local**
definido dentro del componente
      * Toque o haga clic en el botón **Agregar** para agregar un valor, **Eliminar** para eliminar un valor
      * **Valor**
guardado cuando se selecciona esa opción cuando se envía el formulario
      * **Texto**
La etiqueta de la opción mostrada en el formulario
      * **Activo**
La opción se marca como seleccionada cuando se carga el formulario
      * **Deshabilitada**
La opción No se puede seleccionar pero aún se muestra
      * **Lista**
de una lista estática definida en AEM para las opciones
         * **Lista**
de la ruta de la lista estática de AEM
            * Utilice el botón Examinar para localizar el recurso de lista
      * **Fuente
de datos** La fuente de datos se utiliza para las opciones
         * **Tipo**de recurso de fuente
de datos del origen de datos
* **Mensaje**
de ayuda Una sugerencia para el usuario de lo que se puede introducir en el campo

## Cuadro de diálogo de diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Opciones de formulario admite el sistema [de estilos AEM](authoring.md#component-styling).