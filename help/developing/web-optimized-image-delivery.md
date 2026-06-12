---
title: Entrega de imágenes optimizadas para la web
description: Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para la web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.
role: Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
TQID: https://experienceleague.adobe.com/fJgZlABQW0no-vH0tOjLy20ykqPhjopcvY7ei-iqi9M
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: c124fa01-25c5-42ec-adf6-21d1c114058b
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
  - id: f2d27a5f-0d67-4d85-8a24-86a8d8a3574b
subfeature_v2:
  - id: a6c0bfb4-91d0-4952-9c1d-c7f39e7705c4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 100%

---

# Entrega de imágenes optimizadas para la web {#web-optimized-image-delivery}

Descubra cómo los componentes principales pueden aprovechar las funciones de entrega de imágenes optimizadas para la web de AEM as a Cloud Service para ofrecer imágenes de forma más eficaz.

## Información general {#overview}

La función de entrega de imágenes optimizadas para la web de AEM as a Cloud Service ofrece recursos de imagen de DAM en [formato WebP.](https://developers.google.com/speed/webp) WebP puede reducir el tamaño de descarga de una imagen en aproximadamente un 25 % en promedio, lo que resulta en una carga de página más rápida.

La activación de la entrega de imágenes optimizadas para la web en los componentes principales es sencilla y, como todos los exploradores comunes admiten WebP, la experiencia es transparente para el usuario final. La única diferencia que notará es que el contenido se carga más rápido.

## Activación de la entrega de imágenes optimizadas para la web para componentes principales {#activating}

Para activar la entrega de imágenes optimizadas para la web, edite una plantilla de página y simplemente active la opción **Habilitar imágenes optimizadas para web** dentro del cuadro de diálogo de diseño del [componente de imagen.](/help/components/image.md#design-dialog) Esta opción está disponible para las versiones 1, 2 y 3 del componente de imagen.

Si no conoce los cuadros de diálogo de diseño y las plantillas de página de AEM, [revise este documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Habilitación de la entrega de imágenes optimizadas para la web en el cuadro de diálogo de diseño](/help/assets/web-optimized-image-delivery.png)

Eso es todo. El componente de imagen ahora entrega las imágenes en formato WebP.

Una vez que se activa la entrega de imágenes optimizadas para la web, es posible que se desee comprobar la configuración de Dispatcher para verificar que no bloquee la solicitud al servicio de entrega de imágenes. Consulte [esta entrada de Preguntas más frecuentes](#failure-to-deliver) para obtener más información.

## Verificación de la entrega de WebP {#verifying}

La entrega de imágenes optimizadas para la web es transparente para el consumidor del contenido. Lo único que notará un usuario final es un tiempo de carga más rápido. Por lo tanto, para observar cualquier cambio real de comportamiento, debe comprobar el tipo de contenido de las imágenes procesadas en el explorador. Todos los exploradores modernos admiten WebP. Puede hacer referencia a [este sitio](https://caniuse.com/webp) para obtener más información sobre la compatibilidad del explorador.

1. En AEM, edite una página basada en la plantilla en la que [ha activado la entrega de imágenes optimizadas para la web](#activating) para el componente de imagen.
1. En el editor de páginas, seleccione el botón **Información de la página** en la parte superior izquierda y, luego, **Ver tal y como aparece publicado**.
1. Abra las herramientas para desarrolladores del explorador y seleccione la pestaña de red.
1. Vuelva a cargar la página, busque solicitudes HTTP que carguen las imágenes y compruebe el tipo de contenido de la imagen que recibió el explorador.

## Cuando la entrega de imágenes optimizadas para la web no está disponible {#fallback}

La entrega de imágenes optimizadas para la web solo está disponible en AEM as a Cloud Service. En los casos en los que no está disponible, como ejecutar AEM 6.5 en las instalaciones o en una instancia de desarrollo local, la entrega de imágenes vuelve a utilizar [el servlet de imagen adaptable.](/help/developing/adaptive-image-servlet.md)

Al volver al servlet de imagen adaptable, se cambia el atributo `src` de los elementos de `img` en el origen de la página.

## Preguntas más frecuentes {#faq}

### ¿Por qué no existe ninguna opción para habilitar imágenes optimizadas para la web en mi entorno? {#missing-option}

La funcionalidad solo está disponible en AEM as a Cloud Service. Al ejecutar AEM localmente o en las instalaciones, el componente de imagen [vuelve](#fallback) a utilizar el servlet de imagen adaptable.

### ¿Por qué el servicio no funciona con el SDK local? {#local-sdk}

Al utilizar el SDK de AEM en `localhost`, el servicio de imágenes no está disponible y el procesamiento de imágenes [vuelve](#fallback) a utilizar el servlet de imagen adaptable.

Para utilizar el servicio de entrega de imágenes optimizadas para la web, implemente el proyecto en un entorno de desarrollo de AEMaaCS para poder probar con precisión cómo se comporta el servicio de imágenes con el servicio de imágenes.

### ¿Por qué el servicio no funciona para algunas imágenes en mi página? {#some-images}

El servicio de imágenes solo funciona para recursos ubicados en `/content/dam` y no servirá con imágenes cargadas directamente en la página y almacenadas en un objeto `cq:Page`. Estos recursos se entregarán con el servlet de imagen adaptable como [reserva.](#fallback)

### ¿Por qué el servicio muestra una imagen de peor calidad o limita el tamaño de las imágenes? {#quality}

Cuando los recursos de imagen en `/content/dam` se procesan, los entornos de AEM as a Cloud Service generan representaciones optimizadas de diferentes dimensiones. El servicio de imágenes optimizadas para la web analiza la anchura solicitada por el componente principal de imagen, considera la imagen original y todas las representaciones de 2048 px y más pequeñas, y elige la mayor de ellas (dentro de los límites de tamaño y dimensión que puede gestionar el servicio de imágenes, actualmente de 50 MB y `12k`x`12k`) como base para aplicar la configuración solicitada (anchura, recorte, formato, calidad, etc.).

Para conservar la fidelidad de la salida, el servicio de imágenes no aumenta el tamaño de las imágenes. Las representaciones anteriores definen la mejor calidad que el servicio de imágenes podrá ofrecer. Dado que a menudo no puede influir en el tamaño o las dimensiones del recurso de imagen original, asegúrese de que todos los recursos de imagen tengan una representación de zoom de 2048 px y, si no la tienen, vuelva a procesarlos.

### La URL de mis imágenes sigue terminando con .JPG o .PNG, no con .WEBP, y no hay ningún atributo SRCSET o elemento PICTURE. ¿Realmente se utilizan formatos web optimizados? {#content-negotiation}

Para ofrecer formatos WebP, el servicio de entrega de imágenes optimizadas para web lleva a cabo una [negociación de contenido dirigida por el servidor.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Esto ayuda a seleccionar el formato de salida óptimo para la imagen en función de las capacidades anunciadas por el cliente, lo que permite que el servicio de entrega de imágenes ignore la extensión del archivo.

La ventaja de aprovechar la negociación de contenido es que los exploradores que no anuncian la compatibilidad con WebP seguirán teniendo el formato de archivo JPG o PNG sin ningún cambio necesario en el marcado de la página. Esto ofrece una compatibilidad óptima para los sitios existentes y garantiza la ruta más fluida posible a la transición hacia la entrega de imágenes optimizadas para la web.

### ¿Puedo utilizar la entrega de imágenes optimizadas para la web con mi propio componente?

Sí, los componentes personalizados pueden utilizar el servicio de envío de imágenes optimizadas para la web, que se generan al [ampliar el componente de imagen,](/help/developing/customizing.md)

A continuación se muestra una interfaz de servicio que se puede utilizar para ayudar a generar la URL del recurso.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Las incrustaciones de URL directas en una experiencia que no se haya creado mediante la SPI mencionada anteriormente (disponible en sitios AEM as a Cloud Service) infringen las [Condiciones de uso de Media Library](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=es#use-media-library).

### ¿Pueden las imágenes no mostrarse después de habilitar las imágenes optimizadas para la web? {#failure-to-deliver}

No, esto nunca debería suceder por las siguientes razones.

* En el HTML, el marcado no cambia al habilitar imágenes optimizadas para web, solo cambia el valor del atributo `src` del elemento de imagen.
* Cuando el nuevo servicio de imagen no esté disponible o no pueda procesar la imagen deseada, la URL generada [volverá a usar el servlet de imagen adaptable.](#fallback)

Sin embargo, las reglas de Dispatcher pueden bloquear el servicio de entrega de imágenes optimizadas para la web. Las URL del servicio de entrega de imágenes comienzan con `/adobe`, y examinar los registros de Dispatcher para solicitudes rechazadas como [descrito aquí](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html?lang=es#filter-rejects) debería ayudar a solucionar los errores que se hayan encontrado al entregar las imágenes al explorador.
