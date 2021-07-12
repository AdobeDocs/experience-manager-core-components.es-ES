---
title: Componente Botón del formulario (v1)
description: El componente Formulario oculto de componente principal permite incluir un campo oculto en un formulario.
index: n
role: Architect, Developer, Admin, User
exl-id: 2c06a942-7ac5-4847-9d11-7bbcd0ea51bd
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 3%

---

# Componente Botón del formulario (v1) {#form-button-component-v}

El componente Botón de formulario de componente principal permite la inclusión de un campo de botón en un formulario para el déclencheur de una acción.

## Uso {#usage}

El componente Botón de formulario de componente principal permite crear un campo de botón, a menudo para almacenar en déclencheur el envío del formulario y está pensado para utilizarse junto con el [componente de contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir las propiedades del botón en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Botón del formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Botón del formulario.

| Versión de AEM | Componente de botón de formulario v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Botón del formulario.
>
>Para obtener más información sobre la versión actual del componente Botón de formulario, consulte el documento [Componente de botón de formulario](/help/components/forms/form-button.md).

## Salida de componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-48.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales v1](/help/versions.md) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo configurar permite que el autor del contenido defina los parámetros del botón.

![](/help/assets/chlimage_1-49.png)

* **Tipo**
   * **Botón**
   * **Enviar**

* **Título** : texto que se muestra en el botón
   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón que se envía con los datos del formulario.
* **Valor** : el valor del botón que se envía con los datos del formulario.

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Botón del formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
