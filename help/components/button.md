---
title: Componente de botón
description: El componente Botón del componente principal permite la creación y visualización de un botón.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 4%

---


# Componente de botón{#button-component}

El componente Botón del componente principal permite la configuración y visualización de un elemento de botón en una página.

## Uso {#usage}

El componente Botón del componente principal permite la inclusión de un botón en una página.

* Las propiedades del botón se pueden seleccionar en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los estilos del componente Botón se pueden definir en el cuadro de diálogo [](#design-dialog)de diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Botón, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_button)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_button_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el botón y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-properties.png)

* **Texto** : el texto que se va a mostrar en el botón
* **Vínculo** : vínculo a una página de contenido de AEM, un recurso externo o un anclaje
   * Utilice el cuadro de diálogo **** Selección para elegir una ruta dentro de AEM.
* **Icono** : identificador para mostrar un icono en el botón
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Ficha Accesibilidad {#accessibility-tab}

![Ficha Accesibilidad del cuadro de diálogo de edición del componente Botón](/help/assets/button-edit-accessibility.png)

En la ficha **Accesibilidad** , se pueden definir valores para las etiquetas de accesibilidad [de](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para el componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Imagen admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
