---
title: Módulo principal del arquetipo del proyecto AEM
description: Módulo principal del arquetipo del proyecto AEM
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# Módulo principal del arquetipo del proyecto AEM {#core-module}

El módulo principal de procesamiento (`<src-directory>/<project>/core`) incluye todo el código Java necesario para la implementación. El módulo empaquetará todo el código Java e implementará en la instancia de AEM como un paquete OSGi.

El complemento Maven Bundle definido en `<src-directory>/<project>/core/pom.xml` es responsable de compilar el código Java en un paquete OSGi que puede ser reconocido por AEM contenedor OSGi. Tenga en cuenta que aquí es donde se define la ubicación de los modelos Sling.

Aunque es raro que el paquete principal deba implementarse independientemente del módulo ui.apps en los entornos de nivel superior, la implementación del paquete principal directamente resulta útil durante el desarrollo y la prueba locales. El complemento Maven Sling permite implementar el paquete principal para AEM directamente aprovechando el perfil `autoInstallBundle` tal como se define en el [POM principal](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Una vez ejecutada correctamente, debería poder ver la consola de paquetes en `http://<host>:<port>/system/console/bundles`.

##  Pruebas de unidad {#unit-tests}

La prueba unitaria del módulo principal muestra las pruebas unitarias clásicas del código contenido en el paquete. Para realizar la prueba, ejecute:

```shell
mvn clean test
```
