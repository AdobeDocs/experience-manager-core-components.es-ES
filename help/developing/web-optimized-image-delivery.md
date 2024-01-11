---
title: Entrega de imágenes optimizadas para la web
description: Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para la web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: a312eb7a1dc68a264eaf0938c450a17f7cbc4506
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 95%

---

# Entrega de imágenes optimizadas para la web {#web-optimized-image-delivery}

Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para la web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.

## Información general {#overview}

La funcionalidad de entrega de imágenes optimizadas para la web de AEM as a Cloud Service ofrece recursos de imagen de DAM en [formato WebP.](https://developers.google.com/speed/webp) WebP puede reducir el tamaño de descarga de una imagen en aproximadamente un 25 % en promedio, lo que resulta en una carga de página más rápida.

La activación de la entrega de imágenes optimizadas para la web en los componentes principales es sencilla y, como todos los exploradores comunes admiten WebP, la experiencia es transparente para el usuario final. La única diferencia que notará es que el contenido se carga más rápido.

## Activación de la entrega de imágenes optimizadas para la web para componentes principales {#activating}

Para activar la entrega de imágenes optimizadas para la web, edite una plantilla de página y simplemente active la opción **Habilitar imágenes optimizadas para web** dentro del cuadro de diálogo de diseño del [componente de imagen.](/help/components/image.md#design-dialog) Esta opción está disponible para las versiones 1, 2 y 3 del componente de imagen.

Si no conoce los cuadros de diálogo de diseño y las plantillas de página de AEM, [revise este documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Habilitación de la entrega de imágenes optimizadas para la web en el cuadro de diálogo de diseño](/help/assets/web-optimized-image-delivery.png)

Eso es todo. El componente de imagen ahora entrega las imágenes en formato WebP.

Una vez que se activa la entrega de imágenes optimizadas para la web, es posible que también se desee comprobar la configuración de Dispatcher para verificar que no bloquee la solicitud al servicio de imágenes. Las URL de este servicio tienen la siguiente forma.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Esto se puede generalizar con esta expresión regular.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Verificación de la entrega de WebP {#verifying}

La entrega de imágenes optimizadas para la web es transparente para el consumidor del contenido y no afecta al marcado. Lo único que notará un usuario final es un tiempo de carga más rápido.

Por lo tanto, para observar el cambio real de comportamiento, debe ver el origen de la página.

1. En AEM, edite una página basada en la plantilla en la que [ha activado la entrega de imágenes optimizadas para la web](#activating) para el componente de imagen.
1. En el editor de páginas, seleccione el botón **Información de la página** en la parte superior izquierda y, luego, **Ver tal y como aparece publicado**.
1. Con las herramientas para desarrolladores de navegadores, vea el origen de la página y cómo el marcado procesado sigue siendo el mismo, pero la imagen del atributo `src` señala a [la URL del nuevo servicio de imagen.](#activating)

## Cuando la entrega de imágenes optimizadas para la web no está disponible {#fallback}

La entrega de imágenes optimizadas para la web solo está disponible en AEM as a Cloud Service. En los casos en los que no está disponible, como ejecutar AEM 6.5 en las instalaciones o en una instancia de desarrollo local, la entrega de imágenes vuelve a utilizar [el servlet de imagen adaptable.](/help/developing/adaptive-image-servlet.md)

Al igual que habilitar la entrega de imágenes optimizadas para la web no afecta al marcado, volver al servlet de imagen adaptable tampoco tiene ningún efecto en él, ya que solo la URL del atributo `src` del elemento `img` se cambia.

## Preguntas más frecuentes {#faq}

### ¿Por qué no existe ninguna opción para habilitar imágenes optimizadas para la web en mi entorno? {#missing-option}

La funcionalidad solo está disponible en AEM as a Cloud Service. Al ejecutar AEM localmente o en las instalaciones, el componente de imagen [vuelve](#fallback) a utilizar el servlet de imagen adaptable.

### ¿Por qué el servicio no funciona con el SDK local? {#local-sdk}

Al utilizar el SDK de AEM en `localhost`, el servicio de imágenes no está disponible y el procesamiento de imágenes [vuelve](#fallback) a utilizar el servlet de imagen adaptable.

Para utilizar el servicio de entrega de imágenes optimizadas para la web, implemente el proyecto en un entorno de desarrollo de AEMaaCS para poder probar con precisión cómo se comporta el servicio de imágenes con el servicio de imágenes.

### ¿Por qué el servicio no funciona para algunas imágenes en mi página? {#some-images}

El servicio de imágenes solo funciona para recursos ubicados en `/content/dam` y no servirá con imágenes cargadas directamente en la página y almacenadas en un objeto `cq:Page`. Estos recursos se entregarán con el servlet de imagen adaptable como [reserva.](#fallback)

### ¿Por qué el servicio muestra una imagen de peor calidad o limita el tamaño de las imágenes? {#quality}

El servicio de imágenes optimizadas para la web considera todas las representaciones de imágenes de 2048 px y más pequeñas y elige la mayor de ellas como base para aplicar la configuración solicitada (anchura, recorte, formato, calidad, etc.).

El servicio de imágenes nunca aumenta el tamaño de las imágenes. Por lo tanto, estas representaciones definen el mejor tamaño y la mejor calidad que el servicio de imágenes podrá ofrecer. Así, asegúrese de que todos los recursos tengan la representación de Zoom 2048 px y, si no la tienen, vuelva a procesarlos.

### La URL de mis imágenes sigue terminando con .JPG o .PNG, no con .WEBP, y no hay ningún atributo SRCSET o elemento PICTURE. ¿Realmente se utilizan formatos web optimizados? {#content-negotiation}

Para ofrecer formatos WebP, el servicio de entrega de imágenes optimizadas para la web utiliza una técnica denominada “negociación de contenido”. Esto consiste en devolver un formato de archivo WebP, incluso cuando se solicita una extensión de archivo JPG o PNG, pero solo cuando el explorador que emite la solicitud ha proporcionado un encabezado de aceptación HTTP `image/webp`. Los navegadores que admitan esta técnica pueden facilitar este encabezado, mientras que los más antiguos seguirán teniendo el formato de archivo JPG o PNG.

La ventaja de esta técnica es que el elemento `img` y sus atributos pueden seguir siendo los mismos, lo que dará como resultado una compatibilidad óptima para los sitios existentes y garantizará la ruta más fluida posible a la transición hacia la entrega de imágenes optimizadas para la web.

### ¿Puedo utilizar la entrega de imágenes optimizadas para la web con mi propio componente?

Sí, los componentes personalizados, creados por, pueden utilizar el servicio de entrega de imágenes optimizadas para la web [ampliación del componente de imagen,](/help/developing/customizing.md)

A continuación se muestra una interfaz de servicio que se puede utilizar para ayudar a generar la URL del recurso.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Las incrustaciones de URL directas en una experiencia que no se crea mediante los componentes principales que se ejecutan en AEM Sites CS infringen los términos de licencia de Media Library.

### ¿Cuál es la URL de una imagen entregada por el nuevo servicio de imágenes? {#url}

Consulte la sección anterior, [Activación de la entrega de imágenes optimizadas para la web para componentes principales](#activating), para ver un ejemplo de URL y expresión regular.

### ¿Pueden las imágenes no mostrarse después de habilitar las imágenes optimizadas para la web?

No, esto nunca debería suceder.

* En el HTML, el marcado no cambia al habilitar imágenes optimizadas para web, solo cambia el valor del atributo SRC del elemento de imagen.
* Cuando el nuevo servicio de imagen no esté disponible o no pueda procesar la imagen deseada, la URL generada [volverá a usar el servlet de imagen adaptable.](#fallback)
* Las reglas de Dispatcher pueden bloquear el servicio de imágenes optimizadas para la web y [deben comprobarse al activar la funcionalidad.](#activating)
