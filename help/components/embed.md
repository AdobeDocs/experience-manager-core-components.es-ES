---
title: Incrustar componente
description: El componente incrustado permite incrustar contenido externo en una página de contenido de AEM.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Incrustar componente {#embed-component}

El componente de incrustación de componentes principales permite incrustar contenido externo en una página de contenido de AEM.

{{traditional-aem}}

## Uso {#usage}

El componente incrustado de componente principal permite que el autor de contenido defina el contenido externo seleccionado para que se incruste en una página de contenido de AEM. Además, existe la opción de definir el HTML de forma libre que se va a incrustar.

* Las propiedades del componente se pueden definir en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente se pueden definir en el [cuadro de diálogo de diseño](#design-dialog) al agregarlo a una página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente incrustado es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](v1/embed.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente incrustado, ver ejemplos de sus opciones de configuración y la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_embed_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente incrustado [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_embed_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el recurso externo que se va a incrustar en la página.

### Pestaña Propiedades {#properties-tab}

Primero elija qué tipo de recurso debe incrustar:

* [URL](#url)
* [Incrustable](#embeddable)
* [HTML](#html)

Para cada tipo de incrustable, puede definir un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

#### URL {#url}

La incrustación más sencilla es la URL. Simplemente pegue la dirección URL del recurso que desea incrustar en el campo **URL**. El componente intentará acceder al recurso y, si uno de los procesadores lo puede representar, se mostrará un mensaje de confirmación debajo del campo **URL**. Si no es así, el campo se marcará con un error.

El componente incrustado se enviará con procesadores para los siguientes tipos de recursos:

* Recursos que cumplen con el [Estándar de oEmbed](https://oembed.com/), incluidos Facebook Post, Instagram, SoundCloud, Twitter y YouTube
* Pinterest

Los desarrolladores pueden agregar procesadores de URL adicionales [siguiendo la documentación para desarrolladores de componentes incrustados.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Cuadro de diálogo de edición del componente incrustado para la dirección URL](/help/assets/embed-url.png)

#### Incrustable {#embeddable}

Las incrustaciones permiten una mayor personalización del recurso incrustado, que se puede parametrizar e incluir información adicional. Un autor puede elegir entre incrustaciones de confianza preconfiguradas y el componente se enviará con una incrustación de YouTube lista para usar.

El campo **Incrustable** define el tipo de procesador que desea utilizar. En el caso de YouTube incrustable, puede definir:

* **ID de vídeo**: el ID exclusivo del vídeo de YouTube del recurso que desea incrustar
* **Anchura**: la anchura del vídeo incrustado
* **Altura**: altura del vídeo incrustado
* **Habilitar silenciar**: este parámetro especifica si el vídeo se reproducirá silenciado de forma predeterminada. Habilitar esto aumenta las posibilidades de que la reproducción automática funcione en exploradores modernos.
* **Habilitar la reproducción automática**: este parámetro especifica si el vídeo inicial comenzará a reproducirse automáticamente cuando se cargue el reproductor. Esto solo es efectivo en la instancia de publicación o al utilizar la opción **Ver como publicado** en la instancia de creación.
* **Habilitar reproducción en bucle**: en el caso de un solo vídeo, este parámetro especifica si el reproductor debe reproducir repetidamente el vídeo inicial. En el caso de una lista de reproducción, el reproductor reproduce la lista de reproducción completa y, a continuación, comienza de nuevo con el primer vídeo.
* **Habilitar la reproducción en línea (iOS)**: este parámetro controla si los vídeos se reproducen en línea (activado) o a pantalla completa (desactivado) en un reproductor HTML5 en iOS.
* **Vídeos relacionados sin restricciones**: si esta opción está desactivada, los vídeos relacionados provendrán del mismo canal que el vídeo que acaba de reproducirse; de lo contrario, provendrán de cualquier canal.

Otros incrustables ofrecerían campos similares y los puede definir un desarrollador [siguiendo la documentación para desarrolladores de componentes incrustados.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Cuadro de diálogo de edición del componente incrustado para incrustables](/help/assets/embed-embeddable.png)

>[!NOTE]
>
>Los incrustables deben habilitarse en el nivel de plantilla mediante el [Cuadro de diálogo de diseño](#design-dialog) para que estén disponibles para el autor de la página.

#### HTML {#html}

Puede agregar HTML de forma libre a la página mediante el componente Incrustar.

![Cuadro de diálogo de edición del componente incrustado para la dirección HTML](/help/assets/embed-html.png)

>[!NOTE]
>Las etiquetas no seguras, como los scripts, se filtrarán del HTML introducido y no se procesarán en la página resultante.

##### Seguridad {#security}

El marcado HTML que puede introducir el autor se filtra con fines de seguridad para evitar ataques de scripts entre sitios que podrían, por ejemplo, permitir a los autores obtener derechos administrativos.

En general, todos los scripts y elementos `style`, así como todos los `on*` y atributos `style` se eliminarán de la salida.

Sin embargo, las reglas son más complicadas porque el componente Incrustar sigue el conjunto de reglas de filtrado del marco global de saneamiento HTML AntiSamy de AEM, que se puede encontrar en `/libs/cq/xssprotection/config.xml`. Un desarrollador puede superponer esta configuración para un proyecto específico si fuera necesario.

Puede encontrar información de seguridad adicional en la [documentación para desarrolladores para instalaciones en línea de AEM](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html?lang=es), así como [instalaciones de AEM Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html?lang=es)

>[!NOTE]
>
>Aunque las reglas del marco de saneamiento AntiSamy se pueden configurar superponiendo `/libs/cq/xssprotection/config.xml`, estos cambios afectarán a todo el comportamiento de HTL y JSP y no solo al componente principal incrustado.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Incrustado](/help/assets/embed-styles.png)

El componente Incrustado es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor de contenido que utiliza el componente incrustado y los valores predeterminados establecidos al colocar el componente incrustado.

### Pestaña Tipos incrustables {#embeddable-types-tab}

![Cuadro de diálogo de diseño del componente incrustado](/help/assets/embed-design.png)

* **Deshabilitar URL**: deshabilita la opción **URL** para el autor de contenido cuando se selecciona
* **Deshabilitar incrustables**: desactiva la opción **Incrustable** para el autor de contenido cuando se selecciona, independientemente de qué procesadores se admitan.
* **Deshabilitar HTML**: deshabilita la opción **HTML** para el autor de contenido cuando está seleccionada.
* **Incrustables permitidos**: permite seleccionar varios procesadores que definen qué procesadores incrustables están disponibles para el autor de contenido, siempre que la opción **Incrustable** esté activa.

### Pestaña YouTube {#youtube-tab}

![Pestaña YouTube del cuadro de diálogo de diseño del componente incrustado](/help/assets/embed-design-youtube.png)

* **Permitir la configuración del comportamiento silencioso**: permite al autor de contenido configurar la opción **Habilitar silencio** en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de silenciar**: establece automáticamente la opción **Habilitar silencio** cuando se selecciona el tipo incrustado de YouTube
* **Permitir la configuración del comportamiento de reproducción automática**: permite al autor de contenido configurar la opción **Habilitar reproducción automática** en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de reproducción automática**: establece automáticamente la opción **Habilitar reproducción automática** cuando se selecciona el tipo incrustado de YouTube
* **Permitir la configuración del comportamiento de la reproducción en bucle**: permite al autor de contenido configurar la opción **Habilitar reproducción en bucle** en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de reproducción en bucle**: establece automáticamente **Habilitar reproducción en bucle** cuando se selecciona el tipo incrustado de YouTube
* **Permitir la configuración de reproducción en línea (iOS)**: permite al autor de contenido configurar la opción **Habilitar reproducción en línea (iOS)** en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de reproducción en línea (iOS)**: establece automáticamente la opción **Habilitar reproducción en línea (iOS)** cuando se selecciona el tipo incrustado de YouTube
* **Permitir la configuración de vídeos en línea**: permite al autor de contenido configurar la opción **Vídeos relacionados sin restricciones** en el componente cuando se selecciona el tipo incrustado de YouTube
   * **Valor predeterminado de vídeos relacionados sin restricciones**: establece automáticamente la opción **Vídeos relacionados sin restricciones** cuando se selecciona el tipo incrustado de YouTube
