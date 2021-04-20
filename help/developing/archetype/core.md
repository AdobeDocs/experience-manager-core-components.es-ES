---
title: Módulo principal del tipo de archivo del proyecto AEM
description: Módulo principal del tipo de archivo del proyecto AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# Módulo principal del tipo de archivo del proyecto AEM {#core-module}

El módulo principal de maven (`<src-directory>/<project>/core`) incluye todo el código Java necesario para la implementación. El módulo empaquetará todo el código Java e implementará en la instancia de AEM como un paquete OSGi.

El complemento Maven Bundle definido en `<src-directory>/<project>/core/pom.xml` es responsable de compilar el código Java en un paquete OSGi que puede ser reconocido por AEM contenedor OSGi. Tenga en cuenta que aquí es donde se define la ubicación de los modelos Sling.

Aunque es raro que el paquete principal deba implementarse independientemente del módulo ui.apps en entornos de nivel superior, la implementación del paquete principal directamente resulta útil durante el desarrollo/prueba local. El complemento Maven Sling permite implementar el paquete principal para AEM directamente aprovechando el perfil `autoInstallBundle` tal como se define en el [POM principal](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Una vez ejecutado correctamente, debería poder ver la Consola de paquetes en `http://<host>:<port>/system/console/bundles`.

##  Pruebas de unidad {#unit-tests}

La prueba de unidad en el módulo principal muestra la prueba de unidad clásica del código contenido en el paquete. Para probar, ejecute:

```shell
mvn clean test
```
