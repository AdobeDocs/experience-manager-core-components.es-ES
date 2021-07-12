---
title: ui.testing Módulo de AEM tipo de archivo del proyecto
description: Cómo usar las pruebas de interfaz de usuario del tipo de archivo del proyecto AEM
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Módulo ui.testing del tipo de archivo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

* [Pruebas de unidad](core.md#unit-tests)
* [Pruebas de integración](ittests.md)
* Pruebas de la interfaz de usuario

Este artículo describe las pruebas de IU disponibles como parte del módulo ui.testing .

## Ejecución de pruebas de interfaz de usuario {#running-tests}

Para probar, ejecute:

```shell
mvn verify -Pui-tests-local-execution
```

Después de la ejecución, los informes y los registros están disponibles en la carpeta `target/reports` .

## Opciones adicionales {#additional-options}

Las pruebas de IU se pueden ejecutar con muchas opciones diferentes, incluidas las pruebas sin objetivos con un navegador local y como imagen Docker. Consulte el archivo [README.md del módulo ui.testing](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) para obtener más información.
