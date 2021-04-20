---
title: Módulo ui.content del tipo de archivo del proyecto AEM
description: Módulo ui.content del tipo de archivo del proyecto AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# ui.content Módulo del tipo de archivo del proyecto AEM {#uicontent-module}

El módulo ui.content maven (`<src-directory>/<project>/ui.content`) incluye contenido de línea de base y configuraciones debajo de `/content` y `/conf`. ui.content se compila en un paquete AEM como ui.apps. La diferencia principal es que los nodos almacenados en ui.content se pueden modificar directamente en la instancia de AEM. Esto incluye páginas, recursos DAM y plantillas editables. El módulo ui.content se puede utilizar para almacenar contenido de muestra para una instancia limpia o para crear algunas configuraciones de línea de base que se van a administrar en el control de código fuente.

## filter.xml {#filter}

El archivo `filter.xml` para el módulo ui.content se encuentra en `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` y contiene las rutas que se incluirán e instalarán con el paquete ui.content. Observe que se agrega un atributo `mode="merge"` a la ruta. Esto garantiza que las configuraciones implementadas con una implementación de código no anulen automáticamente el contenido o las configuraciones que se hayan creado directamente en la instancia de AEM.

## ui.content/pom.xml

El módulo ui.content, como el módulo ui.apps, utiliza el complemento Paquete FileVault. Sin embargo, el pom ui.content (`<src>/<project>/ui.content/pom.xml`) incluye una propiedad de configuración adicional llamada `acHandling`, establecida en `merge_preserve`. Esto se incluye porque el módulo ui.content incluye Listas de control de acceso (ACL) que son permisos que determinan quién puede editar las plantillas. Para que estas ACL se importen en AEM se necesita la propiedad `acHandling` .
