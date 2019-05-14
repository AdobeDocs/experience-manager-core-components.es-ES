---
title: Componente de fragmento de contenido
seo-title: Componente de fragmento de contenido
description: nulo
seo-description: El componente Fragmento de contenido de componente principal permite mostrar un fragmento de contenido.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 40ce01fdb0f22e3ee3b376a3684a766bd7e7bc11

---


# Componente de fragmento de contenido{#content-fragment-component}

El componente Fragmento de contenido de componente principal permite mostrar un [fragmento de contenido](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

>[!NOTE]
>
>Antes de la versión 2.4.0 de los componentes principales, el componente Fragmento de contenido estaba disponible como extensión para los componentes principales y tenía que descargarse por separado y habilitarse de forma explícita.

## Uso {#usage}

El componente de fragmento de contenido de componente principal permite incluir un fragmento [de contenido](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) en una página.

* El fragmento y sus propiedades se pueden seleccionar en el cuadro de diálogo [de configuración](#configure-dialog).
* Los tipos de recursos para gestionar determinadas imágenes y cuadrículas se pueden definir en el cuadro de diálogo [de diseño](#design-dialog).
* La opción de edición abrirá el fragmento seleccionado dentro del [editor](https://helpx.adobe.com/content/help/en/experience-manager/6-5/assets/using/content-fragments.html)de fragmentos de contenido.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido es v 1, que se introdujo con la versión 1.1.0 de los componentes principales en octubre de 2017 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente Fragmento de contenido, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de contenido [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragment/v1/contentfragment).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite que el autor de contenido defina el fragmento de contenido y los elementos del fragmento que se van a incluir.

![](assets/chlimage_1-87.png)

* **Fragmento de contenido**

   * Ruta al fragmento de contenido deseado
   * El cuadro de diálogo **Selección** se puede utilizar para ubicar el fragmento

* **Elemento** : elemento del fragmento de contenido que se incluirá
* **Variación** : la variación del fragmento de contenido que se va a utilizar (el valor predeterminado **es Maestro**)

* **Párrafos**

   * **Todos** : mostrar todos los párrafos
   * **Intervalo**

      * Especifique los rangos de párrafos que deben mostrarse, separados por un punto y coma
      * Por ejemplo `1;3-5;7;9-*` : incluir el primer, el quinto y el quinto, el 7 y el 9 a los últimos párrafos

* **Encabezado de control como sus propios párrafos**

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los tipos de recurso utilizados para gestionar imágenes de medios mixtos y cuadrículas interactivas.

![](assets/chlimage_1-88.png)

* **Tipo de imagen de medios mixtos**

   * Un tipo de recurso de sling que se utiliza para procesar imágenes de medios mixtos

* **Cuadrícula interactiva interna**

   * El tipo de recurso de sling que se utiliza para la cuadrícula interactiva interna