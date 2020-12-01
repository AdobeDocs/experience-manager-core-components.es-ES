---
title: Diseño front-end para la SPA de reacción
description: Una descripción del proceso de generación de front-end para los proyectos de SPA basados en React
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Compilación de front-end para la SPA de reacción {#frontend-react}

Este documento explica los detalles del proyecto creado al utilizar el arquetipo para crear una aplicación de una sola página (SPA) basada en el marco de React. Es decir, cuando establece la opción `frontendModule` en `react`.

## Información general {#overview}

Este proyecto se ha arrancado con [create-response-app](https://github.com/facebook/create-react-app).

Esta aplicación está diseñada para consumir el modelo AEM de un sitio. Generará automáticamente el diseño mediante los componentes auxiliares del paquete [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components).

## Secuencias de comandos {#scripts}

En el directorio del proyecto, puede ejecutar los siguientes comandos:

### inicio npm {#npm-start}

```
npm start
```

Este comando ejecuta la aplicación en modo de desarrollo mediante el proxy del modelo JSON desde una instancia de AEM local que se ejecuta en http://localhost:4502. Esto supone que todo el proyecto se ha implementado para AEM al menos una vez (`mvn clean install -PautoInstallPackage` en la raíz del proyecto).

Después de ejecutar `npm start` en el directorio [ui.front](uifrontend.md), la aplicación se abrirá automáticamente en el explorador (en la ruta `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Si realiza modificaciones, la página se volverá a cargar.

Si está obteniendo errores relacionados con CORS, puede que desee configurar AEM de la siguiente manera:

1. Vaya a Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra la configuración de la &quot;Política de uso compartido de recursos entre Orígenes de Adobe Granite&quot;
1. Cree una nueva configuración con los siguientes valores adicionales:
   * Orígenes permitidos: http://localhost:3000
   * Encabezados admitidos: Autorización
   * Métodos permitidos: OPTIONS

### prueba npm {#npm-test}

```
npm test
```

Este comando inicia el ejecutor de pruebas en el modo de reloj interactivo. Consulte la [documentación de Reacción sobre la ejecución de pruebas](https://facebook.github.io/create-react-app/docs/running-tests) para obtener más información.

### npm run build {#npm-run-build}

```
npm run build
```

Este comando crea la aplicación para producción en la carpeta de compilación. Agrupa Reaccione en modo de producción y optimiza la compilación para obtener el mejor rendimiento. Consulte la [documentación de Reacción sobre la implementación](https://facebook.github.io/create-react-app/docs/deployment) para obtener más información.

Además, se genera un AEM ClientLib desde la aplicación mediante el paquete [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Compatibilidad con exploradores {#browser-support}

De forma predeterminada, este proyecto utiliza la opción predeterminada de [Browserslist](https://github.com/browserslist/browserslist) para identificar los exploradores de destinatario. Además, incluye polirellenos para las características de idioma moderno que admiten exploradores más antiguos (por ejemplo, Internet Explorer 11). Si la compatibilidad con estos exploradores no es un requisito, se pueden eliminar las importaciones y dependencias de relleno múltiple.

## División de código {#code-splitting}

La aplicación React está configurada para utilizar la división de código [](https://webpack.js.org/guides/code-splitting) de forma predeterminada. Al crear la aplicación para producción, el código se mostrará en varios fragmentos:

```
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

La carga de fragmentos solo cuando son necesarios puede mejorar significativamente el rendimiento de la aplicación.

Para que esta función funcione con AEM, la aplicación debe poder identificar qué archivos JS y CSS deben solicitarse desde el HTML generado por AEM. Esto se puede lograr utilizando la clave &quot;entrypoints&quot; en el archivo asset-manifest.json. El archivo se analiza en clientlib.config.js y solo los archivos de punto de entrada se incluyen en ClientLib. Los archivos restantes se colocan en el directorio de recursos de ClientLib y se solicitarán de forma dinámica y, por tanto, solo se cargarán cuando realmente se necesiten.

Consulte la [documentación general del módulo ui.frontender](uifrontend.md#clientlibs) para obtener más información sobre cómo AEM ClientLibs se utilizan en el arquetipo del proyecto.
