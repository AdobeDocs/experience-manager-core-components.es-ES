---
title: Componente Formulario oculto (versión 1)
description: El componente principal Formulario oculto permite ver un campo oculto.
index: false
role: Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
TQID: https://experienceleague.adobe.com/rMf4285S77F8hsmwcgo24Bd39eDl13nozM6KZFCuPqY
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 344
ht-degree: 100%

---

# Componente Formulario oculto (versión 1) {#form-hidden-component-v}

El componente principal Formulario oculto permite ver un campo oculto.

## Uso {#usage}

El componente principal Formulario oculto permite crear campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el [componente Contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir las propiedades del campo en el [cuadro de diálogo de configuación](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Formulario oculto, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de la versión 1 del componente Formulario oculto.

| Versión de AEM | Componente Formulario oculto (versión 1) |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Formulario oculto.
>
>Para obtener más información sobre la versión actual del componente Formulario oculto, consulte el documento [Componente Formulario oculto](/help/components/forms/form-hidden.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md#release-history-and-compatibility) para obtener más información.

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nombre**: el nombre del campo, que se envía con los datos del formulario
* **Valor:** el valor del campo, que se envía con los datos del formulario
* **Identificador**: el identificador debe ser único en la página y se puede utilizar para vincular secuencias de comandos a este campo de formulario

## Cuadro de diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Formulario oculto.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Formulario oculto [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
