---
title: Módulo ui.content del tipo de archivo del proyecto AEM
description: Módulo ui.content del tipo de archivo del proyecto AEM
feature: Componentes principales, tipo de archivo del proyecto AEM
role: Architect, Developer, Admin
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '223'
ht-degree: 100%

---

# Módulo ui.content del tipo de archivo del proyecto AEM {#uicontent-module}

El módulo ui.content de Maven (`<src-directory>/<project>/ui.content`) incluye contenido de línea de base y configuraciones en `/content` y `/conf`. ui.content se compila en un paquete AEM como ui.apps. La diferencia principal es que los nodos almacenados en ui.content se pueden modificar directamente en la instancia de AEM. Esto incluye páginas, recursos DAM y plantillas editables. El módulo ui.content se puede utilizar para almacenar contenido de muestra para una instancia limpia o para crear algunas configuraciones de línea de base que se van a administrar en el control de código fuente.

## filter.xml {#filter}

El archivo `filter.xml` para el módulo ui.content se encuentra en `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` y contiene las rutas que se incluirán e instalarán con el paquete ui.content. Verá que se agrega un atributo `mode="merge"` a la ruta. Esto garantiza que las configuraciones implementadas con una implementación de código no anulen automáticamente el contenido ni las configuraciones que se hayan creado directamente en la instancia de AEM.

## ui.content/pom.xml

El módulo ui.content, como el módulo ui.apps, utiliza el complemento FileVault Package. Sin embargo, el pom ui.content (`<src>/<project>/ui.content/pom.xml`) incluye una propiedad de configuración adicional llamada `acHandling`, establecida en `merge_preserve`. Esto se incluye porque el módulo ui.content incluye Listas de control de acceso (ACL) que son permisos que determinan quién puede editar las plantillas. Para que estas ACL se importen en AEM se necesita la propiedad `acHandling`.
