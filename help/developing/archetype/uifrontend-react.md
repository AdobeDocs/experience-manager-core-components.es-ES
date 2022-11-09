---
title: Compilación front-end para React SPA
description: Descripción del proceso de compilación del front-end para proyectos de SPA basados en React
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: dd8ef13a-9686-47a9-b6af-e486ff10c4d8
source-git-commit: 0eea0cd65063c739e5b405b0380b73962a858e48
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 99%

---

# Compilación front-end para React SPA {#frontend-react}

Este documento explica los detalles del proyecto creado al utilizar el tipo de archivo para crear una aplicación de una sola página (SPA) basada en el marco de React. Es decir, cuando se establece la opción `frontendModule` en `react`.

## Información general {#overview}

Este proyecto se arrancó con [create-react-app](https://github.com/facebook/create-react-app).

Esta aplicación está diseñada para consumir el modelo AEM de un sitio. Generará automáticamente el diseño utilizando los componentes de ayuda del paquete [@adobe/cq-react-editable-components](https://www.npmjs.com/package/@adobe/aem-react-editable-components).

## Scripts {#scripts}

En el directorio del proyecto, puede ejecutar los siguientes comandos:

### npm start {#npm-start}

```shell
npm start
```

Este comando ejecuta la aplicación en modo de desarrollo mediante el proxy del modelo JSON desde una instancia de AEM local que se ejecuta en http://localhost:4502. Esto supone que todo el proyecto se ha implementado para AEM al menos una vez (`mvn clean install -PautoInstallPackage` en la raíz del proyecto).

Después de ejecutar `npm start` en el directorio [ui.frontend](uifrontend.md), la aplicación se abrirá automáticamente en el explorador (en la ruta `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Si realiza ediciones, la página se volverá a cargar.

Si está obteniendo errores relacionados con CORS, es posible que desee configurar AEM de la siguiente manera:

1. Vaya al Administrador de configuración (http://localhost:4502/system/console/configMgr)
1. Abra la configuración de “Política de uso compartido de recursos de origen cruzado de Adobe Granite”
1. Cree una nueva configuración con los siguientes valores adicionales:
   * Orígenes permitidos: http://localhost:3000
   * Encabezados admitidos: Autorización
   * Métodos permitidos: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Este comando inicia el ejecutor de prueba en el modo de reloj interactivo. Consulte la [documentación de React sobre la ejecución de pruebas](https://facebook.github.io/create-react-app/docs/running-tests) para obtener más información.

### npm run build {#npm-run-build}

```shell
npm run build
```

Este comando crea la aplicación para producción en la carpeta de compilación. Agrupa React en modo de producción y optimiza la compilación para obtener el mejor rendimiento. Consulte la [documentación de React sobre la implementación](https://facebook.github.io/create-react-app/docs/deployment) para obtener más información.

Además, se genera un AEM ClientLib desde la aplicación utilizando el paquete [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Compatibilidad con navegadores {#browser-support}

De forma predeterminada, este proyecto utiliza la opción predeterminada [Browserslist](https://github.com/browserslist/browserslist) para identificar los navegadores de destino. Además, incluye polirellenos para las funciones de lenguaje moderno que admiten navegadores más antiguos (por ejemplo, Internet Explorer 11). Si la compatibilidad con estos exploradores no es un requisito, se pueden eliminar las dependencias y las importaciones de polyfill.

## División de código {#code-splitting}

La aplicación React está configurada para utilizar [división de código](https://webpack.js.org/guides/code-splitting) de forma predeterminada. Al crear la aplicación para producción, el código se muestra en varios fragmentos:

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Cargar fragmentos solo cuando son necesarios puede mejorar significativamente el rendimiento de la aplicación.

Para que esta función funcione con AEM, la aplicación debe poder identificar qué archivos JS y CSS se deben solicitar al HTML generado por AEM. Esto se puede lograr utilizando la clave “entrypoints” en el archivo asset-manifest.json. El archivo se analiza en clientlib.config.js y solo los archivos de punto de entrada se incluyen en ClientLib. Los archivos restantes se colocan en el directorio de recursos de ClientLib y se solicitan de forma dinámica y, por lo tanto, solo se cargan cuando realmente son necesarios.

Consulte la [documentación general del módulo ui.frontend](uifrontend.md#clientlibs) para obtener más información sobre cómo el tipo de archivo del proyecto de AEM utiliza AEM ClientLibs.
