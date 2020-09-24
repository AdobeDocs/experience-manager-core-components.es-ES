---
title: Creación de front-end de arquetipo de proyecto de AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
translation-type: tm+mt
source-git-commit: d8503d92c2d4948e54b2ad7d5407e4c7c98ebf83
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---


# Módulo ui.front del arquetipo del proyecto AEM {#uifrontend-module}

El Arquetipo de proyecto AEM incluye un mecanismo de diseño frontal opcional y dedicado basado en Webpack. El módulo ui.front se convierte así en la ubicación central de todos los recursos front-end del proyecto, incluidos los archivos JavaScript y CSS. Para aprovechar al máximo esta función útil y flexible, es importante comprender cómo encaja el desarrollo front-end en un proyecto AEM.

## Proyectos AEM y desarrollo front-end {#aem-and-front-end-development}

En términos muy simplificados, AEM proyectos pueden considerarse como dos partes separadas pero relacionadas:

* Desarrollo back-end que impulsa la lógica de AEM y produce bibliotecas de Java, servicios OSGi, etc.
* Desarrollo front-end que impulsa la presentación y el comportamiento del sitio web resultante y produce bibliotecas JavaScript y CSS

Debido a que estos dos procesos de desarrollo se centran en diferentes partes del proyecto, el desarrollo del back-end y del front-end puede suceder en paralelo.

![diagrama de flujo de trabajo de front-end](/help/assets/front-end-flow.png)

Sin embargo, cualquier proyecto resultante debe utilizar los resultados de ambos esfuerzos de desarrollo, es decir, tanto el back-end como el front-end.

La ejecución `npm run dev` inicio el proceso de compilación de front-end que recopila los archivos JavaScript y CSS almacenados en el módulo ui.front y produce dos bibliotecas de cliente minimizadas o ClientLibs llamadas `clientlib-site` y `clientlib-dependencies` depositadas en el módulo ui.apps. Las bibliotecas de cliente se pueden implementar para AEM y permiten almacenar el código del cliente en el repositorio.

Cuando se ejecuta todo el arquetipo de proyecto de AEM usando `mvn clean install -PautoInstallPackage` todos los artefactos del proyecto, incluyendo las bibliotecas de cliente, se insertan en la instancia de AEM.

