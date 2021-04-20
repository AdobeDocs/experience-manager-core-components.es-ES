---
title: Módulo it.testing de AEM tipo de archivo del proyecto
description: Cómo utilizar las pruebas de integración de tipo de archivo del proyecto AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Módulo it.testing del tipo de archivo del proyecto AEM {#ittests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas de unidad](core.md#unit-tests)
* Pruebas de integración
* [Pruebas de la interfaz de usuario](uitests.md)

Este artículo describe las pruebas de integración disponibles como parte del módulo it.testing .

## Ejecución de pruebas de integración {#running-tests}

Las pruebas de integración del lado del servidor permiten que las pruebas de tipo unidad se ejecuten en el entorno de AEM, es decir, en el servidor de AEM. Para probar, ejecute:

```
mvn clean verify -PintegrationTests
```
