---
title: Compilación front-end para SPA de Angular
description: Descripción del proceso de compilación del front-end para proyectos de SPA basados en Angular
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Arquitecto, Desarrollador, Administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# Compilación front-end para SPA de Angular {#frontend-angular}

En este documento se explican los detalles del proyecto creado al utilizar el tipo de archivo para crear una aplicación de una sola página (SPA) basada en el marco de Angular. Es decir, cuando se establece la opción `frontendModule` en `angular`.

## Información general {#overview}

Este proyecto se arrancó con el [Angular CLI](https://github.com/angular/angular-cli).

Esta aplicación está diseñada para consumir el modelo AEM de un sitio. Generará automáticamente el diseño utilizando los componentes de ayuda del paquete [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) .

## Secuencias de comandos {#scripts}

En el directorio del proyecto, puede ejecutar los siguientes comandos.

### inicio de npm {#npm-start}

```
npm start
```

Este comando ejecuta la aplicación en modo de desarrollo mediante el proxy del modelo JSON desde una instancia de AEM local que se ejecuta en http://localhost:4502. Esto supone que todo el proyecto se ha implementado para AEM al menos una vez (`mvn clean install -PautoInstallPackage` en la raíz del proyecto).

Después de ejecutar npm start en el directorio ui.frontend , la aplicación se abrirá automáticamente en el explorador (en la ruta http://localhost:4200/content/${appId}/${country}/${language}/home.html). Si realiza ediciones, la página se volverá a cargar.

Si está obteniendo errores relacionados con CORS, es posible que desee configurar AEM de la siguiente manera:

1. Vaya al Administrador de configuración (http://localhost:4502/system/console/configMgr)
1. Abra la configuración de &quot;Política de uso compartido de recursos de origen cruzado de Adobe Granite&quot;
1. Cree una nueva configuración con los siguientes valores adicionales:
   * Orígenes permitidos: http://localhost:4200
   * Encabezados admitidos: Autorización
   * Métodos permitidos: OPTIONS

### prueba npm {#npm-test}

```shell
npm test
```

Este comando inicia el corredor de prueba Karma. Para obtener más información, consulte la [documentación del Angular sobre la ejecución de pruebas](https://angular.io/guide/testing).

### prueba de ejecución de npm:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Este comando inicia el ejecutor de pruebas de Karma en modo de reloj interactivo.

### compilación npm run {#npm-run-build}

```shell
npm run build
```

Este comando crea la aplicación para producción en la carpeta de compilación. Agrupa el Angular en modo de producción y optimiza la compilación para obtener el mejor rendimiento. Consulte la [documentación del Angular sobre la implementación](https://angular.io/guide/deployment) para obtener más información.

Además, se genera un AEM ClientLib desde la aplicación utilizando el paquete [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

Consulte la [documentación general del módulo ui.frontend](uifrontend.md#clientlibs) para obtener más información sobre cómo AEM el tipo de archivo del proyecto utiliza las bibliotecas de cliente.

## Compatibilidad con exploradores {#browser-support}

De forma predeterminada, este proyecto utiliza la opción predeterminada [Browserslist](https://github.com/browserslist/browserslist) para identificar los navegadores de destino. Además, incluye polirellenos para las funciones de lenguaje moderno que admiten navegadores más antiguos (por ejemplo, Internet Explorer 11). Si la compatibilidad con estos exploradores no es un requisito, se pueden eliminar las dependencias y las importaciones de polyfill.
