---
title: Componente Botón de formulario (v 1)
seo-title: Componente Botón de formulario (v 1)
description: nulo
seo-description: El componente de formulario de componente principal permite incluir un campo oculto en un formulario.
uuid: 0525 e 70 f -294 f -4 d 35-bf 96-fc 0 e 4 ec 225 e 9
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: ea 06 acc 0-38 e 2-4252-ac 29-07332835 b 7 c 4
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente Botón de formulario (v 1){#form-button-component-v}

El componente Botón de formulario de componente principal permite incluir un campo de botón en un formulario para activar una acción.

## Uso {#usage}

El componente Botón de formulario de componente principal permite crear campos de botón, con frecuencia para activar el envío del formulario y se pretende utilizarlo junto con [el componente contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del botón en el cuadro de diálogo [de configuración](form-button-v1.md#main-pars_title).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Botón de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de la versión 1 del componente Botón de formulario.

| Versión de AEM | Componente Botón de formulario v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe v 1 del componente Botón de formulario.
>
>Para obtener más información sobre la versión actual del componente Botón de formulario, consulte [el documento Componente](form-button.md) de botón de formulario.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del botón.

![](assets/chlimage_1-49.png)

* **Tipo**
   * **Botón**
   * **Enviar**

* **Título** : el texto que se muestra en el botón
   * Si ninguno siempre que el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón que se envía con los datos del formulario.
* **Valor** : valor del botón que se envía con los datos del formulario.

## Cuadro de diálogo de diseño {#design-dialog}

No hay un cuadro de diálogo de diseño para el componente Botón de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
