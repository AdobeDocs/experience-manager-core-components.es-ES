---
title: Entrega de imágenes optimizada para la Web
description: Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.
role: Architect, Developer, Admin, User
source-git-commit: 20436ffb5d6a6346738be1e6f5e6e2e8a68e76c9
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---


# Entrega de imágenes optimizada para la Web {#web-optimized-image-delivery}

Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.

>[!NOTE]
>
>El servicio de entrega de imágenes optimizado para la web es una función de prelanzamiento, con la versión de junio de 2022 de AEM as a Cloud Service con GA prevista para julio.
>
>Para obtener más información sobre las funciones de la versión preliminar de AEMaaCS, consulte el documento [Canal de prelanzamiento de Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=es)

##  Información general {#overview}

La función de entrega de imágenes optimizada para la web de AEM as a Cloud Service ofrece recursos de imagen desde DAM en [formato WebP.](https://developers.google.com/speed/webp) WebP puede reducir el tamaño de descarga de una imagen en aproximadamente un 25% en promedio, lo que resulta en una carga de página más rápida.

La activación de la entrega de imágenes optimizada para la web en los componentes principales es sencilla y, como todos los navegadores comunes admiten WebP, la experiencia es transparente para el usuario final. La única diferencia que notarán es que el contenido se carga más rápido!

## Activación de la entrega de imágenes optimizadas para la Web para componentes principales {#activating}

Para activar la entrega de imágenes optimizada para la web, edite una plantilla de página y simplemente active la opción **Habilitar imágenes optimizadas para web** dentro del cuadro de diálogo de diseño de la variable [Componente de imagen.](/help/components/image.md#design-dialog) Esta opción está disponible para las versiones 1, 2 y 3 del componente de imagen.

Si no está familiarizado con los cuadros de diálogo de diseño y AEM plantillas de página, [revise este documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Habilitación de la entrega de imágenes optimizada para la Web en el cuadro de diálogo de diseño](/help/assets/web-optimized-image-delivery.png)

¡Eso es todo! El componente Imagen ahora entrega las imágenes en formato WebP.

Una vez que se activa la entrega de imágenes optimizada para la web, es posible que también se desee comprobar la configuración de Dispatcher para verificar que no bloquee la solicitud al servicio de imágenes. Las direcciones URL de este servicio toman el siguiente formulario.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Esto se puede generalizar con esta expresión regular.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Verificación de la entrega de WebP {#verifying}

La entrega de imágenes optimizada para la web es transparente para el consumidor del contenido y no afecta al marcado. Lo único que notará un usuario final es un tiempo de carga más rápido.

Por lo tanto, para observar el cambio real de comportamiento, debe ver el origen de la página.

1. En AEM, edite una página basada en la plantilla en la que [entrega de imágenes optimizada para la web activada](#activating) para el componente de imagen.
1. En el editor de páginas, seleccione la opción **Información de la página** en la parte superior izquierda y, a continuación, **Ver tal y como aparece publicado**.
1. Con las herramientas para desarrolladores de navegadores, vea el origen de la página y vea cómo el marcado procesado sigue siendo el mismo, pero que la imagen en la `src` señala a [la URL del nuevo servicio de imagen.](#activating)

## Cuando el envío de imágenes optimizadas para web no está disponible {#fallback}

La entrega de imágenes optimizada para web solo está disponible en AEM as a Cloud Service. En los casos en los que no está disponible, como ejecutar AEM 6.5 in situ o en una instancia de desarrollo local, la entrega de imágenes vuelve a utilizar [el servlet de imagen adaptable.](/help/developing/adaptive-image-servlet.md)

Al igual que habilitar la entrega de imágenes optimizada para la web no afecta al marcado, volver al servlet de imagen adaptable tampoco tiene ningún efecto en el marcado, ya que solo la URL de la variable `src` del `img` se cambia.

## Preguntas más frecuentes {#faq}

### ¿Por qué no existe esa opción para habilitar imágenes optimizadas para la web en mi entorno? {#missing-option}

La función solo está disponible en AEM as a Cloud Service. Ejecución local o local AEM el componente de imagen [vuelve](#fallback) para utilizar el servlet de imagen adaptable.

### ¿Por qué el servicio no funciona con el SDK local? {#local-sdk}

Al utilizar el SDK de AEM en `localhost`, el servicio de imágenes no está disponible y la renderización de imágenes [vuelve](#fallback) para utilizar el servlet de imagen adaptable.

Para utilizar el servicio de entrega de imágenes optimizado para la web, implemente el proyecto en un entorno de desarrollo AEMaaCS para poder probar con precisión cómo se comporta el servicio de imágenes con el servicio de imágenes.

### ¿Por qué el servicio no funciona para algunas imágenes en mi página? {#some-images}

El servicio de imágenes solo funciona para recursos ubicados en `/content/dam` y no funcionará con imágenes cargadas directamente en la página y almacenadas en un `cq:Page` objeto. Estos recursos se entregarán con el servlet de imagen adaptable como un [reserva.](#fallback)

### ¿Por qué el servicio muestra una imagen de peor calidad o limita el tamaño de las imágenes? {#quality}

El servicio de imágenes optimizado para la web considera todas las representaciones de imágenes de 2048 px y más pequeñas y elige la mayor de ellas como base para aplicar la configuración solicitada (ancho, recorte, formato, calidad, etc.).

El servicio de imágenes nunca aumentará el tamaño de las imágenes. Por lo tanto, estas representaciones definen el mejor tamaño y la mejor calidad que el servicio de imágenes podrá ofrecer. Por lo tanto, asegúrese de que todos los recursos tengan la representación de zoom 2048px y, si no lo tienen, vuelva a procesarlos.

### La URL de mis imágenes sigue terminando con .JPG o .PNG, no con .WEBP, y no hay ningún atributo SRCSET o elemento PICTURE. ¿Realmente se utilizan formatos web optimizados? {#content-negotiation}

Para ofrecer formatos WebP, el servicio de entrega de imágenes optimizado para la web utiliza una técnica denominada &quot;negociación de contenido&quot;. Esto consiste en devolver un formato de archivo WebP, incluso cuando se solicita un JPG o una extensión de archivo PNG, pero solo cuando el explorador que realiza la solicitud proporcionó un `image/webp` Encabezado de aceptación HTTP. Los navegadores que admitan esta técnica pueden proporcionar este encabezado, mientras que los navegadores más antiguos seguirán teniendo el formato de archivo JPG o PNG.

La ventaja de esta técnica es que la variable `img` y sus atributos pueden seguir siendo los mismos, lo que dará como resultado una compatibilidad óptima para los sitios existentes y garantizará la ruta más fluida posible a la transición hacia la entrega de imágenes optimizada para la web.

### ¿Puedo utilizar la entrega de imágenes optimizada para la web con mi propio componente?

Sí, los componentes personalizados pueden utilizar el servicio de entrega de imágenes optimizado para la web. Recomendaciones de Adobe [ampliación del componente de imagen](/help/developing/customizing.md) en este caso.

A continuación se muestra una interfaz de servicio que se puede utilizar para ayudar a generar la URL del recurso.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

Este servicio toma un recurso de recurso como primer parámetro obligatorio y puede tomar un mapa opcional de las transformaciones de imagen deseadas que se van a aplicar y que pueden contener los siguientes parámetros.

* `path` - El ID del recurso que se va a enviar debe ser de patrón `([^:\[\]\|\*\/]+)` (por ejemplo: `unicorn–1234`)
* `seoname` - El nombre definido por el usuario, centrado en SEO, que se anexará a la dirección URL de la imagen, puede contener guiones, debe ser de patrón `([\w-]+)` (por ejemplo: `my-friend-the-unicorn`)
* `format` - El formato de imagen deseado, puede ser `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (por ejemplo: `webp`)
* `preferwebp` - Si es posible, envíe la salida WebP, ignorando el `format` parámetro ([consulte preguntas frecuentes sobre negociación de contenido](#content-negotiation)), booleano (por ejemplo: `true`)
* `width` - La resolución de imagen deseada en píxeles debe ser buena a 1 (p. ej.: `400`)
* `quality` - La compresión deseada, entre `1` y `100` (por ejemplo: `75`)
* `c` - Coordenadas de recorte de imagen deseadas, valores de píxeles separados por coma (p. ej.: `100,100,400,200`)
* `r` - La rotación de imagen deseada puede ser `90`, `180`, `270` (por ejemplo: `90`)
* `flip` - El volteado de imagen deseado, puede ser `h`, `v`, `hv` (por ejemplo: `h`)

### ¿Cuál es la URL de una imagen entregada por el nuevo servicio de imágenes? {#url}

Consulte la sección anterior [Activación de la entrega de imágenes optimizadas para la Web para componentes principales](#activating) para ver un ejemplo de URL y expresión regular.

### ¿Pueden las imágenes no mostrarse después de habilitar las imágenes optimizadas para la web?

No, esto nunca debería suceder.

* En el HTML, el marcado no cambia al habilitar imágenes optimizadas para web, solo cambia el valor del atributo SCR del elemento de imagen.
* Cuando el nuevo servicio de imagen no esté disponible o no pueda procesar la imagen deseada, la URL generada [alternativa al servlet de imagen adaptable.](#fallback)
* Las reglas de Dispatcher pueden bloquear el servicio de imagen optimizado para la web y [debe comprobarse al activar la función.](#activating)
