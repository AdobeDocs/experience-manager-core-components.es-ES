---
title: Inclusión de bibliotecas de cliente
description: Existen varias formas de incluir bibliotecas de cliente según el caso de uso.
role: Arquitecto, Desarrollador, Administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---


# Inclusión de bibliotecas de cliente {#including-client-libraries}

Existen varias formas de incluir [bibliotecas de cliente](/help/developing/archetype/uifrontend.md#clientlibs) según el caso de uso. Este documento proporciona ejemplos y muestra [fragmentos de HTL](https://docs.adobe.com/content/help/es-ES/experience-manager-htl/using/overview.html) para cada uno.

## Uso predeterminado recomendado {#recommended-default-usage}

Si no tiene tiempo para investigar qué es lo mejor de su situación, incluya las bibliotecas de cliente colocando las siguientes líneas HTML dentro del elemento `head` de su página:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Esto incluirá tanto el CSS como el JS en la página `head`, pero si agrega el atributo `defer` a las inclusiones JS `script` , los exploradores esperarán a que el DOM esté listo antes de ejecutar las secuencias de comandos y, por lo tanto, optimizarán la velocidad de carga de la página.

## Uso básico {#basic-usage}

La sintaxis básica para incluir JS y CSS de una categoría de biblioteca de cliente, que generará todos los elementos CSS `link` o elementos JS `script` correspondientes, es la siguiente:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Para hacer lo mismo para varias categorías de biblioteca de cliente a la vez, se puede pasar una matriz de cadenas al parámetro `categories`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Solo CSS o JS {#css-js-only}

Con frecuencia, se desea colocar las inclusiones CSS en el elemento HTML `head` y el JS incluye justo antes del cierre del elemento `body` .

En `head`, para incluir solo el CSS y no el JS, utilice `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Antes de cerrar `body`, para incluir solo el JS y no el CSS, utilice `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Atributos {#attributes}

Para aplicar atributos a los elementos `link` CSS generados y/o a los elementos JS `script` , es posible realizar una serie de parámetros:

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

* `media`: atributos de JS de cadena  `script` que se pueden pasar a  `jsAndCssIncludes` y  `jsIncludes`:
* `async`: boolean
* `defer`: booleano
* `onload`: cadena
* `crossorigin`: cadena

## Inclinación {#inlining}

En algunos casos, ya sea para la optimización o para correo electrónico o [AMP,](amp.md) puede ser necesario integrar el CSS o JS en la salida del HTML.

Para insertar el CSS, se puede utilizar `cssInline` , en cuyo caso debe escribir el elemento `style` que lo rodea:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Del mismo modo, para insertar el JS, se puede utilizar `jsInline` , en cuyo caso debe escribir el elemento `script` que lo rodea:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## Cargando CSS y JavaScript con contexto {#context-aware-loading}

El [Componente de página](/help/components/page.md) también admite la carga de etiquetas CSS, JavaScript o meta definidas por el desarrollador y según el contexto.

Esto se hace creando un [recurso según el contexto](context-aware-configs.md) para `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` con la siguiente estructura:

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Consulte la documentación técnica del componente Página para obtener más información.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
