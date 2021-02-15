---
product: Adobe Experience Manager
description: Documentación para los componentes principales de Adobe Experience Manager
git-repo: https://git.corp.adobe.com/AdobeDocs/experience-manager-core-components.es-ES
index: y
solution-title: Información y asistencia para AEM
solution-hub-url: https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/sites/home.html
getting-started-title: Introducción al desarrollo para AEM
getting-started-url: https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/core-concepts/home.html
tutorials-title: Tutoriales de AEM
tutorials-url: https://docs.adobe.com/content/help/es-ES/experience-manager-learn/cloud-service/overview.html
translation-type: tm+mt
source-git-commit: f109463f1942349c300600acf6b94f268e8aa60e
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 19%

---


# Metadatos para uso interno

Los metadatos en el sistema de creación de GitHub son jerárquicos y se definen con los siguientes niveles crecientes de precedentes.

1. metadata.md
1. ToC
1. Artículo

Los metadatos definidos en el archivo metadata.md se aplican a toda la repo, pero se pueden anular en los niveles de ToC y de artículo. Cualquier anulación de los metadatos debe realizarse en el nivel más bajo posible.

Los metadatos de la repo experience-manager-core-components.en son los mínimos requeridos.

metadata.md

* `product`
* `git-repo`
* `index: y`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

Artículo

* `title`
* `description`
* `index: n` (solo para versiones anteriores de componentes)

Encontrará información adicional sobre los metadatos en la [guía de creación interna.](https://docs.adobe.com/help/en/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
