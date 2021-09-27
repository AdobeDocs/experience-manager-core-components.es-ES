---
title: Componente Separador
description: El componente Separador crea un salto entre los componentes de una página
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '304'
ht-degree: 100%

---

# Componente Separador {#separator-component}

El componente principal Separador muestra una regla horizontal para separar el contenido.

## Uso {#usage}

El componente Separador permite al autor del contenido crear fácilmente una regla horizontal como un salto entre el contenido para organizar mejor la información en una página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Separador es la versión 1, que se introdujo con la versión 2.3.0 de los componentes principales en febrero de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | Compatible | Compatible |

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