>[!TIP]
>
>Obtenga más información sobre cómo AEM gestiona las bibliotecas de cliente en la documentación [de desarrollo](https://docs.adobe.com/content/help/es-ES/experience-manager-65/developing/introduction/clientlibs.html)AEM, cómo [incluirlas](/help/developing/including-clientlibs.md)o ver a continuación [cómo las utiliza el módulo ui.frontender.](#clientlib-generation)

## Información general de ClientLibs {#clientlibs}

El módulo front-end está disponible mediante un [AEM ClientLib](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html). Al ejecutar el script de compilación NPM, la aplicación se crea y el paquete aem-clientlib-generator toma la salida de compilación resultante y la transforma en un ClientLib de este tipo.

ClientLib constará de los siguientes archivos y directorios:

* `css/`:: Archivos CSS que se pueden solicitar en el HTML
* `css.txt`:: Indica AEM el orden y los nombres de los archivos en `css/` los que se pueden combinar
* `js/`:: Archivos JavaScript que se pueden solicitar en el código HTML
* `js.txt` Indica AEM el orden y los nombres de los archivos en `js/` los que se pueden combinar
* `resources/`:: Mapas de origen, fragmentos de código de no punto de entrada (resultantes de la división de códigos), recursos estáticos (por ejemplo, iconos), etc.

## Posibles Flujos de trabajo de desarrollo front-end {#possible-workflows}

El módulo de diseño frontal es una herramienta útil y muy flexible, pero no impone ninguna opinión particular sobre cómo debe utilizarse. Los siguientes son dos ejemplos de *posible* uso, pero las necesidades de cada proyecto pueden dictar otros modelos de uso.

### Uso de Webpack Static Development Server {#using-webpack}

Con Webpack puede diseñar y desarrollar en base a la salida estática de AEM páginas web dentro del módulo ui.frontender.

1. Previsualización de página en AEM mediante el modo de previsualización de página o pasando `wcmmode=disabled` en la dirección URL
1. Vista del origen de la página y guarde como HTML estático en el módulo ui.frontender
1. [Inicio webpack](#webpack-dev-server) y empezar a diseñar y generar el JavaScript y CSS necesarios
1. Ejecutar `npm run dev` para generar las bibliotecas de cliente

En este flujo, un desarrollador de AEM puede realizar los pasos uno y dos y pasar el HTML estático al desarrollador de front-end que se desarrolla en función de la salida HTML AEM.

>[!TIP]
>
>También se podría aprovechar la biblioteca [de](https://adobe.com/go/aem_cmp_library) componentes para capturar muestras de la salida de marcado de cada componente para trabajar en el nivel de componente en lugar de en el nivel de página.

### Uso de Storybook {#using-storybook}

Al utilizar [Storybook](https://storybook.js.org) , puede realizar más desarrollo atómico del front-end. Aunque Storybook no está incluido en el arquetipo del proyecto de AEM, puede instalarlo y almacenar los artefactos del libro de historias dentro del módulo ui.frontender. Cuando estén listos para realizar pruebas en AEM, se pueden implementar como bibliotecas de cliente `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) no está incluido en el arquetipo del proyecto de AEM. Si decide utilizarla, debe instalarla por separado.

### Determinación del marcado {#determining-markup}

Independientemente del flujo de trabajo de desarrollo front-end que decida implementar para su proyecto, los desarrolladores back-end y los desarrolladores front-end primero deben ponerse de acuerdo en el marcado. Normalmente AEM define el marcado, que lo proporcionan los componentes principales. [Sin embargo, esto se puede personalizar si es necesario](/help/developing/customizing.md#customizing-the-markup).

## Módulo ui.frontender {#ui-frontend-module}

El Arquetipo de proyecto AEM incluye un mecanismo de generación de front-end opcional basado en Webpack con las siguientes características.

* Compatibilidad total con TypeScript, ES6 y ES5 (con envoltorios de Webpack aplicables)
* Linting de TypeScript y JavaScript mediante un conjunto de reglas TSLint
* Salida ES5, para compatibilidad con exploradores heredados
* Globalización
   * No es necesario agregar importaciones a ningún lugar
   * Ahora se pueden agregar todos los archivos JS y CSS a cada componente.
      * La práctica recomendada está en curso `/clientlib/js`, `/clientlib/css`o `/clientlib/scss`
   * No se necesitan archivos `.content.xml` ni `js.txt`/`css.txt` ya que todo se ejecuta a través de Webpack.
   * El globber extrae todos los archivos JS de la `/component/` carpeta.
      * Webpack permite encadenar archivos CSS/SCSS mediante archivos JS.
      * Se extraen a través de los dos puntos de entrada `sites.js` y `vendors.js`.
   * El único archivo consumido por AEM son los archivos de salida `site.js` y `site.css` tanto `/clientlib-site` como `dependencies.js` y `dependencies.css` en `/clientlib-dependencies`
* Chunks
   * Principal (sitio js/css)
   * Proveedores (dependencias js/css)
* Compatibilidad total con Sass/Scss (Sass se compila en CSS a través de Webpack)
* Servidor de desarrollo de webpack estático con proxy integrado a una instancia local de AEM

>[!NOTE]
>
>Para obtener más información técnica sobre el módulo ui.frontender, consulte la [documentación en GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Instalación {#installation}

1. Instale [NodeJS](https://nodejs.org/en/download/) (v10+) de forma global. Esto también instalará npm.
1. Vaya a ui.frontender en el proyecto y ejecute `npm install`.

>[!NOTE]
>
>Debe haber [ejecutado el arquetipo](overview.md) con la opción `-DoptionIncludeFrontendModule=y` de rellenar la carpeta ui.frontender.

## Uso {#usage}

Los siguientes scripts npm impulsan el flujo de trabajo de front-end:

* `npm run dev` - compilación completa con la optimización de JS deshabilitada (temblor de árbol, etc.) y los mapas de origen habilitados y la optimización de CSS deshabilitada.
* `npm run prod` - compilación completa con la optimización de JS habilitada (sacudida de árboles, etc.), mapas de origen deshabilitados y optimización de CSS habilitada.
* `npm run start` - Inicio un servidor de desarrollo de webpack estático para el desarrollo local con dependencias mínimas en AEM.

## Salida {#output}

El módulo ui.front compila el código en la `ui.frontend/src` carpeta y genera el CSS y JS compilados, así como cualquier recurso debajo de una carpeta denominada `ui.frontend/dist`.

* **Sitio** : `site.js`, `site.css` y se crea una `resources/` carpeta para las imágenes y fuentes dependientes del diseño en una carpeta `dist/`clientlib-site.
* **Dependencias** : `dependencies.js` y `dependencies.css` se crean en una `dist/clientlib-dependencies` carpeta.

### JavaScript {#javascript}

* Optimización: en el caso de las compilaciones de producción, se eliminan todos los JS que no se estén utilizando o llamando.

### CSS {#css}

* Autoprefixing: Todas las CSS se ejecutan a través de un prefijo y todas las propiedades que requieran un prefijo tendrán automáticamente las agregadas en la CSS.
* Optimización: en la publicación, toda la CSS se ejecuta mediante un optimizador (cssnano) que la normaliza según las siguientes reglas predeterminadas:
   * Reduce la expresión de clics de CSS siempre que sea posible, garantizando la compatibilidad del navegador y la compresiónConvierte entre valores de longitud, tiempo y ángulo equivalentes. Tenga en cuenta que, de forma predeterminada, los valores de longitud no se convierten.
   * Quita los comentarios de las reglas, selectores y declaraciones
   * Quita reglas, reglas y declaraciones duplicadas
      * Tenga en cuenta que esto solo funciona para duplicados exactos.
   * Quita reglas vacías, consultas de medios y reglas con selectores vacíos, ya que no afectan a la salida
   * Combina reglas adyacentes por selectores y pares de propiedades/valores superpuestos
   * Garantiza que solo un @charset esté presente en el archivo CSS y lo mueve a la parte superior del documento
   * Reemplaza la palabra clave inicial CSS con el valor real, cuando la salida resultante es menor
   * Comprime las definiciones de SVG integradas con SVGO
* Limpieza: incluye una tarea limpia explícita para eliminar los archivos CSS, JS y Map generados a petición.
* Asignación de origen: sólo compilación de desarrollo

>[!NOTE]
>
>La opción de compilación de front-end utiliza archivos de configuración de webpack solo para desarrollo y solo para prod que comparten un archivo de configuración común. De este modo, los ajustes de desarrollo y producción se pueden modificar de forma independiente.

### Generación de biblioteca de clientes {#clientlib-generation}

El proceso de compilación del módulo ui.frontened aprovecha el complemento [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) para mover el CSS compilado, JS y cualquier recurso al módulo ui.apps. La configuración de aem-clientlib-generator se define en `clientlib.config.js`. Se generan las siguientes bibliotecas de cliente:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencias** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusión de bibliotecas de cliente en páginas {#clientlib-inclusion}

`clientlib-site` y `clientlib-dependencies` las categorías se incluyen en las páginas mediante la configuración [de la directiva de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#template-definitions) página como parte de la plantilla predeterminada. Para vista de la política, edite la plantilla de página de **contenido > Información de página > Política** de página.

La inclusión final de las bibliotecas de cliente en la página de sitios es la siguiente:

```
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

Por supuesto, la inclusión anterior se puede modificar mediante la actualización de la directiva de página y/o la modificación de las categorías y propiedades incrustadas de las bibliotecas de cliente respectivas.

### Servidor de desarrollo de Webpack estático {#webpack-dev-server}

El módulo ui.frontender incluye un webpack-dev-server que proporciona recarga en directo para un rápido desarrollo front-end fuera de AEM. La configuración aprovecha el complemento html-webpack-plugin para insertar automáticamente CSS y JS compilados desde el módulo ui.front en una plantilla HTML estática.

#### Archivos importantes {#important-files}

* `ui.frontend/webpack.dev.js`
   * Contiene la configuración para el webpack-dev-serve y señala a la plantilla html que se va a utilizar.
   * También contiene una configuración proxy para una instancia de AEM que se ejecuta en localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Es el HTML estático con el que se ejecutará el servidor.
   * Esto permite a los desarrolladores realizar cambios en CSS/JS y verlos reflejados inmediatamente en el marcado.
   * Se da por hecho que el marcado colocado en este archivo refleja con precisión el marcado generado por AEM componentes.
   * El marcado de este archivo no se sincroniza automáticamente con AEM marcado del componente.
   * Este archivo también contiene referencias a bibliotecas de cliente almacenadas en AEM, como CSS de componente principal y CSS de cuadrícula adaptable.
   * El servidor de desarrollo de webpack está configurado para proxy que estos CSS/JS incluyen desde una instancia de AEM local que se ejecuta en función de la configuración que se encuentra en `ui.frontend/webpack.dev.js`.

#### Utilizando {#using-webpack-server}

1. Desde la raíz del proyecto, ejecute el comando `mvn -PautoInstallSinglePackage clean install` para instalar el proyecto completo en una instancia de AEM que se ejecute en `localhost:4502`.
1. Navegue dentro de la `ui.frontend` carpeta.
1. Ejecute el siguiente comando `npm run start` para inicio del servidor de desarrollo de webpack. Una vez iniciado, debe abrir un navegador (`localhost:8080` o el siguiente puerto disponible).

Ahora puede modificar archivos CSS, JS, SCSS y TS y ver los cambios reflejados inmediatamente en el servidor de desarrollo de webpack.
