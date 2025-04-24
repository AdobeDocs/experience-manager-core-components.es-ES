---
title: Componente Imagen
description: El componente principal Imagen es un componente de imagen adaptable.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: ad911040d7e47fc3884071005c17accf8edd0a62
workflow-type: tm+mt
source-wordcount: '2062'
ht-degree: 94%

---


# Componente Imagen {#image-component}

El componente principal Imagen es un componente de imagen adaptable.

## Uso {#usage}

El componente Imagen presenta una selección de imágenes adaptativas y un comportamiento adaptable con carga diferida para el visitante de la página, y una ubicación sencilla de la imagen para el autor del contenido.

El autor del contenido puede utilizar el [cuadro de diálogo de edición](#edit-dialog) para editar el recurso de imagen, como aplicar un recorte o girar la imagen.

El autor de la plantilla puede definir las anchuras de la imagen y la configuración adicional en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede cargar o seleccionar activos en el [cuadro de diálogo de configuración.](#configure-dialog)

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de Imagen es la versión 3, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

En la siguiente tabla se detallan todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 3 | - | Compatible | Compatible | Compatible |
| [Versión 2](v2/image.md) | Compatible | Compatible | - | Compatible |
| [Versión 1](v1/image-v1.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Funciones adaptables {#responsive-features}

El componente de imagen incluye funciones adaptables sólidas listas para usar. En el nivel de plantilla de página, se puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los anchos predeterminados del recurso de imagen. El componente de imagen carga automáticamente la anchura correcta para mostrarla según el tamaño de la ventana del explorador. A medida que cambia el tamaño de la ventana, el componente de imagen carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente de imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que sea visible en el explorador, lo que aumenta la capacidad de respuesta de las páginas.

>[!TIP]
>
>De forma predeterminada, el componente de imagen funciona con el servlet de imagen adaptable. Consulte el documento [Servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md) para obtener más información sobre cómo funciona.

### Diferencias con la versión 2 {#v2-differences}

A diferencia de la versión 2 del componente de imagen, la versión 3 utiliza la capacidad de respuesta nativa del explorador. Esto significa que proporciona al navegador un conjunto de fuentes para una imagen para diferentes anchos y el navegador elegirá el mejor.

La mayoría de las veces, los exploradores prefieren reducir localmente la anchura para ajustarse a una ventanilla más pequeña en lugar de recuperar la imagen de menor anchura del servidor. Esto es lo que se espera y por qué el componente de imagen no debe utilizarse para la dirección de arte (diferentes imágenes/recortes para diferentes ventanillas).

[Consulte la documentación técnica del componente de imagen](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image#javascript-data-attribute-bindings) para obtener más información.

## Asistencia de Dynamic Media {#dynamic-media}

El componente de imagen (a partir de la [versión 2.13.0](/help/versions.md)) admite recursos de [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=es). [Cuando están habilitadas,](#design-dialog) estas funciones permiten agregar recursos de imagen de Dynamic Media con tan solo arrastrar y soltar o mediante el explorador de recursos como lo haría con cualquier otra imagen. Además, también se admiten modificadores de imagen, ajustes preestablecidos de imagen y cultivos inteligentes.

Las experiencias web creadas con los componentes principales pueden ofrecer funciones de imagen de Dynamic Media enriquecidas, potentes, sólidas y de alto rendimiento en varias plataformas.

## Soporte de recursos remotos {#remote-assets}

El componente de imagen (a partir de la [versión 2.23.2](/help/versions.md)) admite recursos remotos. [Una vez configurado,](/help/developing/remote-assets.md) puede seleccionar recursos desde un servicio remoto para su componente de imagen.

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente de imagen.

* Se admiten las funciones de arrastrar y soltar un recurso SVG desde DAM y de cargar un archivo SVG cargado desde un sistema de archivos local.
* El archivo SVG original se transmite (las transformaciones se omiten).
* Para una imagen SVG, las “imágenes inteligentes” y los “tamaños inteligentes” se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través de `<img src="path-to-component">`. Esto evita que el explorador ejecute cualquier script incrustado en el archivo SVG.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente de imagen y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

El componente de imagen admite [microdatos schema.org](https://schema.org).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido recortar y ampliar la imagen.

Dependiendo de si tiene [Dynamic Media](#dynamic-media) habilitado o [Soporte de recursos remotos](#remote-assets) habilitado, las opciones disponibles para editar imágenes difieren.

### Edición de recursos estándar {#standard-assets}

Si está editando recursos AEM estándar, puede hacer clic en el icono **Editar** en el menú contextual del componente de imagen.

![Cuadro de diálogo de edición del componente de imagen](/help/assets/image-edit.png)

* Iniciar recorte

  ![Iniciar icono de recorte](/help/assets/image-start-crop.png)

  Al seleccionar esta opción, se abrirá una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Quitar recorte** para mostrar el recurso original.

  Una vez seleccionada una opción de recorte, utilice los controladores azules para cambiar el tamaño del recorte en la imagen.

  ![Opciones de recorte](/help/assets/image-crop-options.png)

* Girar a la derecha

  ![Icono Rotar a la derecha](/help/assets/image-rotate-right.png)

  Utilice esta opción para girar la imagen 90° a la derecha (en el sentido de las agujas del reloj).

* Restablecer zoom

  ![Icono Restablecer zoom](/help/assets/image-reset-zoom.png)

  Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador del zoom

  ![Icono del deslizador del zoom abierto](/help/assets/image-zoom.png)

  Utilice esta opción para mostrar un control deslizante para controlar el nivel de zoom de la imagen.

  ![Control deslizador del zoom](/help/assets/image-zoom-slider.png)

El editor in situ también se puede utilizar para modificar la imagen. Debido a las limitaciones de espacio, solo las opciones básicas están disponibles en línea. Para obtener opciones de edición completas, utilice el modo de pantalla completa.

![Opciones de edición in situ de imágenes](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes no son compatibles con las imágenes GIF. Los cambios que se hagan en el modo de edición a los GIF no se mantienen.

### Edición de recursos Dynamic Media {#dynamic-media-assets}

Si tiene las [Funciones de Dynamic Media habilitadas,](#dynamic-media) la edición de la propia imagen debe realizarse en la consola recursos.

## Cuadro de diálogo de configuración {#configure-dialog}

El componente de imagen ofrece un cuadro de diálogo de configuración en el que la propia imagen se define junto con su descripción y propiedades básicas.

### Pestaña Recurso {#asset-tab}

![Pestaña de recursos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-asset.png)

* **Heredar imagen destacada de la página**: esta opción utiliza la [imagen destacada de la página vinculada](page.md) o la imagen destacada de la página actual si la imagen no está vinculada.

* **Recurso de imagen**: se rellena automáticamente si **Heredar imagen destacada de la página** está seleccionado. Anule la selección de esta opción para definir manualmente la imagen mediante las siguientes opciones.

   * Coloque un recurso desde el [explorador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Seleccionar** para abrir el [explorador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=es) para seleccionar una imagen.
      * Si [Soporte de recursos remotos](#remote-assets) está habilitado, tiene múltiples opciones para seleccionar un recurso:
         * **Local** selecciona de la biblioteca de recursos de AEM local.
         * **Remoto** selecciona desde una biblioteca de Dynamic Media fuera de su instancia de AEM.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=es) en el Editor de recursos.

* **Texto alternativo para fines de accesibilidad**: este campo le permite definir una descripción de la imagen para los usuarios con discapacidades visuales.

   * **Heredar texto alternativo de la página**: esta opción utiliza la descripción alternativa del valor de recurso vinculado de los `dc:description` metadatos en DAM o de la página actual si no hay ningún recurso vinculado.

* **No proporcionar texto alternativo**: esta opción marca la imagen para que sea ignorada por las tecnologías de asistencia, como lectores de pantalla, en casos en los que la imagen es puramente decorativa o no transmiten información adicional a la página.

### Pestaña de metadatos {#metadata-tab}

![Pestaña de metadatos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-metadata.png)

* **Tipo de ajuste preestablecido**: define los tipos de ajustes preestablecidos de imagen disponibles, ya sea **Ajustes preestablecidos de imágenes** o **Recorte inteligente**, y solo está disponible cuando las [funciones de Dynamic Media](#dynamic-meida) están habilitadas.
   * **Ajuste preestablecido de imagen**: cuando se selecciona **Tipo de ajuste preestablecido** de **Ajuste preestablecido de imagen**, está disponible el desplegable **Ajuste preestablecido de imagen**, que permite seleccionar entre los ajustes preestablecidos disponibles de Dynamic Media. Esto solo está disponible si se han definido ajustes preestablecidos para el recurso seleccionado.
   * **Recorte inteligente**: cuando se selecciona **Tipo de ajuste preestablecido** de **Recorte inteligente**, aparece disponible el menú desplegable **Representación**, que permite seleccionar entre las representaciones disponibles del recurso seleccionado. Esto solo está disponible si las representaciones están definidas para el recurso seleccionado.
   * **Modificadores de imagen**: los comandos de servidor de imágenes adicionales de Dynamic Media se pueden definir aquí separados por `&`, independientemente de los **tipos de ajustes preestablecidos** seleccionados.
* **Pie de ilustración**: información adicional sobre la imagen que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener pie de ilustración de DAM**: cuando se marca esta opción, el texto del pie de ilustración de la imagen se rellena con el valor de los metadatos `dc:title` de DAM.
   * **Mostrar pie de ilustración como elemento emergente**: cuando esta opción está activada, el pie de ilustración no se mostrará debajo de la imagen, sino como una ventana emergente que se muestra en algunos exploradores al pasar el ratón por encima de la imagen.
* **Vínculo**: vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso de AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretan como relativas a AEM.
   * **Abrir en pestaña nueva**: esta opción abre el vínculo en una nueva ventana del explorador.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

>[!TIP]
>
>El **recorte inteligente** y los **ajustes preestablecidos de imagen** son opciones que se excluyen mutuamente. Si un autor necesita utilizar un ajuste preestablecido de imagen junto con una representación de recorte inteligente, el autor debe utilizar los **Modificadores de imagen** para añadir ajustes preestablecidos manualmente.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Imagen](/help/assets/image-configure-styles.png)

El componente Imagen es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Principal {#main-tab}

![Pestaña principal del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-main.png)

* **Activar funciones de DM**: cuando esté marcada, las funciones de activación de [Dynamic Media](#dynamic-media) estarán disponibles.
   * Esta opción solo aparece cuando Dynamic Media está habilitado en el entorno.
* **Habilitar imágenes optimizadas para web**: cuando se selecciona esta opción, el [servicio de envío de imágenes optimizadas para la web](/help/developing/web-optimized-image-delivery.md) ofrece las imágenes en formato WebP, lo que reduce su tamaño en un 25 % como promedio.
   * Esta opción solo está disponible en AEMaaCS.
   * Cuando está desmarcada o el servicio de envío de imágenes optimizadas para la web no está disponible, se utiliza el [servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md).
* **Desactivación de la carga diferida**: cuando se selecciona esta opción, el componente carga previamente todas las imágenes sin carga diferida.
* **La imagen es decorativa**: defina si la opción de imagen decorativa se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener texto alternativo de DAM**: defina si la opción para recuperar el texto alternativo de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener pie de ilustración de DAM**: defina si la opción para recuperar el pie de ilustración de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Mostrar pie de ilustración como ventana emergente**: defina si la opción para mostrar el pie de ilustración como elemento emergente se habilita automáticamente al agregar el componente de imagen a una página.
* **Cambiar anchura**: este valor se utiliza para cambiar el tamaño de la anchura de las imágenes base que son activos DAM.
   * Se conserva la relación de aspecto de las imágenes.
   * Si el valor es mayor que la anchura real de la imagen, este valor no tendrá ningún efecto.
   * Este valor no afecta a las imágenes SVG.

Puede definir una lista de anchuras en píxeles para la imagen y el componente carga automáticamente la anchura más adecuada en función del tamaño del explorador. Esta es una parte importante de las [funciones adaptables](#responsive-features) del componente de imagen.

* **Anchuras**: define una lista de anchuras en píxeles para la imagen y el componente y carga automáticamente la anchura más adecuada en función del tamaño del explorador.
   * Pulse o haga clic en el botón **Añadir** para añadir otro tamaño.
      * Utilice los asideros para reorganizar el orden de tamaño.
      * Utilice el icono **Eliminar** para eliminar una anchura.
   * De forma predeterminada, la carga de imágenes se aplazará hasta que se vuelva visible.
      * Seleccione la opción **Desactivación de la carga diferida** para cargar las imágenes al cargar la página.
* **Calidad JPEG**: el factor de calidad (indicado en porcentajes de 0 a 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).

>[!TIP]
>
>Consulte el documento [Servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md) para obtener sugerencias y optimizar la selección de representaciones definiendo cuidadosamente las anchuras.

### Pestaña Estilos {#styles-tab}

El componente Imagen es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente de imagen es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
