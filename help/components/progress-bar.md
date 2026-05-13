---
title: Componente Barra de progreso
description: El componente Barra de progreso representa visualmente el progreso hacia un objetivo
role: Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
TQID: https://experienceleague.adobe.com/Ovas6znS8-Pimv0hU5zPCnPuugjg2YyucQJbn1r6m8g
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 343
ht-degree: 100%

---

# Componente Barra de progreso {#progress-bar-component}

El componente principal Barra de progreso representa visualmente el progreso hacia un objetivo.

{{traditional-aem}}

## Uso {#usage}

El componente Barra de progreso permite al autor del contenido crear fácilmente una barra de progreso definiendo un porcentaje de finalización, lo que ofrece una visualización visual intuitiva del progreso hacia un objetivo.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Barra de progreso es la versión 1, que se introdujo con la versión 2.9.0 de los componentes principales en mayo de 2020 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Barra de progreso, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_progressbar_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Barra de progreso [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

![Cuadro de diálogo de edición del componente Barra de progreso](/help/assets/progress-bar-edit.png)

* **Finalización**: el progreso representado por un porcentaje
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente Barra de progreso.

### Pestaña Estilos {#styles-tab}

El componente Barra de progreso es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Barra de progreso es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
