---
title: Compilación de front-end de arquetipo de proyecto de AEM
seo-title: Compilación de front-end de arquetipo de proyecto de AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
seo-description: Una plantilla de proyecto para aplicaciones basadas en AEM
contentOwner: bohnert
content-type: referencia
topic-tags: componentes principales
translation-type: tm+mt
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# Compilación de front-end de arquetipo de proyecto de AEM {#aem-project-archetype-front-end-build}

El arquetipo de proyecto de AEM incluye un mecanismo de compilación front-end opcional basado en Webpack con las siguientes funciones.

* Compatibilidad total con TypeScript, ES6 y ES5 (con envoltorios de Webpack aplicables)
* Linting de TypeScript y JavaScript mediante un conjunto de reglas TSLint
* Salida ES5, para compatibilidad con exploradores heredados
* Globalización
   * No es necesario agregar importaciones a ningún lugar
   * Ahora se pueden agregar todos los archivos JS y CSS a cada componente
      * La práctica recomendada está en curso `/clientlib/js`, `/clientlib/css`o `/clientlib/scss`
   * No se necesitan `.content.xml` ni archivos `js.txt`/`css.txt` ya que todo se ejecuta a través de Webpack
   * El globber extrae todos los archivos JS de la `/component/` carpeta.
      * Webpack permite encadenar archivos CSS/SCSS mediante archivos JS.
      * Se extraen a través de los dos puntos de entrada `sites.js` y `vendors.js`.
   * El único archivo consumido por AEM son los archivos de salida `site.js` y `site.css` tanto en `/clientlib-site` como `dependencies.js` y `dependencies.css` en `/clientlib-dependencies`
* Chunks
   * Principal (sitio js/css)
   * Proveedores (dependencias js/css)
* Compatibilidad total con Sass/Scss (Sass se compila en CSS a través de Webpack).

## Instalación {#installation}

1. Instale [NodeJS](https://nodejs.org/en/download/) (v10+) de forma global. Esto también instalará npm.
1. Vaya a ui.frontender en el proyecto y ejecute `npm install`.

## Uso {#usage}

Los siguientes scripts npm impulsan el flujo de trabajo de front-end:

* `npm run dev` - compilación completa con la optimización de JS deshabilitada (temblor de árbol, etc.) y los mapas de origen habilitados y la optimización de CSS deshabilitada.
* `npm run prod` - compilación completa con la optimización de JS habilitada (sacudida de árboles, etc.), mapas de origen deshabilitados y optimización de CSS habilitada.

## Salida {#output}

### General {#general}

* Sitio: `site.js` y `site.css` se crean en una carpeta clientlib-site.
* Dependencias - `dependencies.js` y `dependencies.css` se crean en una carpeta clientlib-dependencias.

### JavaScript {#javascript}

* Optimización: en el caso de las compilaciones de producción, se eliminan todos los JS que no se estén utilizando o llamando.

### CSS {#css}

* Autoprefixing: Todas las CSS se ejecutan a través de un prefijo y todas las propiedades que requieran un prefijo tendrán automáticamente las agregadas en la CSS.
* Optimización: en la publicación, toda la CSS se ejecuta mediante un optimizador (cssnano) que la normaliza según las siguientes reglas predeterminadas:
   * Reduce la expresión de calc de CSS siempre que sea posible, garantizando la compatibilidad del navegador y la compresiónConvierte entre valores de longitud, tiempo y ángulo equivalentes. Tenga en cuenta que, de forma predeterminada, los valores de longitud no se convierten.
   * Quita los comentarios de las reglas, selectores y declaraciones
   * Quita reglas, reglas y declaraciones duplicadas
      * Tenga en cuenta que esto solo funciona para duplicados exactos.
   * Quita reglas vacías, consultas de medios y reglas con selectores vacíos, ya que no afectan al resultado
   * Combina reglas adyacentes por selectores y pares de propiedades/valores superpuestos
   * Garantiza que solo un @charset esté presente en el archivo CSS y lo mueve a la parte superior del documento
   * Reemplaza la palabra clave inicial CSS con el valor real, cuando la salida resultante es menor
   * Comprime las definiciones SVG integradas con SVGO
* Limpieza: incluye una tarea explícita y limpia para eliminar los archivos CSS, JS y Map generados a petición.
* Asignación de origen: sólo compilación de desarrollo

>[!NOTE]
>La opción de compilación de front-end utiliza archivos de configuración de webpack solo para desarrollo y solo para prod que comparten un archivo de configuración común. De este modo, los ajustes de desarrollo y producción se pueden modificar de forma independiente.
