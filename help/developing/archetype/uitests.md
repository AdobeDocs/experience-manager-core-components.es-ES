---
title: ui.testing Módulo del arquetipo del proyecto de AEM
description: Cómo utilizar las pruebas JUnit de arquetipo de proyecto de AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Módulo ui.testing del arquetipo del proyecto AEM {#uitests-module}

El proyecto contiene tres niveles de prueba:

## Pruebas unitarias {#unit-tests}

La prueba unitaria del módulo [](core.md) principal muestra la prueba unitaria clásica del código contenido en el paquete. Para realizar la prueba, ejecute:

```
mvn clean test
```

## Pruebas de integración {#integration-tests}

Las pruebas de integración del lado del servidor permiten ejecutar pruebas de tipo unidad en el entorno AEM, es decir, en el servidor AEM. Para realizar la prueba, ejecute:

```
mvn clean verify -PintegrationTests
```

## Pruebas del lado del cliente {#client-side-tests}

Las `client-side Hobbes.js` pruebas son pruebas basadas en JavaScript en el navegador que verifican el comportamiento en el navegador.

Para realizar la prueba, cuando visualice una página de AEM que desee probar en el navegador, abra la página en el modo **** Desarrollador abriendo el panel izquierdo y cambie a la ficha **Pruebas** , busque las pruebas **** MyName generadas y ejecútelas.
