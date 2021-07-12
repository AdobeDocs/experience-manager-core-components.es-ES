---
title: Módulo it.testing de AEM tipo de archivo del proyecto
description: Cómo utilizar las pruebas de integración de tipo de archivo del proyecto AEM
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Architect, Developer, Admin
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '80'
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
