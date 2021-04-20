---
title: Componente oculto de formulario (v1)
description: El componente Formulario oculto de componente principal permite la visualización de un campo oculto.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 2%

---


# Componente oculto de formulario (v1) {#form-hidden-component-v}

El componente Formulario oculto de componente principal permite la visualización de un campo oculto.

## Uso {#usage}

El componente Formulario oculto de componente principal permite la creación de campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el [componente de contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir las propiedades del campo en el cuadro de diálogo [configurar](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente oculto de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de v1 del componente oculto del formulario.

| Versión de AEM | Componente oculto de formulario v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente oculto de formulario.
>
>Para obtener más información sobre la versión actual del componente oculto de formulario, consulte el documento [Componente oculto de formulario](/help/components/forms/form-hidden.md).

## Salida de componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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

>[!NOTE]
>
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales v1](/help/versions.md#release-history-and-compatibility) para obtener más información.

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo configurar permite al autor del contenido definir los parámetros del campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nombre** : el nombre del campo que se envía con los datos del formulario.
* **Valor** : el valor del campo que se envía con los datos del formulario.
* **Identificador** : el identificador debe ser único en la página y se puede utilizar para enlazar secuencias de comandos a este campo de formulario

## Diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Formulario oculto.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente oculto de formulario [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
