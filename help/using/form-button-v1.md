---
title: Componente Botón de formulario (v1)
seo-title: Componente Botón de formulario (v1)
description: nulo
seo-description: El componente Formulario oculto de componente principal permite incluir un campo oculto en un formulario.
uuid: 0525e70f-294f-4d35-bf96-fc0e4ec225e9
content-type: referencia
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: ea06acc0-38e2-4252-ac29-07332835b7c4
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Form Button Component (v1){#form-button-component-v}

El componente Botón de formulario de componente principal permite incluir un campo de botón en un formulario para activar una acción.

## Uso {#usage}

El componente Botón de formulario de componente principal permite la creación de un campo de botón, a menudo para activar el envío del formulario y está diseñado para utilizarse junto con el componente [contenedor de](form-container.md)formulario.

El editor de contenido puede definir las propiedades del botón en el cuadro de diálogo [](form-button-v1.md#main-pars_title)configurar.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Botón de formulario, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente Botón de formulario.

| Versión de AEM | Componente de botón de formulario v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Botón de formulario.
>
>Para obtener más información sobre la versión actual del componente Botón de formulario, consulte el documento Componente [Botón de](form-button.md) formulario.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del botón.

![](assets/chlimage_1-49.png)

* **Tipo**
   * **Botón**
   * **Enviar**

* **Título** : el texto que se muestra en el botón
   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón, que se envía con los datos del formulario
* **Valor** : el valor del botón, que se envía con los datos del formulario

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Botón de formulario.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.
