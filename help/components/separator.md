---
title: Componente Separador
description: El componente Separador crea un salto entre los componentes de una página
role: Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
TQID: https://experienceleague.adobe.com/phmSUsqkY69wmGhAtWuj1qvFcjr84gPe2H90CsKVAAE
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 309
ht-degree: 100%

---

# Componente Separador {#separator-component}

El componente principal Separador muestra una regla horizontal para separar el contenido.

{{traditional-aem}}

## Uso {#usage}

El componente Separador permite al autor del contenido crear fácilmente una regla horizontal como un salto entre el contenido para organizar mejor la información en una página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Separador es la versión 1, que se introdujo con la versión 2.3.0 de los componentes principales en febrero de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Separador, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_separator_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Separador [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

![Cuadro de diálogo de edición del componente Separador](/help/assets/separator-edit.png)

* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente Separador.

### Pestaña Estilos {#styles-tab}

El componente Separador es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).
