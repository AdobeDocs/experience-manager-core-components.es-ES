---
title: Módulo ui.testing de AEM arquetipo del proyecto
description: Cómo usar las pruebas JUnit de arquetipo del proyecto AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# ui.testing Módulo del arquetipo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

## Pruebas de unidad {#unit-tests}

La prueba unitaria del [módulo principal](core.md) muestra las pruebas unitarias clásicas del código contenido en el paquete. Para realizar la prueba, ejecute:

```
mvn clean test
```

## Pruebas de integración {#integration-tests}

Las pruebas de integración del lado del servidor permiten ejecutar pruebas de tipo unidad en el entorno de AEM, es decir, en el servidor AEM. Para realizar la prueba, ejecute:

```
mvn clean verify -PintegrationTests
```

## Pruebas del lado del cliente {#client-side-tests}

Las pruebas `client-side Hobbes.js` son pruebas del lado del explorador basadas en JavaScript que verifican el comportamiento del lado del explorador.

Para realizar la prueba, cuando visualice una página AEM que desee probar en el explorador, abra la página en **modo de desarrollador** abriendo el panel izquierdo, cambie a la ficha **Pruebas** y busque las **Pruebas de MyName** generadas y ejecútelas.
