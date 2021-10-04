---
title: Configuraciones según el contexto y componentes principales de Sling
description: Los componentes principales aprovechan las configuraciones según el contexto de Sling para determinadas funciones
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 96%

---

# Configuraciones según el contexto y componentes principales de Sling {#sling-context-aware-configurations}

Las configuraciones según el contexto son una [función de Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Son configuraciones que están relacionadas con un recurso de contenido o un árbol de recursos y que los componentes principales aprovechan para permitir configuraciones en todo el sitio.

## Configuraciones según el contexto de Sling {#context-aware-configurations}

El sitio puede necesitar diferentes configuraciones para diferentes regiones del sitio, por ejemplo, donde algunos parámetros pueden compartirse y requieren herencia para contextos anidados y valores de reserva globales. AEM aprovecha las configuraciones según el contexto de Sling, que permiten esta posibilidad.

Para obtener más información sobre las configuraciones en AEM, consulte la [documentación de configuraciones y el explorador de configuración.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html)

## Uso en los componentes principales {#core-components}

Varias funciones de componentes principales aprovechan las configuraciones según el contexto. Todas estas configuraciones se encuentran en el siguiente nodo:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Las configuraciones individuales dependen del componente o la función específicos. Las funciones de los componentes principales que utilizan configuraciones según el contexto son:

* [Componente Visualizador de PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Compatibilidad con AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
