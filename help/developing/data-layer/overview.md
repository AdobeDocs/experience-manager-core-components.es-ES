---
title: Uso de la capa de datos del cliente de Adobe con los componentes principales
description: Uso de la capa de datos del cliente de Adobe con los componentes principales
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 55c984d3-deb7-4eda-a81d-7768791d2b46
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 100%

---


# Uso de la capa de datos del cliente de Adobe con los componentes principales {#data-layer-core-components}

El objetivo de la capa de datos del cliente de Adobe es reducir el esfuerzo por instrumentar sitios web mediante un método estandarizado para exponer y acceder a cualquier tipo de datos para cualquier script.

La capa de datos del cliente de Adobe no depende de la plataforma, pero está completamente integrada en los componentes principales para su uso con AEM.

Al igual que los componentes principales, el código de la capa de datos del cliente de Adobe está disponible en GitHub junto con la documentación para desarrolladores. Este documento ofrece información general sobre cómo los componentes principales interactúan con la capa de datos, pero los detalles técnicos completos se aplazan hasta la documentación de GitHub.

>[!TIP]
>
>Para obtener más información sobre la capa de datos del cliente de Adobe, [consulte los recursos de su repositorio de GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Para obtener más información técnica sobre la integración de la capa de datos del cliente de Adobe con los componentes principales, consulte el archivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) en el repositorio de componentes principales.

{{traditional-aem}}

## Instalación y activación {#installation-activation}

A partir de la versión 2.9.0 de los componentes principales, la capa de datos se distribuye con los componentes principales como una biblioteca de cliente de AEM y no es necesario realizar ninguna instalación. Todos los proyectos generados por el [tipo de archivo del proyecto de AEM versión 24+](/help/developing/archetype/overview.md) incluyen una capa de datos activada de forma predeterminada.

Para activar manualmente la capa de datos debe crear una [configuración de reconocimiento de contexto](/help/developing/context-aware-configs.md) para ello:

1. Cree la siguiente estructura debajo de la carpeta `/conf/<mySite>`, donde `<mySite>` es el nombre del proyecto del sitio:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Donde cada nodo tiene un `jcr:primaryType` establecido en `nt:unstructured`.
1. Agregue una propiedad boolean llamada `enabled` y configúrela en `true`.

   ![Ubicación de DataLayerConfig en el sitio de referencia WKND](/help/assets/datalayer-contextaware-sling-config.png)

   *Ubicación de DataLayerConfig en el sitio de referencia WKND*

1. Agregue una propiedad `sling:configRef` al nodo `jcr:content` del sitio debajo de `/content` (p. ej. `/content/<mySite>/jcr:content`) y configúrelo en `/conf/<mySite>` desde el paso anterior.

1. Una vez habilitada, puede comprobar la activación cargando una página del sitio fuera del editor, por ejemplo, utilizando la opción **Ver como publicado** en el editor. Inspeccione el origen de la página y la etiqueta `<body>` deben incluir un atributo `data-cmp-data-layer-enabled`

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

1. También puede abrir las herramientas para desarrolladores del explorador y el objeto JavaScript `adobeDataLayer` debería estar disponible en la consola. Introduzca el siguiente comando para obtener el estado de la capa de datos de su página actual:

   ```javascript
   window.adobeDataLayer.getState();
   ```

## Componentes compatibles {#supported-components}

Los siguientes componentes son compatibles con la capa de datos.

