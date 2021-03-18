---
title: Componente de fragmento de contenido
description: El componente Fragmento de contenido del componente principal permite la visualización de un fragmento de contenido.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 7%

---


# Componente de fragmento de contenido{#content-fragment-component}

El componente Fragmento de contenido del componente principal permite la visualización de un [fragmento de contenido](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Antes de la versión 2.4.0 de los componentes principales, el componente Fragmento de contenido estaba disponible como extensión para los componentes principales y tenía que descargarse por separado y habilitarse explícitamente.

## Uso {#usage}

El componente de fragmento de contenido del componente principal permite la inclusión de un [fragmento de contenido](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) en una página.

* El fragmento y sus propiedades se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los tipos de recursos para gestionar ciertas imágenes y cuadrículas se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).
* La opción de edición abrirá el fragmento seleccionado dentro del [editor de fragmentos de contenido](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de fragmento de contenido es v1, que se introdujo con la versión 1.1.0 de los componentes principales en octubre de 2017 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

>[!NOTE]
>
>Antes de la versión 2.4.0, el componente Fragmento de contenido se encontraba en la carpeta de extensiones.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>Desde la versión 2.4.0 se ha movido a la siguiente ubicación.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Aunque ambos son v1, cualquier componente de fragmento de contenido que se haya utilizado desde la carpeta de extensiones requerirá una migración de sus componentes proxy relacionados para utilizar el nuevo tipo de recurso al actualizar a la versión 2.4.0 o superior de los componentes principales.

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente Fragmento de contenido, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cf).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de fragmento de contenido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué fragmento de contenido y qué elementos de ese fragmento se incluyen.

### Ficha Propiedades {#properties-tab}

![Componente de fragmento de contenido](/help/assets/content-fragment-edit-properties.png)

* **Fragmento de contenido**

   * Ruta al fragmento de contenido deseado
   * Se puede utilizar el **Cuadro de diálogo de selección** para localizar el fragmento

* **Modo de visualización**
   * **Elemento de texto único** : permite la selección de un elemento de texto multilínea y activa las opciones de control de párrafo
   * **Varios elementos** : permite seleccionar uno o varios elementos del fragmento de contenido seleccionado
* **Elemento** : el elemento o elementos del fragmento de contenido que se va a incluir.
* **Variación** : qué variación del fragmento de contenido se va a utilizar (el valor predeterminado es  **Principal**)

* **Párrafos**

   * **Todo** : mostrar todos los párrafos
   * **Intervalo**

      * Especifique intervalos de párrafos que se deben mostrar, separados por punto y coma
      * Por ejemplo, `1;3-5;7;9-*` para incluir los párrafos primero, tercero a quinto, séptimo y noveno en los párrafos finales
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### Pestaña Control de párrafo {#paragraph-control-tab}

Esta pestaña no está disponible cuando el modo **Multiple Elements** está seleccionado.

![Componente de fragmento de contenido](/help/assets/content-fragment-edit-paragraph.png)

* **Párrafos** : permite seleccionar todos los párrafos o un intervalo
* **Gestionar encabezado como sus propios párrafos**

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los tipos de recurso utilizados para gestionar imágenes de medios mixtos y cuadrículas adaptables.

![Cuadro de diálogo Diseño del componente Fragmento de contenido](/help/assets/content-fragment-design.png)

* **Cuadrícula interactiva interna**

   * El tipo de recurso de sling que se utiliza para la cuadrícula interactiva interna

## Capa de datos del cliente de Adobe {#data-layer}

El componente Fragmento de contenido es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
