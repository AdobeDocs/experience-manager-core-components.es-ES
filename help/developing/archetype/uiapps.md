---
title: Módulo ui.apps del tipo de archivo del proyecto AEM
description: Módulo ui.apps del tipo de archivo del proyecto AEM
feature: Componentes principales, tipo de archivo del proyecto AEM
role: Architect, Developer, Admin
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# Módulo ui.apps del tipo de archivo del proyecto AEM {#uiapps-module}

El módulo ui.apps de maven (`<src-directory>/<project>/ui.apps`) incluye todo el código de renderización necesario para el sitio debajo de `/apps`. Esto incluye CSS/JS que se almacenarán en un formato AEM llamado [clientlibs.](uifrontend.md#clientlibs) Esto también incluye scripts de HTL para procesar HTML dinámico. El módulo ui.apps es similar a un mapa de la estructura en el JCR pero en un formato que se puede almacenar en un sistema de archivos y comprometerse con el control de código fuente.

El complemento Apache Jackrabbit FileVault Package se utiliza para compilar el contenido del módulo ui.apps en un paquete AEM que se puede implementar en AEM. Las configuraciones globales para el complemento se definen en el pom.xml principal.

## POM principal {#parent-pom}

[El POM principal](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) incluye secciones de `<plugin>` que definen varias configuraciones para los complementos utilizados en el proyecto. Esto incluye una configuración para el `filterSource` para el complemento Jackrabbit FileVault Package. El `filterSource` indica a la ubicación del archivo `filter.xml` que se utiliza para definir las rutas jcr que se incluyen en el paquete.

Además del complemento Jackrabbit FileVault Package, se encuentra una definición del complemento Paquete de contenido que se utiliza para insertar el paquete en AEM. Tenga en cuenta que se utilizan variables para `aem.host`, `aem.port`, `vault.user` y `vault.password` que corresponden a las propiedades globales definidas en el mismo POM principal.

## ui.apps/pom.xml {#uiapps-pom}

El pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) proporciona las etiquetas `embedded` para `filevault-package-maven-plugin`. Las etiquetas `embedded` incluyen el paquete principal compilado como parte del paquete ui.apps y dónde se instalará.

Verá que los paquetes core.wcm.components.all y core.wcm.components.example se incluyen como subpaquete. Esto implementará el paquete de componentes principales junto con el código de WKND cada vez.

Los ejemplos core.wcm.components.all y core.wcm.components.components se incluyen como dependencias en la lista de dependencias. Sin embargo, como práctica recomendada, las versiones para dependencias se omiten aquí y se administran en el [archivo pom principal](/help/developing/archetype/using.md#core-components).

## filter.xml {#filter}

El archivo `filter.xml` para el módulo ui.apps se encuentra en `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` y contiene las rutas que se incluirán e instalarán con el paquete ui.apps.
