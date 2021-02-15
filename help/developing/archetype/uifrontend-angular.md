---
title: Compilación front-end para SPA angulares
description: Una descripción del proceso de construcción del front-end para proyectos de SPA basados en Angular
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Compilación front-end para SPA angulares {#frontend-angular}

Este documento explica los detalles del proyecto creado al utilizar el arquetipo para crear una aplicación de una sola página (SPA) basada en el marco Angular. Es decir, cuando establece la opción `frontendModule` en `angular`.

## Información general {#overview}

Este proyecto se inició con la [CLI angular](https://github.com/angular/angular-cli).

Esta aplicación está diseñada para consumir el modelo AEM de un sitio. Generará automáticamente el diseño utilizando los componentes auxiliares del paquete [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components).

## Secuencias de comandos {#scripts}

En el directorio del proyecto, puede ejecutar los siguientes comandos.

### inicio npm {#npm-start}

```
npm start
```

Este comando ejecuta la aplicación en modo de desarrollo mediante el proxy del modelo JSON desde una instancia de AEM local que se ejecuta en http://localhost:4502. Esto supone que todo el proyecto se ha implementado para AEM al menos una vez (`mvn clean install -PautoInstallPackage` en la raíz del proyecto).

Después de ejecutar el inicio npm en el directorio ui.front, la aplicación se abrirá automáticamente en el explorador (en la ruta http://localhost:4200/content/${appId}/${country}/${language}/home.html). Si realiza modificaciones, la página se volverá a cargar.

Si está obteniendo errores relacionados con CORS, puede que desee configurar AEM de la siguiente manera:

1. Vaya a Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra la configuración de la &quot;Política de uso compartido de recursos entre Orígenes de Adobe Granite&quot;
1. Cree una nueva configuración con los siguientes valores adicionales:
   * Orígenes permitidos: http://localhost:4200
   * Encabezados admitidos: Autorización
   * Métodos permitidos: OPTIONS

### prueba npm {#npm-test}

```shell
npm test
```

Este comando inicia el ejecutor de pruebas Karma. Consulte la [documentación angular sobre la ejecución de pruebas](https://angular.io/guide/testing) para obtener más información.

### prueba de ejecución npm:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Este comando inicia el ejecutor de pruebas Karma en modo de reloj interactivo.

### npm run build {#npm-run-build}

```shell
npm run build
```

Este comando crea la aplicación para producción en la carpeta de compilación. Agrupa Angular en modo de producción y optimiza la compilación para obtener el mejor rendimiento. Consulte la [documentación angular sobre la implementación](https://angular.io/guide/deployment) para obtener más información.

Además, se genera un AEM ClientLib desde la aplicación mediante el paquete [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

Consulte la [documentación general del módulo ui.frontender](uifrontend.md#clientlibs) para obtener más información sobre cómo AEM ClientLibs se utilizan en el arquetipo del proyecto.

## Compatibilidad con exploradores {#browser-support}

De forma predeterminada, este proyecto utiliza la opción predeterminada de [Browserslist](https://github.com/browserslist/browserslist) para identificar los exploradores de destinatario. Además, incluye polirellenos para las características de idioma moderno que admiten exploradores más antiguos (por ejemplo, Internet Explorer 11). Si la compatibilidad con estos exploradores no es un requisito, se pueden eliminar las importaciones y dependencias de relleno múltiple.
