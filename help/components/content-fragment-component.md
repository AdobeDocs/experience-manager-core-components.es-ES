---
title: Componente Fragmento de contenido
description: El componente principal Fragmento de contenido permite ver un fragmento de contenido.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 100%

---


# Componente Fragmento de contenido {#content-fragment-component}

El componente principal Fragmento de contenido permite ver un [fragmento de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es).

>[!NOTE]
>
>Antes de la versión 2.4.0 de los componentes principales, el componente Fragmento de contenido estaba disponible como extensión para los componentes principales y tenía que descargarse por separado y habilitarse explícitamente.

{{traditional-aem}}

## Uso {#usage}

El componente principal Fragmento de contenido permite incluir un [fragmento de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es) en una página.

* El fragmento y sus propiedades se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los tipos de recursos para gestionar ciertas imágenes y cuadrículas se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).
* La opción de edición abrirá el fragmento seleccionado dentro del [editor de fragmentos de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html?lang=es).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido es la versión 1, que se introdujo con la versión 1.1.0 de los componentes principales en octubre de 2017 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |

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
>Aunque ambos corresponden a la versión 1, cualquier componente Fragmento de contenido que se haya utilizado desde la carpeta de extensiones requerirá una migración de sus componentes proxy relacionados para utilizar el nuevo tipo de recurso al actualizar a la versión 2.4.0 o superior de los componentes principales.

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Fragmento de contenido, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cf_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de contenido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué fragmento de contenido y qué elementos de ese fragmento se incluyen.

### Pestaña Propiedades {#properties-tab}

![Componente Fragmento de contenido](/help/assets/content-fragment-edit-properties.png)

* **Fragmento de contenido**

   * Ruta al fragmento de contenido deseado
   * Se puede utilizar el **Cuadro de diálogo de selección** para localizar el fragmento

* **Modo de visualización**
   * **Elemento de texto único**: permite la selección de un elemento de texto multilínea y activa las opciones de control de párrafo
   * **Varios elementos**: permite seleccionar uno o varios elementos del fragmento de contenido seleccionado
* **Elemento**: el elemento o elementos del fragmento de contenido que se van a incluir.
* **Variación**: qué variación del fragmento de contenido se va a utilizar (el valor predeterminado es **Principal**)

* **Párrafos**

   * **Todo**: mostrar todos los párrafos
   * **Intervalo**

      * Especifique los intervalos de párrafos que se deben mostrar, separados por punto y coma
      * Por ejemplo, `1;3-5;7;9-*` para incluir los párrafos primero, tercero a quinto, séptimo y noveno en los párrafos finales
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Control de párrafo {#paragraph-control-tab}

Esta pestaña no está disponible cuando el modo **Varios elementos** está seleccionado.

![Componente Fragmento de contenido](/help/assets/content-fragment-edit-paragraph.png)

* **Párrafos**: permite seleccionar todos los párrafos o un intervalo
* **Gestionar encabezados como sus propios párrafos**

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina los tipos de recurso utilizados para gestionar imágenes de medios mixtos y cuadrículas adaptables.

![Cuadro de diálogo Diseño del componente Fragmento de contenido](/help/assets/content-fragment-design.png)

* **Cuadrícula interactiva interna**

   * El tipo de recurso de sling que se utiliza para la cuadrícula interactiva interna

## Capa de datos del cliente de Adobe {#data-layer}

El componente Fragmento de contenido es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
