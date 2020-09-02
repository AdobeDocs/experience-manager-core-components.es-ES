---
title: Configuraciones y componentes principales según el contexto de Sling
description: Los componentes principales aprovechan las configuraciones de Sling según el contexto para determinadas funciones
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Configuraciones y componentes principales según el contexto de Sling {#sling-context-aware-configurations}

Las configuraciones según el contexto son una característica de Sling y son configuraciones relacionadas con un recurso de contenido o un árbol de recursos y que son aprovechadas por los Componentes principales para permitir configuraciones en todo el sitio.

## Configuraciones según el contexto de Sling {#context-aware-configurations}

El sitio puede necesitar diferentes configuraciones para diferentes regiones del sitio, por ejemplo, algunos parámetros pueden compartirse y requerir herencia para contextos anidados y valores de reserva globales. Las configuraciones compatibles con contexto Sling lo habilitan.

Para obtener información detallada sobre las configuraciones compatibles con el contexto de Sling, [consulte la documentación de Apache.](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## Uso en los componentes principales {#core-components}

Varias funciones de componentes principales aprovechan las configuraciones según el contexto. Todas estas configuraciones se encuentran en el nodo siguiente:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Las configuraciones individuales dependen del componente o la función específicos. Las funciones de los componentes principales que utilizan configuraciones según el contexto son:

* [Componente de visor PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Compatibilidad con AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
