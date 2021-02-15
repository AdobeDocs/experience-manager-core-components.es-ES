---
title: Módulo ui.testing de AEM arquetipo del proyecto
description: Cómo utilizar las pruebas de IU de arquetipo de proyecto AEM
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# ui.testing Módulo del arquetipo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas unitarias](core.md#unit-tests)
* [Pruebas de integración](ittests.md)
* Pruebas de la interfaz de usuario

En este artículo se describen las pruebas de interfaz de usuario disponibles como parte del módulo ui.testing.

## Ejecutando pruebas de IU {#running-tests}

Para realizar la prueba, ejecute:

```shell
mvn verify -Pui-tests-local-execution
```

Después de la ejecución, los informes y registros están disponibles en la carpeta `target/reports`.

## Opciones adicionales {#additional-options}

Las pruebas de interfaz de usuario se pueden ejecutar con muchas opciones diferentes, incluso para realizar pruebas sin encabezado con un navegador local y como imagen de Docker. Consulte el archivo [README.md del módulo ui.testing](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obtener más información.
