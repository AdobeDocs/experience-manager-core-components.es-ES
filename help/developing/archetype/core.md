---
title: Módulo principal del arquetipo del proyecto AEM
description: Módulo principal del arquetipo del proyecto AEM
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# Módulo principal del arquetipo del proyecto AEM {#core-module}

El módulo principal de procesamiento (`<src-directory>/<project>/core`) incluye todo el código Java necesario para la implementación. El módulo empaquetará todo el código Java e implementará en la instancia de AEM como un paquete OSGi.

El complemento Maven Bundle definido en `<src-directory>/<project>/core/pom.xml` es responsable de compilar el código Java en un paquete OSGi que puede ser reconocido por AEM contenedor OSGi. Tenga en cuenta que aquí es donde se define la ubicación de los modelos Sling.

Aunque es raro que el paquete principal deba implementarse independientemente del módulo ui.apps en los entornos de nivel superior, la implementación del paquete principal directamente resulta útil durante el desarrollo y la prueba locales. El complemento Maven Sling permite implementar el paquete principal para AEM directamente aprovechando el perfil `autoInstallBundle` tal como se define en el [POM principal](/help/developing/archetype/using.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

Una vez ejecutada correctamente, debería poder ver la consola de paquetes en `http://<host>:<port>/system/console/bundles`.
