---
title: Módulo de ui.tests del tipo de archivo del proyecto AEM
description: Utilización de las pruebas de IU de tipo de archivo del proyecto AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '112'
ht-degree: 100%

---

# Módulo ui.tests del tipo de archivo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas de unidad](core.md#unit-tests)
* [Pruebas de integración](ittests.md)
* Pruebas de la interfaz de usuario

Este artículo describe las pruebas de IU disponibles como parte del módulo ui.tests.

## Ejecución de pruebas de interfaz de usuario {#running-tests}

Para iniciar la prueba, ejecute:

```shell
mvn verify -Pui-tests-local-execution
```

Después de la ejecución, los informes y los registros están disponibles en la carpeta `target/reports`.

## Opciones adicionales {#additional-options}

Las pruebas de IU se pueden ejecutar con muchas opciones diferentes, incluidas las pruebas sin objetivos con un navegador local y como imagen Docker. Consulte el archivo [README.md del módulo ui.tests](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obtener más información.
