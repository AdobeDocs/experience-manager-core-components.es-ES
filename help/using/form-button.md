---
title: Componente Botón de formulario
seo-title: Componente Botón de formulario
description: nulo
seo-description: El componente de formulario de componente principal permite incluir un campo oculto en un formulario.
uuid: 22 c 53 cd 0-d 0 bc -4 e 5 d -89 f 3-5 ac 4 f 61 a 9100
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 6 e 2974 a -243 f -40 ab -903 c-c 7 d 3 e 8615 bcc
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


# Componente Botón de formulario{#form-button-component}

El componente Botón de formulario de componente principal permite incluir un botón para activar una acción en una página.

## Uso {#usage}

El componente Botón de formulario de componente principal permite crear campos de botón, con frecuencia para activar el envío del formulario y está pensado que se utilice junto con [el componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del botón en el cuadro de diálogo [de configuración](form-button.md).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón de formulario es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-button-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/screen_shot_2018-01-12at120021.png)

### HTML {#html}

```
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="button aem-GridColumn aem-GridColumn--default--12">
<button type="BUTTON" class="cmp-form-button" name="loveToast" value="ILoveToast">Click here if you love toast!</button>
</div>

</form>
</div>
```

### JSON {#json}

```
"button":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           ":type":"core/wcm/sandbox/components/form/button/v2/button",
                           "name":"loveToast",
                           "jcr:title":"Click here if you love toast!",
                           "type":"button",
                           "value":"ILoveToast"
                        }
```

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del botón.

### Ficha Propiedades {#properties-tab}

![](assets/screen_shot_2018-01-12at120433.png)

* **Tipo**

   * **Botón**
   * **Enviar**

* **Título** : el texto que se muestra en el botón

   * Si ninguno siempre que el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón que se envía con los datos del formulario.
* **Valor** : valor del botón que se envía con los datos del formulario.

## Cuadro de diálogo de diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Botón de formulario admite el sistema [de estilos AEM](authoring.md#component-styling).