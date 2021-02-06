---
title: Uso de la capa de datos del cliente de Adobe con los componentes principales
description: Uso de la capa de datos del cliente de Adobe con los componentes principales
translation-type: tm+mt
source-git-commit: 1ada05d5089ccef95d41d47468776654e397f31d
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 3%

---


# Uso de la capa de datos del cliente de Adobe con los componentes principales {#data-layer-core-components}

El objetivo de la capa de datos del cliente de Adobe es reducir el esfuerzo de instrumentar sitios web proporcionando un método estandarizado para exponer y acceder a cualquier tipo de datos para cualquier secuencia de comandos.

La capa de datos del cliente de Adobe no depende de la plataforma, pero está completamente integrada en los componentes principales para su uso con AEM.

Al igual que los componentes principales, el código de la capa de datos del cliente de Adobe está disponible en GitHub junto con la documentación para desarrolladores. Este documento proporciona una visión general de cómo interactúan los componentes principales con la capa de datos, pero los detalles técnicos completos se posponen a la documentación de GitHub.

>[!TIP]
>
>Para obtener más información sobre la capa de datos del cliente de Adobe, [consulte los recursos de su repositorio de GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Para obtener más información técnica sobre la integración de la capa de datos del cliente de Adobe con los componentes principales, consulte el archivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) en el repositorio de componentes principales.

## Instalación y Activación {#installation-activation}

A partir de la versión 2.9.0 de los componentes principales, la capa de datos se distribuye con los componentes principales como una biblioteca del cliente AEM y no es necesaria ninguna instalación. Todos los proyectos generados por [AEM Project Archetype v. 24+](/help/developing/archetype/overview.md) incluyen una capa de datos activada de forma predeterminada.

Para activar manualmente la capa de datos debe crear una configuración [contextual](/help/developing/context-aware-configs.md) para ella:

1. Cree la siguiente estructura debajo de la carpeta `/conf/<mySite>`, donde `<mySite>` es el nombre del proyecto del sitio:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Donde cada nodo tiene un `jcr:primaryType` establecido en `nt:unstructured`.
1. Añada una propiedad booleana llamada `enabled` y configúrela en `true`.

   ![Ubicación de DataLayerConfig en el sitio de referencia WKND](/help/assets/datalayer-contextaware-sling-config.png)

   *Ubicación de DataLayerConfig en el sitio de referencia WKND*

1. Añada una propiedad `sling:configRef` en el nodo `jcr:content` de su sitio debajo de `/content` (por ejemplo: `/content/<mySite>/jcr:content`) y establézcalo en `/conf/<mySite>` desde el paso anterior.

1. Una vez habilitada, puede comprobar la activación cargando una página del sitio fuera del editor. Inspect el origen de la página y la etiqueta `<body>` deben incluir un atributo `data-cmp-data-layer-enabled`

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. También puede abrir las herramientas de desarrollador del explorador y, en la consola, el objeto `adobeDataLayer` JavaScript debería estar disponible. Introduzca el siguiente comando para obtener el estado de la capa de datos de la página actual:

   ```javascript
   window.adobeDataLayer.getState();
   ```

## Esquemas de datos de componentes principales {#data-schemas}

A continuación se muestra una lista de esquemas que los componentes principales utilizan con la capa de datos.

### Esquema de elemento de componente/Contenedor {#item}

El esquema Componente/Elemento de Contenedor se utiliza en los siguientes componentes:

