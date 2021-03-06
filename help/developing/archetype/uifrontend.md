---
title: Creación del front-end de tipo de archivo del proyecto de AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 0e8082b0c5db1f2efc7db51f13123b5264a3a608
workflow-type: ht
source-wordcount: '1621'
ht-degree: 100%

---

# Módulo ui.frontend del tipo de archivo del proyecto de AEM {#uifrontend-module}

El tipo de archivo del proyecto de AEM incluye un mecanismo de versión del front-end opcional basado en Webpack. Por lo tanto, el módulo ui.frontend se convierte en la ubicación central de todos los recursos front-end del proyecto, incluidos los archivos JavaScript y CSS. Para aprovechar plenamente esta función tan útil y flexible, es importante comprender cómo encaja el desarrollo front-end en un proyecto de AEM.

## Proyectos de AEM y desarrollo front-end {#aem-and-front-end-development}

En términos muy simplificados, los proyectos de AEM se pueden considerar como dos partes separadas pero relacionadas:

* Desarrollo back-end que impulsa la lógica de AEM y produce bibliotecas Java, servicios OSGi, etc.
* Desarrollo front-end que impulsa la presentación y el comportamiento del sitio web resultante y produce bibliotecas JavaScript y CSS

Puesto que estos dos procesos de desarrollo se centran en diferentes partes del proyecto, el desarrollo del back-end y del front-end puede ocurrir en paralelo.

![diagrama del flujo de trabajo de front-end](/help/assets/front-end-flow.png)

Sin embargo, cualquier proyecto resultante debe utilizar los resultados de ambos esfuerzos de desarrollo, es decir, tanto del back-end como el front-end.

La ejecución de `npm run dev` inicia el proceso de versión del front-end que recopila los archivos JavaScript y CSS almacenados en el módulo ui.frontend y produce dos bibliotecas de cliente minimizadas o ClientLibs denominadas `clientlib-site` y `clientlib-dependencies`, y las deposita en el módulo ui.apps. ClientLibs se pueden implementar para AEM y le permiten almacenar el código del lado del cliente en el repositorio.

Cuando se ejecuta todo el tipo de archivo del proyecto de AEM utilizando `mvn clean install -PautoInstallPackage`, todos los artefactos del proyecto, incluido ClientLibs, se insertan en la instancia de AEM.

