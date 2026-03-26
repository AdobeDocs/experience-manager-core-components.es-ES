---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
landing-page-name: experience-manager
landing-page-breadcrumb-title: AEM
type: Documentation
description: Documentación de los componentes principales de Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.es-ES
index: true
recommendations: noDisplay
source-git-commit: 1975e060e8db5526518dcf6fc722e3623c47dda6
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Metadatos para uso interno

Los metadatos del sistema de creación de GitHub son jerárquicos y se definen con los siguientes niveles crecientes de precedentes.

1. metadata.md
1. ToC
1. Artículo

Los metadatos definidos en el archivo metadata.md se aplican a todo el repositorio, pero se pueden sobrescribir en los niveles de TDC y de artículo. Cualquier anulación de los metadatos debe realizarse en el nivel más bajo posible.

Los metadatos del repositorio experience-manager-core-components.en son los mínimos requeridos.

metadata.md

* `product`
* `git-repo`
* `index: true`
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
* `index: false` (solo para versiones anteriores de componentes)

Encontrará información adicional sobre los metadatos en la [guía de creación interna.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
