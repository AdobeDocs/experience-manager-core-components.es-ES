---
title: Módulo ui.apps del arquetipo del proyecto AEM
seo-title: Módulo ui.apps del arquetipo del proyecto AEM
description: Módulo ui.apps del arquetipo del proyecto AEM
seo-description: Módulo ui.apps del arquetipo del proyecto AEM
contentOwner: bohnert
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Módulo ui.apps del arquetipo del proyecto AEM {#uiapps-module}

El módulo muven ui.apps (`<src-directory>/<project>/ui.apps`) incluye todo el código de procesamiento necesario para el sitio debajo `/apps`. Esto incluye CSS/JS que se almacenarán en un formato AEM denominado clientlibs. Esto también incluye secuencias de comandos HTML para procesar HTML dinámico. Puede pensar en el módulo ui.apps como un mapa de la estructura del JCR, pero en un formato que se puede almacenar en un sistema de archivos y transferir al control de código fuente.

El complemento Apache Jackrabbit FileVault Package se utiliza para compilar el contenido del módulo ui.apps en un paquete AEM que se puede implementar en AEM. Las configuraciones globales del complemento se definen en el archivo pom.xml principal.

## POM principal {#parent-pom}

[El POM](overview.md#parent-pom) principal (`<src>/<project>/pom.xml`) incluye `<plugin>` secciones que definen distintas configuraciones para los complementos utilizados en el proyecto. Esto incluye una configuración para el `filterSource` complemento de paquete Jackrabbit FileVault. El `filterSource` apunta a la ubicación del `filter.xml` archivo que se utiliza para definir las rutas jcr incluidas en el paquete.

Además del complemento de paquete Jackrabbit FileVault es una definición del complemento de paquete de contenido que se utiliza para insertar el paquete en AEM. Tenga en cuenta que se utilizan variables para `aem.host`, `aem.port`, `vault.user`y `vault.password` que corresponden a las propiedades globales definidas en el mismo POM principal.

## ui.apps/pom.xml {#uiapps-pom}

La pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) proporciona las `embedded` etiquetas de la `filevault-package-maven-plugin`. Las `embedded` etiquetas incluyen el paquete principal compilado como parte del paquete ui.apps y dónde se instalará.

Observe que los paquetes core.wcm.components.all y core.wcm.components.samples se incluyen como un subpaquete. Esto implementará el paquete de componentes principales junto con el código WKND cada vez.

Los archivos core.wcm.components.all y core.wcm.components.samples se incluyen como dependencias en la lista de dependencias. Sin embargo, como práctica recomendada, las versiones para dependencias se omiten aquí y se administran en el archivo [pom](overview.md#core-components)principal.

## filter.xml {#filter}

El `filter.xml` archivo del módulo ui.apps se encuentra en `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` y contiene las rutas que se incluirán e instalarán con el paquete ui.apps.