* [Ruta de navegación](/help/components/breadcrumb.md)
* [Botón](/help/components/button.md)
* [Navegación por idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegación](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

El esquema Componente/Elemento de Contenedor se define de la siguiente manera.

```javascript
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```

El siguiente [evento](#events) es relevante para el esquema del componente/elemento de Contenedor:

* `cmp:click`

### Esquema de página {#page}

El siguiente componente utiliza el esquema Página:

* [Página](/help/components/page.md)

El esquema Página se define de la siguiente manera.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

Un evento `cmp:show` se activa al cargar la página. Este evento se distribuye desde JavaScript en línea justo debajo de la etiqueta `<body>` de apertura, lo que lo convierte en el evento más antiguo de la cola de eventos de capa de datos.

### Esquema de contenedor {#container}

Los siguientes componentes utilizan el esquema de Contenedor:

* [Acordeón](/help/components/accordion.md)
* [Pestañas](/help/components/tabs.md)
* [Carrusel](/help/components/carousel.md)

El esquema de Contenedor se define de la siguiente manera.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

Los siguientes [eventos](#events) son relevantes para el esquema del Contenedor:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Esquema de imagen {#image}

El siguiente componente utiliza el esquema de imagen:

* [Imagen](/help/components/image.md)

El esquema de imagen se define de la siguiente manera.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

El siguiente [evento](#events) es relevante para el esquema de imagen:

* `cmp:click`

### Esquema de recursos {#asset}

El esquema de recursos se utiliza dentro del componente [Imagen.](/help/components/image.md)

El esquema de recursos se define de la siguiente manera.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

El siguiente [evento](#events) es relevante para el esquema de recursos:

* `cmp:click`

## Eventos de componentes principales {#events}

Hay varios eventos que déclencheur de componentes principales a través de la capa de datos. La mejor manera de interactuar con la capa de datos es [registrar un detector de evento](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) y *luego* realizar una acción basada en el tipo de evento y/o componente que activó el evento. Esto evitará posibles condiciones de carrera con scripts asincrónicos.

A continuación se muestran los eventos predeterminados proporcionados por AEM componentes principales:

* **`cmp:click`** - Al hacer clic en un elemento en el que se puede hacer clic (un elemento que tiene un  `data-cmp-clickable` atributo), la capa de datos se déclencheur en un  `cmp:click` evento.
* **`cmp:show`** y  **`cmp:hide`** - Manipular el acordeón (expandir/contraer), el carrusel (botones siguiente/anterior) y los componentes de fichas (selección de tabuladores) hacen que la capa de datos se déclencheur  `cmp:show` y se  `cmp:hide` evento, respectivamente. También se envía un evento `cmp:show` al cargar la página y se espera que sea el primer evento.
* **`cmp:loaded`** - Tan pronto como se rellena la capa de datos con los componentes principales de la página, la capa de datos déclencheur un  `cmp:loaded` evento.

### Eventos activados por componente {#events-components}

Las siguientes tablas lista los componentes principales estándar que déclencheur eventos junto con esos eventos.

| Componente | Eventos |
|---|---|
| [Acordeón](/help/components/accordion.md) | `cmp:show` y `cmp:hide` |
| [Botón](/help/components/button.md) | `cmp:click` |
| [Ruta de navegación](/help/components/breadcrumb.md) | `cmp:click` |
| [Carrusel](/help/components/carousel.md) | `cmp:show` y `cmp:hide` |
| [Navegación por idiomas](/help/components/language-navigation.md) | `cmp:click` |
| [Navegación](/help/components/navigation.md) | `cmp:click` |
| [Página](/help/components/page.md) | `cmp:show` |
| [Pestañas](/help/components/tabs.md) | `cmp:show` y `cmp:hide` |
| [Teaser](/help/components/teaser.md) | `cmp:click` |

### Información de ruta de evento {#event-path-info}

Cada evento de capa de datos activado por un componente principal de AEM incluirá una carga útil con el siguiente objeto JSON:

```json
eventInfo: {
    path: '<component-path>'
}
```

Donde `<component-path>` es la ruta JSON al componente en la capa de datos que activó el evento.  El valor, disponible mediante `event.eventInfo.path`, es importante ya que se puede utilizar como parámetro de `adobeDataLayer.getState(<component-path>)`, que recupera el estado actual del componente que activó el evento, permitiendo que el código personalizado acceda a datos adicionales y los agregue a la capa de datos.

Por ejemplo:

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## Tutorial

¿Desea explorar la capa de datos y los componentes principales con más detalle? [Consulte este tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html) práctico.

>[!TIP]
>
>Para explorar más a fondo la flexibilidad de la capa de datos, consulte las opciones de integración, incluida la forma de habilitar la capa de datos para los componentes personalizados.
