---
title: Componente Opciones de formulario
seo-title: Componente Opciones de formulario
description: El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.
seo-description: El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.
uuid: 7e8714df-75d1-4bb0-b1ee-b7c7450d806a
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: 42289c2b-1671-463a-ac1d-457aa9aefa2a
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente Opciones de formulario{#form-options-component}

El componente Opciones de formulario de componentes principales permite seleccionar opciones predefinidas en diversos formatos.

## Uso {#usage}

El componente Opciones de formulario de componentes principales permite enviar distintos tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el componente [Contenedor de](form-container.md)formularios.

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el cuadro de diálogo [de](#configure-dialog)configuración.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Opciones de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-options-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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

La documentación técnica más reciente sobre el componente Opciones de formulario [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![](assets/screen_shot_2018-01-12at113153.png)

* **Tipos** : cómo se presentarán las opciones
   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**
* **Título** El título que se mostrará como la etiqueta de las opciones
* **Nombre** El nombre del campo enviado con los datos del formulario
* **Origen** donde se definen las opciones
   * **Local** definido dentro del componente
      * Toque o haga clic en el botón **Agregar** para agregar un valor, **Eliminar** para eliminarlo
      * **Valor** El valor guardado cuando se selecciona esa opción al enviar el formulario
      * **Texto** Etiqueta de la opción mostrada en el formulario
      * **Activo** La opción se marca como seleccionada cuando se carga el formulario
      * **Deshabilitada** La opción no se puede seleccionar pero se muestra
      * **Lista** Se utiliza una lista estática definida en otra parte de AEM para las opciones
         * **Lista** La ruta de la lista estática en AEM
            * Utilice el botón Examinar para localizar el recurso de lista
      * **Fuente** de datos Se utiliza una fuente de datos para las opciones
         * **Origen** de datos Tipo de recurso de la fuente de datos
* **Mensaje** de ayuda Una sugerencia para el usuario sobre lo que se puede introducir en el campo

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Opciones de formulario admite el sistema [de](authoring.md#component-styling)estilo AEM.