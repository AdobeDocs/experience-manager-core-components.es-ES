---
title: Componente de botón de formulario
description: El componente Formulario oculto de componente principal permite incluir un campo oculto en un formulario.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Form Button Component {#form-button-component}

El componente Botón de formulario de componente principal permite la inclusión de un botón para activar una acción en una página.

## Uso {#usage}

El componente Botón de formulario de componente principal permite la creación de un campo de botón, a menudo para activar el envío del formulario y está diseñado para utilizarse junto con el componente [Contenedor de](form-container.md)formulario.

El editor de contenido puede definir las propiedades del botón en el cuadro de diálogo [](#configure-dialog)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-button-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Botón de formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_button)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del botón.

### Ficha Propiedades {#properties-tab}

![](/help/assets/screen_shot_2018-01-12at120433.png)

* **Tipo**

   * **Botón**
   * **Enviar**

* **Título** : el texto que se muestra en el botón

   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón, que se envía con los datos del formulario
* **Valor** : el valor del botón, que se envía con los datos del formulario

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Botón de formulario admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.