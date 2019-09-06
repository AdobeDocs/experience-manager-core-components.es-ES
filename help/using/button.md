---
title: Componente Botón
seo-title: Componente Botón
description: nulo
seo-description: El componente Botón de componente principal permite crear y visualizar un botón.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: d37cde072dea612ccb55ad31b4aaf42f17839cb4

---


# Componente Botón{#button-component}

El componente Botón Componente Core permite la configuración y visualización de un elemento de botón en una página.

## Uso {#usage}

El componente Botón de componente principal permite incluir un botón en una página.

* Las propiedades del botón se pueden seleccionar en el cuadro de diálogo [de configuración](#configure-dialog).
* Los estilos del componente Botón pueden definirse en el cuadro de diálogo [de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón es v 1, introducida con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Botón, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/button.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor de contenido definir el botón y cómo se comportará y aparecerá para un visitante de la página.

### Ficha Propiedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.19.32.png)

* **Texto** : El texto que se va a mostrar en el botón
* **Vínculo** : vínculo a una página de contenido dentro de AEM, un recurso externo o un anclaje
   * Utilice el cuadro de diálogo **Selección** para elegir una ruta dentro de AEM.
* **Icono** : identificador para mostrar un icono en el botón

### Ficha Accesibilidad {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.19.43.png)

En la ficha **Accesibilidad** , los valores se pueden definir para [las etiquetas de accesibilidad](https://www.w3.org/WAI/standards-guidelines/aria/) de ARIA para el componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Cuadro de diálogo de diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Imagen admite [el sistema de estilos AEM](authoring.md#component-styling).
