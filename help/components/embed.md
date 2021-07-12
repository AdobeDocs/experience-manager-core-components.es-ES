---
title: Incrustar componente
description: El componente incrustado permite incrustar contenido externo en una página de contenido AEM.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 2%

---

# Incrustar componente{#embed-component}

El componente de incrustación de componentes principales permite incrustar contenido externo en una página de contenido AEM.

## Uso {#usage}

El componente incrustado de componente principal permite que el autor de contenido defina el contenido externo seleccionado para que se incruste en una página de contenido AEM. Además, existe la opción de definir el HTML de forma libre que se va a incrustar.

* Las propiedades del componente se pueden definir en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente al agregarlo a una página se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente incrustado es v1, que se introdujo con la versión 2.7.0 de los componentes principales en septiembre de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente incrustado , así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_embed).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente incrustado [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo configurar permite al autor del contenido definir el recurso externo que se va a incrustar en la página. Primero elija qué tipo de recurso debe incrustar:

* [URL](#url)
* [Insertable](#embeddable)
* [HTML](#html)

Para cada tipo de incrustable, puede definir el **ID** de la publicidad. Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

### URL {#url}

La incrustación más sencilla es la URL. Simplemente pegue la dirección URL del recurso que desea incrustar en el campo **URL**. El componente intentará acceder al recurso y, si uno de los procesadores lo puede representar, mostrará un mensaje de confirmación debajo del campo **URL**. Si no es así, el campo se marcará con un error.

El componente incrustado se envía con procesadores para los siguientes tipos de recursos:

* Recursos que cumplen con el [oEmbed standard](https://oembed.com/), incluidos Facebook Post, Instagram, SoundCloud, Twitter y YouTube
* Pinterest

Los desarrolladores pueden agregar procesadores de URL adicionales [siguiendo la documentación para desarrolladores del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Cuadro de diálogo de edición del componente incrustado para la dirección URL](/help/assets/embed-url.png)

### Insertable {#embeddable}

Las incrustaciones permiten una mayor personalización del recurso incrustado, que se puede parametrizar e incluir información adicional. Un autor puede seleccionar entre incrustaciones de confianza preconfiguradas y el componente se envía con una incrustación de YouTube lista para usar.

El campo **Incrustable** define el tipo de procesador que desea utilizar. En el caso de YouTube incrustado, puede definir:

* **ID de vídeo** : el ID de vídeo exclusivo de YouTube del recurso que desea incrustar.
* **Anchura** : la anchura del vídeo incrustado
* **Altura** : altura del vídeo incrustado
* **Habilitar Silenciar** : este parámetro especifica si el vídeo se reproducirá silenciado de forma predeterminada. Habilitar esto aumenta las posibilidades de que la reproducción automática funcione en exploradores modernos.
* **Habilitar reproducción automática** : este parámetro especifica si el vídeo inicial empezará a reproducirse automáticamente cuando se cargue el reproductor. Esto solo es efectivo en la instancia de publicación o al utilizar la opción **Ver como publicado** en la instancia de creación.
* **Habilitar bucle** : en el caso de un solo vídeo, este parámetro especifica si el reproductor debe reproducir repetidamente el vídeo inicial. En el caso de una lista de reproducción, el reproductor reproduce la lista de reproducción completa y, a continuación, comienza de nuevo en el primer vídeo.
* **Habilitar reproducción en línea (iOS)** : este parámetro controla si los vídeos se reproducen en línea (activado) o en pantalla completa (desactivado) en un reproductor HTML5 en iOS.
* **Vídeos relacionados sin restricciones** : si esta opción está desactivada, los vídeos relacionados provendrán del mismo canal que el vídeo que acaba de reproducirse; de lo contrario, provendrán de cualquier canal.

Tenga en cuenta que las opciones &quot;habilitar&quot; deben activarse a través del [Diálogo de diseño](#design-dialog) y pueden establecerse como valores predeterminados.

Otros incrustables ofrecerían campos similares y los puede definir un desarrollador [siguiendo la documentación para desarrolladores del componente incrustado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Cuadro de diálogo de edición del componente incrustado para incrustables](/help/assets/embed-embeddable.png)

>[!NOTE]
>Los incrustables deben habilitarse en el nivel de plantilla mediante el [Diálogo de diseño](#design-dialog) para que estén disponibles para el autor de la página.

### HTML {#html}

Puede agregar HTML de forma libre a la página mediante el componente Insertar.

![Cuadro de diálogo de edición del componente incrustado para HTML](/help/assets/embed-html.png)

>[!NOTE]
>Las etiquetas no seguras, como las secuencias de comandos, se filtrarán del HTML introducido y no se procesarán en la página resultante.

#### Seguridad {#security}

El marcado HTML que puede introducir el autor se filtra con fines de seguridad para evitar ataques de scripts entre sitios que podrían, por ejemplo, permitir a los autores obtener derechos administrativos.

*En general,* todas las secuencias de comandos y  `style` elementos, así como todos  `on*` los  `style` atributos y se eliminarán de la salida.

Sin embargo, las reglas son más complicadas porque el componente incrustado sigue AEM conjunto de reglas de filtrado del marco de saneamiento HTML AntiSamy global, que se puede encontrar en `/libs/cq/xssprotection/config.xml`. Un desarrollador puede superponer esta configuración para un proyecto específico si es necesario.

Puede encontrar información de seguridad adicional en la [AEM documentación para desarrolladores para instalaciones in situ](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html), así como [AEM como instalaciones de Cloud Service.](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Aunque las reglas del marco de saneamiento AntiSamy se pueden configurar superponiendo `/libs/cq/xssprotection/config.xml`, estos cambios afectan a todo el comportamiento de HTL y JSP y no solo al componente principal incrustado.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor de contenido que utiliza el componente incrustado y los valores predeterminados establecidos al colocar el componente incrustado.

### Ficha Tipos incrustables {#embeddable-types-tab}

![Cuadro de diálogo de diseño del componente incrustado](/help/assets/embed-design.png)

* **Deshabilitar URL** : deshabilita la  **** opción URL para el autor de contenido cuando se selecciona
* **Deshabilitar incrustables** : desactiva la  **** opción Incrustar para el autor de contenido cuando se selecciona, independientemente de qué procesadores se admiten.
* **Desactivar HTML** : deshabilita la opción  **** HTML para el autor de contenido cuando está seleccionada.
* **Incrustables permitidos** : permite seleccionar varios procesadores que definen qué procesadores incrustables están disponibles para el autor de contenido, siempre que la opción  **** Incrustar esté activa.

### Ficha YouTube {#youtube-tab}

![Ficha YouTube del cuadro de diálogo de diseño del componente incrustado](/help/assets/embed-design-youtube.png)

* **Permitir configuración del comportamiento silencioso** : permite al autor de contenido configurar la opción  **Habilitar** silenciamiento en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de silenciar** : establece automáticamente  **Enable** Silteoption cuando se selecciona el tipo incrustado de YouTube
* **Permitir configuración del comportamiento de reproducción automática** : permite al autor de contenido configurar la opción  **Habilitar reproducción** automática en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de reproducción automática** : establece automáticamente la opción  **Habilitar reproducción** automática cuando se selecciona el tipo incrustado de YouTube
* **Permitir configuración del comportamiento del bucle** : permite al autor de contenido configurar el  **Enable** Lopotion en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de bucle** : establece automáticamente  **Enable** Lopotion cuando se selecciona el tipo incrustado de YouTube
* **Permitir configuración de reproducción en línea (iOS)** : permite al autor de contenido configurar la opción  **Habilitar reproducción en línea (iOS)**  en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de reproducción en línea (iOS)** : establece automáticamente la opción  **Habilitar reproducción en línea (iOS)**  cuando se selecciona el tipo incrustado de YouTube
* **Permitir configuración de vídeos**  en línea: permite al autor de contenido configurar la opción  **Vídeos relacionados** sin restricciones en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de vídeos**  relacionados no restringidos: establece automáticamente la opción  **Vídeos relacionados no restringidos** cuando se selecciona el tipo incrustado de YouTube