* [Acordeón](/help/components/accordion.md)
* [Ruta de navegación](/help/components/breadcrumb.md)
* [Botón](/help/components/button.md)
* [Carrusel](/help/components/carousel.md)
* [Fragmento de contenido](/help/components/content-fragment-component.md)
* [Imagen](/help/components/image.md)
* [Navegación por idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegación](/help/components/navigation.md)
* [Página](/help/components/page.md)
* [Barra de progreso](/help/components/progress-bar.md)
* [Pestañas](/help/components/tabs.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

Consulte también los [eventos activados por los componentes.](#events-components)

## Esquemas de datos de componentes principales {#data-schemas}

A continuación se muestra una lista de esquemas que los componentes principales utilizan con la capa de datos.

### Esquema de componente/elemento del contenedor {#item}

El esquema de componente/elemento de contenedor se utiliza en los siguientes componentes:

* [Ruta de navegación](/help/components/breadcrumb.md)
* [Botón](/help/components/button.md)
* [Navegación por idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegación](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

El esquema de componente/elemento del contenedor se define de la siguiente manera.

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

El siguiente [evento](#events) es relevante para el esquema de componente/elemento del contenedor:

* `cmp:click`

### Esquema de página {#page}

El esquema de página se utiliza en el siguiente componente:

* [Página](/help/components/page.md)

El esquema de página se define de la siguiente manera.

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

Un evento `cmp:show` se activa al cargar la página. Este evento se envía desde JavaScript en línea justo debajo de la etiqueta de apertura `<body>`, lo que lo convierte en el primer evento de la cola de eventos de la capa de datos.

### Esquema del contenedor {#container}

Los siguientes componentes utilizan el esquema del contenedor:

* [Acordeón](/help/components/accordion.md)
* [Pestañas](/help/components/tabs.md)
* [Carrusel](/help/components/carousel.md)

El esquema del contenedor se define de la siguiente manera.

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

Los siguientes [eventos](#events) son relevantes para el esquema del contenedor:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Esquema de imagen {#image}

El esquema de imagen se utiliza en el siguiente componente:

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

El esquema de recursos se utiliza dentro del [componente de imagen.](/help/components/image.md)

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

### Esquema de fragmento de contenido {#content-fragment}

El esquema de fragmento de contenido lo utiliza el componente [Fragmento de contenido.](/help/components/content-fragment-component.md)

El esquema de fragmento de contenido se define de la siguiente manera.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    elements            // array of the Content Fragment elements
}
```

El esquema utilizado para el elemento Fragmento de contenido es el siguiente.

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## Eventos de componentes principales {#events}

Hay varios eventos en los que los componentes principales se activan a través de la capa de datos. La práctica recomendada para interactuar con la capa de datos es [registrar un detector de eventos](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) y *luego* realizar una acción según el tipo de evento o el componente que activó el evento. Esto evitará posibles problemas de especie con scripts asincrónicos.

A continuación se muestran los eventos predeterminados ofrecidos por los componentes principales de AEM:

* **`cmp:click`**: al hacer clic en un elemento activo (un elemento que tiene un atributo `data-cmp-clickable`), la capa de datos activa un evento `cmp:click`.
* **`cmp:show`** y **`cmp:hide`**: la manipulación del acordeón (expandir/contraer), el carrusel (botones de siguiente/anterior) y los componentes de pestañas (selección de pestañas) hace que la capa de datos active `cmp:show` y se produzca un evento `cmp:hide`, respectivamente. También se envía un evento `cmp:show` al cargar la página y se espera que sea el primer evento.
* **`cmp:loaded`**: Cuando se rellene la capa de datos con los componentes principales de la página, la capa de datos activará un evento `cmp:loaded`.

### Eventos activados por el componente {#events-components}

En las siguientes tablas se enumeran los componentes principales estándar que activan eventos junto con esos eventos.

| Componente | Evento(s) |
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

### Información de la ruta del evento {#event-path-info}

Cada evento de capa de datos activado por un componente principal de AEM incluirá una carga útil con el siguiente objeto JSON:

```json
eventInfo: {
    path: '<component-path>'
}
```

Donde `<component-path>` es la ruta JSON al componente de la capa de datos que activó el evento.  El valor, disponible a través de `event.eventInfo.path`, es importante ya que se puede utilizar como parámetro de `adobeDataLayer.getState(<component-path>)` que recupera el estado actual del componente que activó el evento, lo que permite que el código personalizado acceda a datos adicionales y los añada a la capa de datos.

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

¿Quiere explorar la capa de datos y los componentes principales con más detalle? [Consulte este tutorial](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html?lang=es).

>[!TIP]
>
>Para explorar más en profundidad la flexibilidad de la capa de datos, revise las opciones de integración, incluido cómo habilitar la capa de datos para los componentes personalizados.
