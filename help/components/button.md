---
title: Componente Botón
description: El componente principal Botón permite crear y visualizar un botón.
role: Developer, Admin, User
exl-id: e17efd1d-90d4-497a-9e7d-45934d81bc28
TQID: https://experienceleague.adobe.com/u7y51o7kFmth4WgbZX9wLuhY-hz90LjJ1-0Fr-00iVc
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 545
ht-degree: 100%

---

# Componente Botón{#button-component}

El componente principal Botón permite configurar y mostrar un elemento de botón en una página.

{{traditional-aem}}

## Uso {#usage}

El componente principal Botón permite incluir un botón en una página.

* Las propiedades del botón se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los estilos del componente Botón se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](v1/button.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Botón, así como ver ejemplos de sus opciones de configuración, además de la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_button_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_button_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el botón y cómo se comportará y aparecerá para un visitante de la página.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-properties.png)

* **Texto**: Texto que se muestra en el botón
* **Vínculo**: vínculo a una página de contenido dentro de AEM, un recurso externo o un anclaje
   * Utilice el **Cuadro de diálogo de selección** para elegir una ruta dentro de AEM.
* **Abrir en ficha nueva**: si se selecciona, el vínculo se abre en una nueva pestaña del explorador.
* **Icono**: Identificador de iconos para mostrar un icono en el botón
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: Valor de un atributo de etiqueta ARIA para el componente

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-styles.png)

El componente Botón es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Botón es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
