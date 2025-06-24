---
title: Componente Botón (versión 1)
description: El componente principal Botón permite crear y visualizar un botón.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 98%

---


# Componente Botón (versión 1) {#button-component}

El componente principal Botón permite configurar y mostrar un elemento de botón en una página.

## Uso {#usage}

El componente principal Botón permite incluir un botón en una página.

* Las propiedades del botón se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los estilos del componente Botón se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

El documento describe la versión 1 del componente Botón, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019.

>[!CAUTION]
>
>Este documento describe la versión 1 del componente botón.
>
>Para obtener más información sobre la versión actual del componente Botón, consulte el documento [Componente Botón](/help/components/button.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Botón, así como ver ejemplos de sus opciones de configuración, además de la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_button).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_button_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el botón y cómo se comportará y aparecerá para un visitante de la página.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-properties.png)

* **Texto**: Texto que se muestra en el botón
* **Vínculo**: vínculo a una página de contenido dentro de AEM, un recurso externo o un anclaje
   * Utilice el **Cuadro de diálogo de selección** para elegir una ruta dentro de AEM.
* **Icono**: Identificador de iconos para mostrar un icono en el botón
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: Valor de un atributo de etiqueta ARIA para el componente

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Botón es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
