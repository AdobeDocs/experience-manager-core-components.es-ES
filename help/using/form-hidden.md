---
title: Componente oculto de formulario
seo-title: Componente oculto de formulario
description: nulo
seo-description: El componente Formulario de componente principal oculto permite la visualización de un campo oculto.
uuid: 63a1b381-f45c-4241-b743-dea8abd45e11
contentOwner: Usuario
content-type: referencia
topic-tags: componentes principales
discoiquuid: 36e49035-7641-4bad-8a61-723060032903
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente oculto de formulario{#form-hidden-component}

El componente Formulario de componente principal oculto permite la visualización de un campo oculto.

## Uso {#usage}

El componente Oculto del formulario de componente principal permite crear campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el componente [contenedor de](form-container.md)formularios.

El editor de contenido puede definir las propiedades del campo en el cuadro de diálogo [](form-hidden.md)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Formulario oculto es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-hidden-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
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
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente oculto de formulario [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del campo oculto.

![](assets/chlimage_1-26.png)

* **Nombre** El nombre del campo, que se envía con los datos del formulario
* **Valor** El valor del campo, que se envía con los datos del formulario
* **Identificador** El identificador debe ser único en la página y puede utilizarse para enlazar secuencias de comandos a este campo de formulario

Dado que el componente Formulario oculto normalmente no tiene atributos visibles, el marcador de posición del componente en el editor muestra los valores de campo **Nombre** y **Valor** si están asignados para ayudar al autor a identificar el componente Formulario oculto apropiado.

![](assets/screenshot_2018-10-19at094927.png)

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Formulario oculto.