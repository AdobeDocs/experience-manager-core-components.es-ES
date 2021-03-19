---
product: adobe experience manager
solution: Experience Manager Sites
type: Documentación
description: Documentación de los componentes principales de Adobe Experience Manager
git-repo: https://git.corp.adobe.com/AdobeDocs/experience-manager-core-components.es-ES
index: y
translation-type: tm+mt
source-git-commit: 290423c39b925ea8cf4077f31a76ecf01167f344
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 6%

---


# Metadatos para uso interno

Los metadatos en el sistema de creación de GitHub son jerárquicos y se definen con los siguientes niveles crecientes de precedentes.

1. metadata.md
1. ToC
1. Artículo

Los metadatos definidos en el archivo metadata.md se aplican a todo el repositorio, pero se pueden sobrescribir en los niveles de ToC y de artículo. Cualquier anulación de los metadatos debe realizarse en el nivel más bajo posible.

Los metadatos del repositorio experience-manager-core-components.en son los mínimos requeridos.

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
