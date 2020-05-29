---
title: Componente de separador
description: El componente separador crea un salto entre los componentes de una página
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 5%

---


# Componente de separador {#separator-component}

El componente separador de componentes principales muestra una regla horizontal para separar el contenido.

## Uso {#usage}

El componente Separador permite al autor del contenido crear fácilmente una regla horizontal como un salto entre el contenido para organizar mejor la información en una página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente separador es v1, que se introdujo con la versión 2.3.0 de los componentes principales en febrero de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Separador, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [](https://adobe.com/go/aem_cmp_library_separator)de componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente separador [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

![Cuadro de diálogo de edición del componente separador](/help/assets/separator-edit.png)

* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los estilos aplicados al componente separador.

### Ficha Estilos {#styles-tab}

El componente Separador admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
