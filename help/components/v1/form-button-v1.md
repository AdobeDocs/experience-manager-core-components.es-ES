---
title: Componente Botón de formulario (versión 1)
description: El componente principal Formulario oculto permite incluir un campo oculto en un formulario.
index: n
role: Architect, Developer, Admin, User
exl-id: 2c06a942-7ac5-4847-9d11-7bbcd0ea51bd
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Botón de formulario (versión 1) {#form-button-component-v}

El componente principal Botón de formulario permite incluir un campo de botón en un formulario para activar una acción.

## Uso {#usage}

El componente principal Botón de formulario permite crear un campo de botón, a menudo para activar el envío del formulario y está pensado para utilizarse junto con el [componente Contenedor de formulario](form-container-v1.md).

El editor de contenido puede definir las propiedades del botón en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Botón de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de la versión 1 del componente Botón de formulario.

| Versión de AEM | Componente Botón de formulario (versión 1) |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Botón de formulario.
>
>Para obtener más información sobre la versión actual del componente Botón de formulario, consulte el documento [Componente Botón de formulario](/help/components/forms/form-button.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite que el autor del contenido defina los parámetros del botón.

![](/help/assets/chlimage_1-49.png)

* **Tipo**
   * **Botón**
   * **Enviar**

* **Título**: texto que se muestra en el botón
   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre**: el nombre del botón, que se envía con los datos del formulario
* **Valor:** el valor del botón, que se envía con los datos del formulario

## Cuadro de diálogo de diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Botón de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
