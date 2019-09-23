---
title: Componente de texto de formulario
seo-title: Componente de texto de formulario
description: nulo
seo-description: The Core Component Form Text component allows the entry of form text for submission.
uuid: f2418d55-0b59-4c7c-a541-d12dda4db4cf
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 3a970c4b-806b-4a0a-b6b8-b3dca4e9f136
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


# Form Text Component{#form-text-component}

The Core Component Form Text component allows the entry of form text for submission.

## Uso {#usage}

The Form Text component allows for the submission of different types of text and is intended to be used along with the form container component. [](form-container.md) The type of text validation, labels, and help messages can be defined by the content editor in the configure dialog.[](#configure-dialog)

## Version and Compatibility {#version-and-compatibility}

The current version of the Form Text Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

| Component Version | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-text-v1.md) | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document Core Components Versions.[](versions.md)

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="text aem-GridColumn aem-GridColumn--default--12">
   <div class="cmp-form-text">
      <label for="form-text-2146967">How many pieces of toast would you like?
      </label>
   <input class="cmp-form-text__text" type="number" id="form-text-2146967" name="pieces">
   </div>
</div>
```

### JSON {#json}

```
"text":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "id":"form-text-2146967",
                     "title":"How many pieces of toast would you like?",
                     "name":"pieces",
                     "value":"",
                     "helpMessage":"",
                     "type":"number",
                     "readOnly":false,
                     "required":false,
                     "requiredMessage":"",
                     "constraintMessage":"",
                     "rows":2,
                     "defaultValue":"",
                     ":type":"core/wcm/components/form/text/v2/text"
                  }
```

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Texto del formulario [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de texto que se debe introducir, así como los valores y etiquetas predeterminados.

### Ficha Principal {#main-tab}

![](assets/chlimage_1-23.png)

* **Restricción** El tipo de texto que se va a introducir y se validará con
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas** de texto Número de líneas que se mostrarán en el área de texto (solo se muestran cuando **Restricción** se establece en Área **de** texto)
* **Etiqueta** Etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para que no se muestre** Necesario si la etiqueta es necesaria solo para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre** del elemento El nombre del campo que se envía con los datos del formulario
* **Valor** predeterminado que se rellena previamente en el campo

### Ficha Acerca de {#about-tab}

![](assets/chlimage_1-24.png)

* **Mensaje** de ayuda Una sugerencia para el usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición** Para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando esté vacío y no esté centrado

### Ficha Restricciones {#constraints-tab}

![](assets/chlimage_1-25.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para los tipos de restricción **Texto** y Área **de texto**
* **Obligatorio** Si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
* **Convertir en solo** lectura Si se selecciona, el usuario no puede modificar el valor del campo

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Texto de formulario.