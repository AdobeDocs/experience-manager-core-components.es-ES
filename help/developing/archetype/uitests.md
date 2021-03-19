---
title: ui.testing Módulo de AEM tipo de archivo del proyecto
description: Cómo usar las pruebas de interfaz de usuario del tipo de archivo del proyecto AEM
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Arquitecto, Desarrollador, Administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# ui.testing Módulo del tipo de archivo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas de unidad](core.md#unit-tests)
* [Pruebas de integración](ittests.md)
* Pruebas de la interfaz de usuario

Este artículo describe las pruebas de IU disponibles como parte del módulo ui.testing .

## Ejecución de pruebas de IU {#running-tests}

Para probar, ejecute:

```shell
mvn verify -Pui-tests-local-execution
```

Después de la ejecución, los informes y los registros están disponibles en la carpeta `target/reports` .

## Opciones adicionales {#additional-options}

Las pruebas de IU se pueden ejecutar con muchas opciones diferentes, incluidas las pruebas sin objetivos con un navegador local y como imagen Docker. Consulte el archivo [README.md del módulo ui.testing](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obtener más información.
