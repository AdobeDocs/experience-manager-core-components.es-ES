---
title: Uso de la capa de datos del cliente de Adobe con los componentes principales
description: Uso de la capa de datos del cliente de Adobe con los componentes principales
translation-type: tm+mt
source-git-commit: 4a44a5f584efa736320556f6b4e2f4126d058a48
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 5%

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

A partir de la versión 2.9.0 de los componentes principales, la capa de datos se distribuye con los componentes principales como clientlib. No es necesaria ninguna instalación.

Sin embargo, la capa de datos no está activada de forma predeterminada. Para activar la capa de datos debe crear una configuración [](/help/developing/context-aware-configs.md) contextual para ella:

1. Cree la siguiente estructura debajo del `/conf` nodo:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Tipo de nodo: `nt:unstructured`
1. Añada una propiedad booleana llamada `enabled` y configúrela en `true`.
1. Añada una `sling:configRef` propiedad en el `jcr:content` nodo del sitio siguiente `/content` (p. ej. `/content/<mySite>/jcr:content`) y configúrela en `/conf/<mySite>`.

Una vez habilitada, puede comprobar la activación cargando una página del sitio fuera del editor. Cuando inspeccione la página verá que se ha cargado la capa de datos del cliente de Adobe.

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

El siguiente [evento](#events) es pertinente para el esquema de elementos de componente/Contenedor:

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

### Esquema contenedor {#container}

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

Los siguientes [eventos](#events) son pertinentes para el esquema de Contenedor:

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

El siguiente [evento](#events) es relevante para el esquema de imágenes:

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

El [evento](#events) siguiente es pertinente para el esquema de activos:

* `cmp:click`

## Sucesos {#events}

Existen varios eventos que la capa de datos desencadena.

* **`cmp:click`** - Al hacer clic en un elemento en el que se puede hacer clic (un elemento que tiene un `data-cmp-clickable` atributo), la capa de datos activa un `cmp:click` evento.
* **`cmp:show`** y **`cmp:hide`** : Al manipular el acordeón (expandir/contraer), los componentes carrusel (botones siguiente/anterior) y las fichas (selección de tabuladores), la capa de datos se activa `cmp:show` y se `cmp:hide` eventos respectivamente.
* **`cmp:loaded`** - Tan pronto como la capa de datos se rellena con los componentes principales de la página, la capa de datos desencadena un `cmp:loaded` evento.

### Eventos activados por componente {#events-components}

Las siguientes tablas lista los componentes principales estándar que activan eventos junto con esos eventos.

| Componente | Eventos |
|---|---|
| [Navegación](/help/components/navigation.md) | `cmp:click` |
| [Navegación por idiomas](/help/components/language-navigation.md) | `cmp:click` |
| [Ruta de navegación](/help/components/breadcrumb.md) | `cmp:click` |
| [Botón](/help/components/button.md) | `cmp:click` |
| [Carrusel](/help/components/carousel.md) | `cmp:show` y `cmp:hide` |
| [Pestañas](/help/components/tabs.md) | `cmp:show` y `cmp:hide` |
| [Acordeón](/help/components/accordion.md) | `cmp:show` y `cmp:hide` |
