---
title: Configuraciones y componentes principales según el contexto de Sling
description: Los componentes principales aprovechan las configuraciones de Sling según el contexto para determinadas funciones
translation-type: tm+mt
source-git-commit: 11e2c6da0fa93084b601437fd45fd65dd8d73231
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# Configuraciones y componentes principales según el contexto de Sling {#sling-context-aware-configurations}

Las configuraciones según el contexto son una característica de Sling y son configuraciones relacionadas con un recurso de contenido o un árbol de recursos y que son aprovechadas por los Componentes principales para permitir configuraciones en todo el sitio.

## Configuraciones según el contexto de Sling {#context-aware-configurations}

El sitio puede necesitar diferentes configuraciones para diferentes regiones del sitio, por ejemplo, algunos parámetros pueden compartirse y requerir herencia para contextos anidados y valores de reserva globales. AEM aprovecha las configuraciones según el contexto de Sling, que permiten esta posibilidad.

Para obtener más información sobre las configuraciones en AEM, [consulte la documentación Configuraciones y Navegador de configuración.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/configurations.html)

## Uso en los componentes principales {#core-components}

Varias funciones de componentes principales aprovechan las configuraciones según el contexto. Todas estas configuraciones se encuentran en el nodo siguiente:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Las configuraciones individuales dependen del componente o la función específicos. Las funciones de los componentes principales que utilizan configuraciones según el contexto son:

* [Componente de visor PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Compatibilidad con AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
