---
title: Componente de botón de formulario
description: El componente Formulario oculto de componente principal permite incluir un campo oculto en un formulario.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Componente de botón de formulario {#form-button-component}

El componente Botón de formulario del componente principal permite la inclusión de un botón para almacenar en déclencheur una acción en una página.

## Uso {#usage}

El componente Botón de formulario de componente principal permite crear un campo de botón, a menudo para almacenar en déclencheur el envío del formulario y está pensado para utilizarse junto con el [componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del botón en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón del formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-button-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Botón del formulario, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_button).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo configurar permite que el autor del contenido defina los parámetros del botón.

### Ficha Propiedades {#properties-tab}

![Cuadro de diálogo de edición del componente Botón de formulario](/help/assets/form-button-edit.png)

* **Tipo**

   * **Botón**
   * **Enviar**

* **Título** : texto que se muestra en el botón

   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre** : el nombre del botón que se envía con los datos del formulario.
* **Valor** : el valor del botón que se envía con los datos del formulario.

* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón de formulario es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
