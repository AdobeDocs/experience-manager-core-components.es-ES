---
title: Componente de separador
description: El componente separador crea un salto entre los componentes de una página
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 5%

---


# Componente de separador {#separator-component}

El componente separador de componentes principales muestra una regla horizontal para separar el contenido.

## Uso {#usage}

El componente separador permite al autor del contenido crear fácilmente una regla horizontal como un salto entre el contenido para organizar mejor la información en una página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente separador es v1, que se introdujo con la versión 2.3.0 de los componentes principales en febrero de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente separador, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_separator).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente separador [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

![Cuadro de diálogo de edición del componente separador](/help/assets/separator-edit.png)

* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente separador.

### Pestaña Estilos {#styles-tab}

El componente separador es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
