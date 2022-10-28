---
title: Componente de imagen de correo electrónico
description: El componente Imagen de correo electrónico es un componente de imagen adaptable que incluye la edición in situ.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 63%

---


# Componente de imagen de correo electrónico {#email-image-component}

El componente Imagen de correo electrónico es un componente de imagen adaptable que incluye la edición in situ.

## Uso {#usage}

El componente Imagen de correo electrónico incluye selección de imágenes adaptables y comportamiento interactivo con carga diferida para el visitante de la página, así como una ubicación y configuración de imágenes fáciles de arrastrar y soltar para el autor del contenido.

* El autor de la plantilla puede definir las anchuras de la imagen y la configuración adicional en el [cuadro de diálogo de diseño.](#design-dialog)
* El editor de contenido puede cargar o seleccionar activos en el [cuadro de diálogo de configuración.](#configure-dialog)

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Imagen de correo electrónico es v1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales de correo electrónico](/help/email/versions.md).

## Funciones adaptables {#responsive-features}

El componente Imagen de correo electrónico incluye funciones adaptables sólidas listas para usar. En el nivel de plantilla de página, se puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los anchos predeterminados del recurso de imagen. El componente Imagen de correo electrónico cargará automáticamente la anchura correcta para mostrarla según el tamaño de la ventana del explorador. A medida que cambia el tamaño de la ventana, el componente Imagen de correo electrónico carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente Imagen de correo electrónico ya está optimizado para cargar el contenido.

Además, el componente Imagen de correo electrónico admite la carga diferida para aplazar la carga del recurso de imagen real hasta que sea visible en el explorador, lo que aumenta la capacidad de respuesta del contenido.

>[!TIP]
>
>De forma predeterminada, el componente de imagen de correo electrónico funciona con el servlet de imagen adaptable. Consulte el documento [Servlet de imagen adaptable](#adaptive-image-servlet) para obtener más información sobre cómo funciona.

## Asistencia de Dynamic Media {#dynamic-media}

El componente Imagen de correo electrónico es compatible [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=es#dynamicmedia) activos. [Cuando están habilitadas,](#design-dialog) estas funciones permiten agregar recursos de imagen de Dynamic Media con tan solo arrastrar y soltar o mediante el explorador de recursos como lo haría con cualquier otra imagen. Además, también se admiten modificadores de imagen, ajustes preestablecidos de imagen y cultivos inteligentes.

Las experiencias de correo electrónico creadas con los componentes principales de correo electrónico pueden presentar funciones de imagen Dynamic Media enriquecidas, potentes, sólidas y de alto rendimiento con tecnología Sensei.

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente Imagen de correo electrónico .

* Se admiten las funciones de arrastrar y soltar un recurso SVG desde DAM y de cargar un archivo SVG cargado desde un sistema de archivos local.
* El archivo SVG original se transmite (las transformaciones se omiten).
* Para una imagen SVG, las “imágenes inteligentes” y los “tamaños inteligentes” se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través de `<img src=“path-to-component”>`. Esto evita que el explorador ejecute cualquier script incrustado en el archivo SVG.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Imagen de correo electrónico , así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_image)

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Imagen de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

El componente de imagen admite [microdatos schema.org.](https://schema.org)

## Cuadro de diálogo de configuración {#configure-dialog}

El componente Imagen de correo electrónico ofrece un cuadro de diálogo de configuración en el que la propia imagen se define junto con su descripción y propiedades básicas.

### Pestaña Recurso {#asset-tab}

![Pestaña Recurso del cuadro de diálogo de configuración del componente de imagen de correo electrónico](/help/email/assets/email-image-configure-asset.png)

* **Heredar imagen destacada de la página**: esta opción utiliza la [imagen destacada de la página vinculada](page.md) o la imagen destacada de la página actual si la imagen no está vinculada.

* **Texto alternativo para fines de accesibilidad**: este campo le permite definir una descripción de la imagen para los usuarios con deficiencias visuales.

   * **Heredar texto alternativo de la página**: esta opción utiliza la descripción alternativa del valor de recurso vinculado de los `dc:description` metadatos en DAM o de la página actual si no hay ningún recurso vinculado.

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic **Editar** a [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el Editor de recursos.

* **No proporcionar texto alternativo**: esta opción marca la imagen para que sea ignorada por las tecnologías de asistencia, como lectores de pantalla, en casos en los que la imagen es puramente decorativa o no transmite información adicional a la página.

* **Desactivación de la carga diferida** : Esta opción carga previamente todos los componentes de la imagen sin cargarla según sea necesario.

### Pestaña de metadatos {#metadata-tab}

![Pestaña de metadatos del cuadro de diálogo de configuración del componente de imagen](/help/email/assets/email-image-configure-metadata.png)

* **Tipo de ajuste preestablecido**: define los tipos de ajustes preestablecidos de imagen disponibles, ya sea **Ajustes preestablecidos de imágenes** o **Recorte inteligente**, y solo está disponible cuando las [funciones de Dynamic Media](#dynamic-meida) están habilitadas.
   * **Ajuste preestablecido de imagen** - When **Tipo de ajuste preestablecido** de **Ajuste preestablecido de imagen** está seleccionada, la lista desplegable **Ajuste preestablecido de imagen** está disponible, lo que permite seleccionar entre los ajustes preestablecidos de Dynamic Media disponibles. Esto solo está disponible si se han definido ajustes preestablecidos para el recurso seleccionado.
   * **Recorte inteligente** - When **Tipo de ajuste preestablecido** de **Recorte inteligente** está seleccionado en la lista desplegable **Representación** está disponible, lo que permite seleccionar entre las representaciones disponibles del recurso seleccionado. Esto solo está disponible si las representaciones están definidas para el recurso seleccionado.
   * **Modificadores de imagen** - Los comandos adicionales de servicio de imágenes de Dynamic Media se pueden definir aquí separados por `&`, independientemente de cuál **Tipo de ajuste preestablecido** está seleccionado.
* **Pie de ilustración**: información adicional sobre la imagen que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener pie de ilustración de DAM**: cuando se marca, el texto del pie de la imagen se rellena con el valor de los metadatos `dc:title` de DAM. Solo está disponible cuando se elige un recurso de DAM.
   * **Mostrar pie de ilustración como ventana emergente**: cuando esta opción está activada, el pie de ilustración no se mostrará debajo de la imagen, sino como una ventana emergente que se muestra en algunos exploradores al pasar el ratón por encima de la imagen.
* **Vínculo**: vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso de AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.
   * **Abrir en ficha nueva**: esta opción abre el vínculo en una nueva ventana del explorador.
* **ID** - Esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar a CSS.
* **Se ha corregido con** - Esta opción define la anchura en píxeles de la imagen.
* **Escalar imagen a anchura disponible** - Esta opción se aplica `"width":"100%"` al atributo de estilo de imagen.

>[!TIP]
>
>El **recorte inteligente** y los **ajustes preestablecidos de imagen** son opciones que se excluyen mutuamente. Si un autor necesita utilizar un ajuste preestablecido de imagen junto con una representación de recorte inteligente, el autor deberá utilizar los **Modificadores de imagen** para añadir ajustes preestablecidos manualmente.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Imagen de correo electrónico](/help/assets/image-configure-styles.png)

El componente Imagen de correo electrónico admite la AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en la variable [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Principal {#main-tab}

![Pestaña principal del cuadro de diálogo de diseño del componente de imagen](/help/email/assets/email-image-design-main.png)

* **Habilitar funciones de DM**: cuando esté marcada, las funciones de activación de [Dynamic Media](#dynamic-media) estarán disponibles.
   * Esta opción solo aparece cuando Dynamic Media está habilitado en el entorno.
* **Habilitar imágenes optimizadas para web**: cuando se selecciona, el [servicio de entrega de imágenes optimizadas para la web](/help/developing/web-optimized-image-delivery.md) ofrece las imágenes en formato WebP, lo que reduce su tamaño en un 25 % como promedio.
   * Esta opción solo está disponible en AEMaaCS.
   * Cuando está desactivada o cuando el servicio de entrega de imágenes optimizado para la web no está disponible, la variable [Servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md) se utiliza.
* **La imagen es decorativa**: defina si la opción de imagen decorativa se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener texto alternativo de DAM**: defina si la opción para recuperar el texto alternativo de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener pie de ilustración de DAM**: defina si la opción para recuperar el pie de ilustración de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Mostrar pie de ilustración como ventana emergente**: defina si la opción para mostrar el pie de ilustración como elemento emergente se habilita automáticamente al agregar el componente de imagen a una página.
* **Cambiar anchura**: este valor se utiliza para cambiar el tamaño de la anchura de las imágenes base que son activos DAM.
   * Se conservará la relación de aspecto de las imágenes.
   * Si el valor es mayor que la anchura real de la imagen, este valor no tendrá ningún efecto.
   * Este valor no afecta a las imágenes SVG.

Puede definir una lista de anchuras en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada en función del tamaño del explorador. Esta es una parte importante del [funciones adaptables](#responsive-features) del componente Imagen de correo electrónico .

* **Anchuras**: define una lista de anchuras en píxeles para la imagen y el componente y carga automáticamente la anchura más adecuada en función del tamaño del explorador.
   * Pulse o haga clic en el botón **Añadir** para añadir otro tamaño.
      * Utilice los asideros para reorganizar el orden de los tamaños.
      * Utilice el icono **Eliminar** para eliminar una anchura.
   * De forma predeterminada, la carga de imágenes se aplazará hasta que se vuelva visible.
      * Seleccione la opción **Deshabilitar la carga a medida** para cargar las imágenes al cargar la página.
* **Calidad JPEG**: el factor de calidad (indicado en porcentajes de 0 a 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).
* **Ancho predeterminado** - El ancho predeterminado de las imágenes en píxeles que se utilizará en el cuadro de diálogo de diseño

>[!TIP]
>
>Consulte el documento [Servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md) para obtener sugerencias y optimizar la selección de representaciones definiendo cuidadosamente las anchuras.

### Pestaña Estilos {#styles-tab}

El componente Imagen de correo electrónico admite la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
