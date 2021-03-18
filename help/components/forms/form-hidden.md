---
title: Componente oculto de formulario
description: El componente Formulario oculto de componente principal permite la visualización de un campo oculto.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 3%

---


# Componente oculto de formulario{#form-hidden-component}

El componente Formulario oculto de componente principal permite la visualización de un campo oculto.

## Uso {#usage}

El componente Formulario oculto de componente principal permite la creación de campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el [componente de contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del campo en el cuadro de diálogo [configurar](form-hidden.md).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente oculto de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente oculto del formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_hidden).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente oculto de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo configurar permite al autor del contenido definir los parámetros del campo oculto.

![Cuadro de diálogo de edición oculta de formulario](/help/assets/form-hidden-edit.png)

* **Nombre** : el nombre del campo que se envía con los datos del formulario.
* **Valor** : el valor del campo que se envía con los datos del formulario.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

Dado que el componente Oculto del formulario normalmente no tiene atributos visibles, el marcador de posición del componente en el editor muestra los valores de campo **Name** y **Value** si están asignados para ayudar al autor a identificar el componente oculto del formulario correspondiente.

![Ejemplo de componente oculto de formulario](/help/assets/form-hidden-example.png)

## Diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente oculto de formulario es compatible con el sistema de estilos AEM [](/help/get-started/authoring.md#component-styling).
