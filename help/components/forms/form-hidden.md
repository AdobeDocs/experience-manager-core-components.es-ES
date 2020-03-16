---
title: Componente oculto de formulario
description: El componente Formulario de componente principal oculto permite la visualización de un campo oculto.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente oculto de formulario{#form-hidden-component}

El componente Formulario de componente principal oculto permite la visualización de un campo oculto.

## Uso {#usage}

El componente Oculto del formulario de componente principal permite crear campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el componente [contenedor de](form-container.md)formularios.

El editor de contenido puede definir las propiedades del campo en el cuadro de diálogo [](form-hidden.md)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Formulario oculto es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Oculto del formulario y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_hidden)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Oculto del formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del campo oculto.

![](/help/assets/chlimage_1-26.png)

* **Nombre** El nombre del campo, que se envía con los datos del formulario
* **Valor** El valor del campo, que se envía con los datos del formulario
* **Identificador** El identificador debe ser único en la página y puede utilizarse para enlazar secuencias de comandos a este campo de formulario

Dado que el componente Formulario oculto normalmente no tiene atributos visibles, el marcador de posición del componente en el editor muestra los valores de campo **Nombre** y **Valor** si están asignados para ayudar al autor a identificar el componente Formulario oculto apropiado.

![](/help/assets/screenshot_2018-10-19at094927.png)

## Cuadro de diálogo Diseño {#design-dialog}

No hay ningún cuadro de diálogo de diseño para el componente Formulario oculto.
