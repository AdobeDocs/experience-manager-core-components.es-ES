---
title: Componente de texto de formulario
seo-title: Componente de texto de formulario
description: nulo
seo-description: El componente de texto de formulario de componente principal permite la entrada del texto del formulario para su envío.
uuid: f 2418 d 55-0 b 59-4 c 7 c-a 541-d 12 dda 4 db 4 cf
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 a 970 c 4 b -806 b -4 a 0 a-b 6 b 8-b 3 dca 4 e 9 f 136
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de texto de formulario{#form-text-component}

El componente de texto de formulario de componente principal permite la entrada del texto del formulario para su envío.

## Uso {#usage}

El componente Texto de formulario permite enviar distintos tipos de texto y está pensado que se utilice junto con [el componente Contenedor de formulario](form-container.md). El editor de contenido del cuadro de diálogo [de configuración puede definir el tipo de validación de texto, etiquetas y mensajes de ayuda](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de texto de formulario es v 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](form-text-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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

La documentación técnica más reciente sobre el componente de texto de formulario [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el tipo de texto que se va a introducir como así también los valores y etiquetas predeterminados.

### Ficha Principal {#main-tab}

![](assets/chlimage_1-23.png)

* **Restricción**
El tipo de texto que se va a introducir y se validará con
   * **Texto**
   * **Área de texto**
   * **Correo electrónico**
   * **Tel.**
   * **Fecha**
   * **Número**
   * **Contraseña**
* **Líneas
de texto** Número de líneas que se mostrarán en el área de texto (solo se muestra cuando **la restricción** se define como **Área de texto**)
* **Etiqueta**
La etiqueta que se mostrará para el campo
* **Ocultar la etiqueta para**que se muestre necesario
si la etiqueta es necesaria solo para fines de accesibilidad y no proporciona información visual adicional sobre el campo
* **Nombre
del elemento** El nombre del campo que se envía con los datos del formulario
* **Valor**predeterminado Valor
predefinido en el campo

### Acerca de la ficha {#about-tab}

![](assets/chlimage_1-24.png)

* **Mensaje**
de ayuda Una sugerencia al usuario de lo que se puede introducir en el campo
* **Mostrar mensaje de ayuda como marcador de posición**
Para mostrar el mensaje de ayuda dentro de la entrada del formulario cuando esté vacío y no está enfocado

### Ficha Restricciones {#constraints-tab}

![](assets/chlimage_1-25.png)

* **Mensaje de restricción**
   * El mensaje se muestra como información cuando se envía el formulario si el valor no valida el tipo elegido
   * No se muestra para **los tipos de restricción Texto** y **Área** de texto
* **Obligatorio**
Si se selecciona, el usuario debe rellenar un valor antes de enviar el formulario
* **Hacer lectura solo** si se selecciona el usuario no puede modificar el valor del campo

## Cuadro de diálogo de diseño {#design-dialog}

No hay un cuadro de diálogo de diseño para el componente Texto de formulario.