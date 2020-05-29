---
title: Componente oculto de formulario
description: El componente Formulario de componente principal oculto permite la visualización de un campo oculto.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---


# Componente oculto de formulario{#form-hidden-component}

El componente Formulario de componente principal oculto permite la visualización de un campo oculto.

## Uso {#usage}

El componente Oculto del formulario de componente principal permite crear campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el componente [contenedor del](form-container.md)formulario.

El editor de contenido puede definir las propiedades del campo en el cuadro de diálogo [](form-hidden.md)configurar.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Formulario oculto es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Oculto del formulario y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_hidden)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Oculto del formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del campo oculto.

![Cuadro de diálogo de edición oculta del formulario](/help/assets/form-hidden-edit.png)

* **Nombre** : el nombre del campo, que se envía con los datos del formulario
* **Valor** : el valor del campo, que se envía con los datos del formulario.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

Dado que el componente Formulario oculto normalmente no tiene atributos visibles, el marcador de posición del componente en el editor muestra los valores de campo **Nombre** y **Valor** si están asignados para ayudar al autor a identificar el componente Formulario oculto apropiado.

![Ejemplo de componente oculto de formulario](/help/assets/form-hidden-example.png)

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Formulario oculto es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo de AEM.