>[!TIP]
>
>Obtenga más información sobre cómo administra AEM las bibliotecas de cliente en la [documentación de desarrollo de AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=es), cómo [incluirlas](/help/developing/including-clientlibs.md) o consulte [cómo las utiliza el módulo ui.frontend.](#clientlib-generation)

## Información general sobre las bibliotecas de cliente {#clientlibs}

El módulo de front-end está disponible mediante un [ClientLib de AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=es). Al ejecutar el script de versión de NPM, la aplicación se crea y el paquete aem-clientlib-generator toma la salida de versión resultante y la transforma en un ClientLib de este tipo.

El ClientLib constará de los siguientes archivos y directorios:

* `css/`: Archivos CSS que se pueden solicitar en el HTML
* `css.txt`: Indica a AEM el orden y los nombres de los archivos en `css/` para que se puedan combinar
* `js/`: Archivos JavaScript que se pueden solicitar en el HTML
* `js.txt` Indica a AEM el orden y los nombres de los archivos en `js/` para que se puedan combinar
* `resources/`: Mapas de origen, fragmentos de código de punto de entrada (resultantes de la división del código), recursos estáticos (por ejemplo, iconos), etc.

## Posibles flujos de trabajo de desarrollo front-end {#possible-workflows}

El módulo de versión del front-end es una herramienta útil y muy flexible, pero no impone ninguna opinión particular sobre cómo debe usarse. Los siguientes son dos ejemplos de uso *posible*, pero las necesidades de cada proyecto pueden dictar otros modelos de uso.

### Uso del servidor de desarrollo estático de Webpack {#using-webpack}

Con Webpack puede aplicar estilos y desarrollar en función de la salida estática de páginas web de AEM dentro del módulo ui.frontend.

1. Vista previa de la página en AEM con el modo de vista previa de página o pasando `wcmmode=disabled` en la URL
1. Ver el origen de la página y guardar como HTML estático en el módulo ui.frontend
1. [Inicie Webpack](#webpack-dev-server) y empiece a aplicar estilos y generar el JavaScript y CSS necesarios
1. Ejecute `npm run dev` para generar las ClientLibs

En este flujo, un desarrollador de AEM puede realizar los pasos uno y dos y transferir el HTML estático al desarrollador de front-end que se desarrolla en función de la salida HTML de AEM.

>[!TIP]
>
>También se puede aprovechar la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_es) para capturar muestras de la salida de marcado de cada componente para que funcionen a nivel de componente en lugar de a nivel de página.

### Utilizar Storybook {#using-storybook}

Al utilizar [Storybook](https://storybook.js.org) puede realizar un desarrollo del front-end atómico más amplio. Aunque Storybook no está incluido en el tipo de archivo del proyecto de AEM, puede instalarlo y almacenar los artefactos de Storybook dentro del módulo ui.frontend. Cuando estén listos para realizar pruebas en AEM, se pueden implementar como bibliotecas de cliente ejecutando `npm run dev`.

>[!NOTE]
>
>El tipo de archivo del proyecto de AEM no incluye [Storybooktype](https://storybook.js.org). Si decide usarlo, debe instalarlo por separado.

### Determinar el marcado {#determining-markup}

Independientemente del flujo de trabajo de desarrollo front-end que decida implementar para su proyecto, los desarrolladores back-end y front-end deben acordar primero el marcado. Normalmente AEM define el marcado, que proporciona los componentes principales. [Sin embargo, esto se puede personalizar si es necesario](/help/developing/customizing.md#customizing-the-markup).

## Módulo ui.frontend {#ui-frontend-module}

El tipo de archivo del proyecto de AEM incluye un mecanismo de versión del front-end opcional basado en Webpack con las siguientes funciones.

* Soporte completo para TypeScript, ES6 y ES5 (con envoltorios Webpack aplicables)
* Vinculación TypeScript y JavaScript con un conjunto de reglas TSLint
* Salida ES5, para compatibilidad con exploradores anteriores
* Globalización
   * No es necesario agregar importaciones a ninguna parte
   * Ahora se pueden añadir todos los archivos JS y CSS a cada componente.
      * La práctica recomendada es `/clientlib/js`, `/clientlib/css` o `/clientlib/scss`
   * No se necesitan archivos `.content.xml` o `js.txt`/`css.txt` porque todo se ejecuta a través de Webpack.
   * El globber extrae todos los archivos JS de la carpeta `/component/`.
      * Webpack permite que los archivos CSS/SCSS se encadenen a través de archivos JS.
      * Se extraen a través de los dos puntos de entrada, `sites.js` y `vendors.js`.
   * El único archivo consumido por AEM son los archivos de salida `site.js` y `site.css` en `/clientlib-site`, así como `dependencies.js` y `dependencies.css` en `/clientlib-dependencies`
* Frascos
   * Principal (sitio js/css)
   * Proveedores (dependencias js/css)
* Compatibilidad total con Sass/Scss (Sass se compila en CSS a través de Webpack)
* Servidor de desarrollo de Webpack estático con proxy integrado a una instancia local de AEM

>[!NOTE]
>
>Para obtener más información técnica sobre el módulo ui.frontend, consulte la [documentación en GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Instalación {#installation}

1. Instale [NodeJS](https://nodejs.org/es/download/) (versión 10+) globalmente. Esto también instalará npm.
1. Vaya a ui.frontend en el proyecto y ejecute `npm install`.

>[!NOTE]
>
>Debe tener [ejecutar el tipo de archivo](overview.md) con la opción `-DoptionIncludeFrontendModule=y` para llenar la carpeta ui.frontend.

## Uso {#usage}

Los siguientes scripts npm controlan el flujo de trabajo de front-end:

* `npm run dev`: versión completa con la optimización de JS deshabilitada (agitación de árbol, etc.) y los mapas de origen habilitados y la optimización de CSS deshabilitada.
* `npm run prod`: versión completa con la optimización de JS habilitada (sacudido de árbol, etc.), mapas de origen deshabilitados y optimización de CSS habilitada.
* `npm run start`: inicia un servidor estático de desarrollo de Webpack para el desarrollo local con dependencias mínimas en AEM.

## Salida {#output}

El módulo ui.frontend compila el código en la carpeta `ui.frontend/src` y genera el CSS y JS compilados, así como cualquier recurso debajo de una carpeta denominada `ui.frontend/dist`.

* **Sitio**: `site.js`, `site.css` y una `resources/` la carpeta para el diseño, las imágenes y las fuentes dependientes se crean en una carpeta `dist/`clientlib-site.
* **Dependencias**: `dependencies.js` y `dependencies.css` se crean en una carpeta `dist/clientlib-dependencies`.

### JavaScript {#javascript}

* Optimización: en el caso de las versiones de producción, se eliminan todos los JS a los que no se llamen ni se utilicen.

### CSS {#css}

* Corrección automática: todas las CSS se ejecutan a través de un prefijo y todas las propiedades que requieran prefijos tendrán automáticamente las agregadas en el CSS.
* Optimización: en la publicación, toda la CSS se ejecuta a través de un optimizador (cssnano) que la normaliza según las siguientes reglas predeterminadas:
   * Reduce la expresión de llamada CSS siempre que sea posible, lo que garantiza la compatibilidad y la compresión del explorador.
Convierte entre valores de longitud, tiempo y ángulo equivalentes. Tenga en cuenta que, de forma predeterminada, los valores de longitud no se convierten.
   * Quita los comentarios de las reglas, selectores y declaraciones y alrededor de ellos
   * Elimina las reglas y las declaraciones duplicadas
      * Tenga en cuenta que esto solo funciona para duplicados exactos.
   * Elimina las reglas vacías, las consultas de medios y las reglas con selectores vacíos, ya que no afectan a la salida
   * Combina reglas adyacentes entre selectores y pares de propiedad/valor superpuestos
   * Garantiza que solo haya un @charset en el archivo CSS y lo mueve a la parte superior del documento
   * Reemplaza la palabra clave inicial CSS por el valor real, cuando la salida resultante sea menor
   * Comprime las definiciones de SVG en línea con SVGO
* Limpieza: incluye una tarea de limpieza explícita para borrar los archivos CSS, JS y Map generados bajo demanda.
* Asignación de fuentes: solo versión de desarrollo

>[!NOTE]
>
>La opción de versión de front-end utiliza archivos de configuración de Webpack solo para desarrollo y de solo prod que comparten un archivo de configuración común. De este modo, la configuración de desarrollo y producción se puede modificar de forma independiente.

### Generación de bibliotecas de clientes {#clientlib-generation}

El proceso de creación del módulo ui.frontend aprovecha el complemento [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) para mover el CSS compilado, JS y cualquier recurso al módulo ui.apps. La configuración de aem-clientlib-generator se define en `clientlib.config.js`. Se generan las siguientes bibliotecas de cliente:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Incluir bibliotecas de cliente en páginas {#clientlib-inclusion}

`clientlib-site` y `clientlib-dependencies` las categorías se incluyen en las páginas a través de la [configuración de la directiva de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=es#template-definitions) como parte de la plantilla predeterminada. Para ver la directiva, edite **Plantilla de página de contenido > Información de página > Directiva de página**.

La inclusión final de las bibliotecas de cliente en la página de sitios es la siguiente:

```html
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

Por supuesto, la inclusión anterior se puede modificar actualizando la Directiva de página y/o modificando las categorías y propiedades de incrustación de las respectivas bibliotecas de cliente.

### Servidor de desarrollo de Webpack estático {#webpack-dev-server}

Hay un webpack-dev-server incluido en el módulo ui.frontend que proporciona recarga en vivo para un rápido desarrollo front-end fuera de AEM. La configuración aprovecha el complemento html-webpack-plugin para insertar automáticamente CSS y JS compilados desde el módulo ui.frontend en una plantilla HTML estática.

#### Archivos importantes {#important-files}

* `ui.frontend/webpack.dev.js`
   * Esto contiene la configuración para el webpack-dev-serve y señala a la plantilla html que se va a utilizar.
   * También contiene una configuración proxy para una instancia de AEM que se ejecuta en localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Este es el HTML estático con el que se ejecutará el servidor.
   * Esto permite a los desarrolladores realizar cambios en CSS/JS y verlos reflejados inmediatamente en el marcado.
   * Se da por hecho que el marcado colocado en este archivo refleja con precisión el marcado generado por componentes de AEM.
   * El marcado de este archivo no se sincroniza automáticamente con el marcado del componente de AEM.
   * Este archivo también contiene referencias a bibliotecas de cliente almacenadas en AEM, como CSS de componente principal y CSS de cuadrícula interactiva.
   * El servidor de desarrollo de Webpack está configurado para proxy. Estos CSS/JS incluyen una instancia de AEM local que se ejecuta en función de la configuración que se encuentra en `ui.frontend/webpack.dev.js`.

#### Utilización {#using-webpack-server}

1. Desde la raíz del proyecto, ejecute el comando `mvn -PautoInstallSinglePackage clean install` para instalar todo el proyecto en una instancia de AEM que se ejecute en `localhost:4502`.
1. Vaya a la carpeta `ui.frontend`.
1. Ejecute el siguiente comando `npm run start` para iniciar el servidor de desarrollo de Webpack. Una vez iniciado, debe abrir un explorador (`localhost:8080` o el siguiente puerto disponible).

Ahora puede modificar los archivos CSS, JS, SCSS y TS y ver los cambios inmediatamente reflejados en el servidor de desarrollo de Webpack.
