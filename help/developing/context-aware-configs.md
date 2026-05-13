---
title: Configuraciones según el contexto y componentes principales de Sling
description: Los componentes principales aprovechan las configuraciones según el contexto de Sling para determinadas funciones
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
TQID: https://experienceleague.adobe.com/jCBeHjuqLJzIxggeZxpusUkv9ZAyE-Ktr5N-gakWK18
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 257
ht-degree: 100%

---

# Configuraciones según el contexto y componentes principales de Sling {#sling-context-aware-configurations}

Las configuraciones según el contexto son una [función de Sling](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Son configuraciones que están relacionadas con un recurso de contenido o un árbol de recursos y que los componentes principales aprovechan para permitir configuraciones en todo el sitio.

## Configuraciones según el contexto de Sling {#context-aware-configurations}

El sitio puede necesitar diferentes configuraciones para diferentes regiones del sitio, por ejemplo, donde algunos parámetros pueden compartirse y requieren herencia para contextos anidados y valores de reserva globales. AEM aprovecha las configuraciones según el contexto de Sling, que permiten esta posibilidad.

Para obtener más información sobre las configuraciones en AEM, consulte la [documentación de configuraciones y el explorador de configuración.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html?lang=es)

## Uso en los componentes principales {#core-components}

Varias funciones de componentes principales aprovechan las configuraciones según el contexto. Todas estas configuraciones se encuentran en el siguiente nodo:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Las configuraciones individuales dependen del componente o la función específicos. Las funciones de los componentes principales que utilizan configuraciones según el contexto incluyen:

* [El componente Página](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) se basa en la configuración según el contexto al procesar etiquetas `link`, `script` y `meta`.
* [Componente Visualizador de PDF](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [Compatibilidad con AMP](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
