---
title: Componente Formulario oculto
description: El componente principal Formulario oculto permite ver un campo oculto.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 99%

---

# Componente Formulario oculto {#form-hidden-component}

El componente principal Formulario oculto permite ver un campo oculto.

## Uso {#usage}

El componente principal Formulario oculto permite crear campos ocultos para devolver a AEM la información sobre la página actual y está diseñado para utilizarse junto con el [componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del campo en el [cuadro de diálogo de configuación](form-hidden.md).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Formulario oculto es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 2 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/form-hidden-v1.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Formulario oculto, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_hidden_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Formulario oculto [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir los parámetros del campo oculto.

![Cuadro de diálogo de edición de Formulario oculto](/help/assets/form-hidden-edit.png)

* **Nombre**: el nombre del campo, que se envía con los datos del formulario
* **Valor:** el valor del campo, que se envía con los datos del formulario
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

Dado que el componente Formulario oculto normalmente no tiene atributos visibles, el marcador de posición del componente en el editor muestra los valores de campo **Nombre** y **Valor** si están asignados para ayudar al autor a identificar el componente oculto del formulario correspondiente.

![Ejemplo de componente Formulariooculto](/help/assets/form-hidden-example.png)

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Formulario oculto es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) AEM.
