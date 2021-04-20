---
title: Componente de botón
description: El componente Botón del componente principal permite la creación y visualización de un botón.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Componente de botón{#button-component}

El componente Botón del componente principal permite la configuración y visualización de un elemento de botón en una página.

## Uso {#usage}

El componente Botón del componente principal permite la inclusión de un botón en una página.

* Las propiedades del botón se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los estilos del componente Botón se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente Botón, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_button).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Button [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el botón y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-properties.png)

* **Texto** : el texto que se mostrará en el botón.
* **Vínculo** : vínculo a una página de contenido dentro de AEM, un recurso externo o un anclaje
   * Utilice el **Cuadro de diálogo de selección** para elegir una ruta dentro de AEM.
* **Icono**  - Identificador para mostrar un icono en el botón
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas [ARIA accesibilidad](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta** : Valor de un atributo de etiqueta ARIA para el componente

## Diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Botón es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
