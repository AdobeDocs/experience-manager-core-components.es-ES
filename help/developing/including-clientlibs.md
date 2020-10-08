---
title: Inclusión de bibliotecas de cliente
description: Existen diferentes maneras de incluir bibliotecas de cliente según el caso de uso.
translation-type: tm+mt
source-git-commit: 87e39566617f64b91bd8e98b3779b9b5c426c31c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 4%

---


# Inclusión de bibliotecas de cliente {#including-client-libraries}

Existen diferentes maneras de incluir bibliotecas [de](/help/developing/archetype/uifrontend.md#clientlibs) cliente según el caso de uso. Este documento proporciona ejemplos y fragmentos [HTL de muestra](https://docs.adobe.com/content/help/es-ES/experience-manager-htl/using/overview.html) para cada uno.

## Uso predeterminado recomendado {#recommended-default-usage}

Si no tiene tiempo para investigar qué es lo mejor de su situación, incluya las bibliotecas de cliente colocando las siguientes líneas HTML dentro del elemento de página `head` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Esto incluirá tanto el CSS como el JS en la página `head`, pero agregando el `defer` atributo a los elementos incluidos en el JS `script` , de modo que los navegadores esperen a que el DOM esté listo antes de ejecutar los scripts y, por lo tanto, optimizarán la velocidad de carga de la página.

## Uso básico {#basic-usage}

La sintaxis básica para incluir JS y CSS de una categoría de biblioteca de cliente, que generará todos los `link` elementos CSS y/o elementos JS `script` correspondientes, es la siguiente:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Para hacer lo mismo con varias categorías de biblioteca de cliente a la vez, se puede pasar una matriz de cadenas al `categories` parámetro:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Solo CSS o JS {#css-js-only}

A menudo, uno quiere colocar las inclusiones CSS en el elemento HTML `head` , y JS incluye justo antes del cierre del `body` elemento.

En el `head`, para incluir solo el CSS y no el JS, utilice `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Antes del `body` cierre, para incluir solo el JS, y no el CSS, utilice `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Atributos {#attributes}

Para aplicar atributos a los `link` elementos CSS generados y/o a los elementos JS `script` , es posible utilizar una serie de parámetros:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Atributos CSS `link` que se pueden pasar a `jsAndCssIncludes` y `cssIncludes`:

* `media`: cadena

Atributos JS `script` que se pueden pasar a `jsAndCssIncludes` y `jsIncludes`:

* `async`: boolean
* `defer`: boolean
* `onload`: cadena
* `crossorigin`: cadena

## Inclinación {#inlining}

En algunos casos, ya sea para la optimización o para correo electrónico o [AMP,](amp.md) puede que sea necesario integrar el CSS o JS en la salida del HTML.

Para alinear la CSS, `cssInline` se puede utilizar, en cuyo caso se debe escribir el `style` elemento que la rodea:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Del mismo modo, para integrar el JS, `jsInline` se puede utilizar, en cuyo caso se debe escribir el `script` elemento circundante:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
