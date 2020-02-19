---
title: Módulo ui.content del arquetipo del proyecto de AEM
description: Módulo ui.content del arquetipo del proyecto de AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Módulo ui.content del arquetipo del proyecto de AEM {#uicontent-module}

El módulo ui.content maven (`<src-directory>/<project>/ui.content`) incluye contenido de línea de base y configuraciones debajo `/content` y `/conf`. ui.content se compila en un paquete de AEM como ui.apps. La principal diferencia es que los nodos almacenados en ui.content se pueden modificar directamente en la instancia de AEM. Esto incluye páginas, recursos DAM y plantillas editables. El módulo ui.content puede utilizarse para almacenar contenido de muestra para una instancia limpia o para crear algunas configuraciones de línea de base que se administrarán en el control de código fuente.

## filter.xml {#filter}

El `filter.xml` archivo para el módulo ui.content se encuentra en `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` y contiene las rutas que se incluirán e instalarán con el paquete ui.content. Observe que se agrega un `mode="merge"` atributo a la ruta. Esto garantiza que las configuraciones implementadas con una implementación de código no anulen automáticamente el contenido o las configuraciones que se hayan creado directamente en la instancia de AEM.

## ui.content/pom.xml

El módulo ui.content, al igual que el módulo ui.apps, utiliza el complemento FileVault Package. Sin embargo, el pom ui.content (`<src>/<project>/ui.content/pom.xml`) incluye una propiedad de configuración adicional llamada `acHandling`, establecida en `merge_preserve`. Esto se incluye porque el módulo ui.content incluye listas de control de acceso (ACL), que son permisos que determinan quién puede editar las plantillas. Para que estas ACL se importen a AEM, se necesita la `acHandling` propiedad.
