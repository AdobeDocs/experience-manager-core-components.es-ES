---
title: Servlet de imagen adaptable
description: Descubra cómo los componentes principales utilizan el servlet de imagen adaptable para la entrega de imágenes y cómo puede optimizarlo.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 420e6085da57e5dc6deb670a5f0498b018441cb8
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 61%

---

# Servlet de imagen adaptable {#adaptive-image-servlet}

Descubra cómo los componentes principales utilizan el servlet de imagen adaptable para la entrega de imágenes y cómo puede optimizarlo.

## ¿Servicio de imagen adaptable o entrega de imágenes optimizadas para la web? {#options}

El componente principal de imagen puede utilizar dos métodos para entregar imágenes.

* El servlet de imagen adaptable es el predeterminado.
* [Entrega de imágenes optimizadas para la web](/help/developing/web-optimized-image-delivery.md) está disponible para AEMaaCS y reduce el tamaño de descarga en un 25 % de media.

Este documento describe el servlet de imagen adaptable predeterminado.

## Información general {#overview}

De forma predeterminada, el componente de imagen utiliza el servlet de imagen adaptable del componente principal para ofrecer imágenes. [El servlet de imagen adaptable](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) es responsable del procesamiento y la transmisión de imágenes y los desarrolladores pueden aprovecharlo en sus [personalizaciones de los componentes principales](/help/developing/customizing.md).

## Selección de representación {#rendition-selection}

El servlet de imagen adaptable seleccionará automáticamente la representación más adecuada para mostrar en función del tamaño del contenedor en el que se muestra. El proceso de selección de la representación es el siguiente.

1. El servlet de imagen adaptable revisa todas las representaciones disponibles del recurso de imagen.
1. Solo selecciona los que tienen el mismo mime/tipo del recurso al que se hace referencia original.
   * Por ejemplo, si el recurso original era un PNG, solo tendrá en cuenta las representaciones PNG.
1. De esas representaciones, considera las dimensiones y las compara con el tamaño del contenedor en el que se debe mostrar la imagen.
   1. Si la representación es >= el tamaño del contenedor, se agrega a una lista de representaciones candidatas.
   1. Si la representación es &lt; el tamaño del contenedor, no se tiene en cuenta.
   1. Estos criterios garantizan que la representación no se actualice, lo que afectaría a la calidad de la imagen.
1. A continuación, el servlet de imagen adaptable selecciona la representación con el tamaño de archivo más pequeño de la lista de candidatos.

## Optimización de la selección de representaciones {#optimizing-rendition-selection}

Adaptive Image Servlet intentará elegir la mejor representación para el tamaño y tipo de imagen solicitado. Se recomienda que las representaciones DAM y los anchos permitidos de los componentes de imagen se definan de forma sincronizada, de modo que Adaptive Image Servlet realice el menor procesamiento posible.

Esto mejorará el rendimiento y evitará que la biblioteca de procesamiento de imágenes subyacente no procese correctamente algunas imágenes.

## Uso de encabezados de última modificación {#last-modified}

Las solicitudes condicionales a través del encabezado `Last-Modified` son compatibles con el servlet de imagen adaptable, pero el almacenamiento en caché del encabezado `Last-Modified` [debe habilitarse en Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=es#caching-http-response-headers).

La configuración de Dispatcher de ejemplo [del tipo de archivo del proyecto de AEM](/help/developing/archetype/overview.md) ya contiene esta configuración.
