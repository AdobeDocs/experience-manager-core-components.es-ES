---
title: Módulo principal del arquetipo del proyecto de AEM
seo-title: Módulo principal del arquetipo del proyecto de AEM
description: Módulo principal del arquetipo del proyecto de AEM
seo-description: Módulo principal del arquetipo del proyecto de AEM
contentOwner: bohnert
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# Módulo principal del arquetipo del proyecto de AEM {#core-module}

El módulo maestro principal (`<src-directory>/<project>/core`) incluye todo el código Java necesario para la implementación. El módulo empaquetará todo el código Java e implementará en la instancia de AEM como un paquete OSGi.

El complemento Maven Bundle definido en la `<src-directory>/<project>/core/pom.xml` es responsable de compilar el código Java en un paquete OSGi que puede ser reconocido por el contenedor OSGi de AEM. Tenga en cuenta que aquí es donde se define la ubicación de los modelos Sling.

Aunque es raro que el paquete principal deba implementarse independientemente del módulo ui.apps en entornos de nivel superior, la implementación del paquete principal directamente resulta útil durante las pruebas y el desarrollo locales. El complemento Maven Sling permite implementar el paquete principal en AEM directamente aprovechando el `autoInstallBundle` perfil tal como se define en el POM [](overview.md#parent-pom)principal.

```
mvn -PautoInstallBundle clean install
```

Una vez ejecutada correctamente, debería poder ver la Consola de Bundels en `http://<host>:<port>/system/console/bundles`.
