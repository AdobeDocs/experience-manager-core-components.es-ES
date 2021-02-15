---
title: Módulo it.testing de AEM arquetipo de proyecto
description: Cómo utilizar las pruebas de integración de arquetipos del proyecto AEM
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# Módulo it.testing del arquetipo de proyecto AEM {#ittests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas unitarias](core.md#unit-tests)
* Pruebas de integración
* [Pruebas de la interfaz de usuario](uitests.md)

Este artículo describe las pruebas de integración disponibles como parte del módulo it.testing.

## Ejecución de pruebas de integración {#running-tests}

Las pruebas de integración del lado del servidor permiten ejecutar pruebas de tipo unidad en el entorno de AEM, es decir, en el servidor AEM. Para realizar la prueba, ejecute:

```
mvn clean verify -PintegrationTests
```
