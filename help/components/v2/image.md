---
title: Componente Imagen  (Versión 2)
description: El componente principal Imagen es una función del componente de imagen adaptable que se edita in situ.
role: Architect, Developer, Admin, User
exl-id: 3f2b93f9-c48d-43ef-a78a-accd5090fe6f
source-git-commit: 6c251cd03997dca8961b31498c6f5de3cfdc3793
workflow-type: ht
source-wordcount: '2073'
ht-degree: 100%

---

# Componente Imagen   (Versión 2) {#image-component}

El componente de imagen del componente principal es un componente de imagen adaptable que incluye la edición in situ.

## Uso {#usage}

El componente de imagen presenta una selección de imágenes adaptativa y un comportamiento interactivo con carga diferida para el visitante de la página, así como una ubicación y un recorte sencillos de la imagen para el autor del contenido.

El autor de la plantilla puede definir los anchos de la imagen, así como el recorte y la configuración adicional en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede cargar o seleccionar recursos en el [cuadro de diálogo de configuración](#configure-dialog) y recortar la imagen en el [cuadro de diálogo de edición](#edit-dialog). Para una mayor comodidad, también está disponible una modificación simple in situ de la imagen.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 2 del componente de Imagen, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018.

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de imagen.
>
>Para obtener más información sobre la versión actual del componente de imagen, consulte el documento [Componente de imagen](/help/components/image.md).

## Funciones adaptables {#responsive-features}

El componente de imagen incluye funciones adaptables sólidas listas para usar. En el nivel de plantilla de página, se puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los anchos predeterminados del recurso de imagen. El componente de imagen cargará automáticamente la anchura correcta para mostrarla según el tamaño de la ventana del explorador. A medida que cambia el tamaño de la ventana, el componente de imagen carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente de imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que sea visible en el explorador, lo que aumenta la capacidad de respuesta de las páginas.

>[!TIP]
>
>El componente de imagen funciona con el servlet de imagen adaptable. Consulte el documento [Servlet de imagen adaptable](#adaptive-image-servlet) para obtener más información sobre cómo funciona.

## Asistencia de Dynamic Media {#dynamic-media}

El componente de imagen (a partir de la [versión 2.13.0](/help/versions.md)) admite recursos de [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=es#dynamicmedia). [Cuando están habilitadas,](#design-dialog) estas funciones permiten agregar recursos de imagen de Dynamic Media con tan solo arrastrar y soltar o mediante el explorador de recursos como lo haría con cualquier otra imagen. Además, también se admiten modificadores de imagen, ajustes preestablecidos de imagen y cultivos inteligentes.

Las experiencias web creadas con los componentes principales pueden ofrecer funciones de imagen de Dynamic Media enriquecidas, potentes, sólidas y de alto rendimiento en varias plataformas.

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente de imagen.

* Se admiten las funciones de arrastrar y soltar un recurso SVG desde DAM y de cargar un archivo SVG cargado desde un sistema de archivos local.
* El archivo SVG original se transmite (las transformaciones se omiten).
* Para una imagen SVG, las &quot;imágenes inteligentes&quot; y los &quot;tamaños inteligentes&quot; se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través de `<img src=“path-to-component”>`. Esto evita que el explorador ejecute cualquier script incrustado en el archivo SVG.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente de imagen y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_image_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

El componente de imagen admite [microdatos schema.org](https://schema.org).

## Cuadro de diálogo de configuración {#configure-dialog}

Además del [cuadro de diálogo de edición](#edit-dialog) y del [cuadro de diálogo de diseño](#design-dialog) estándar, el componente de imagen ofrece un cuadro de diálogo de configuración en el que la propia imagen se define junto con su descripción y propiedades básicas.

### Pestaña Recurso {#asset-tab}

![Pestaña de recursos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-asset.png)

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el editor de recursos.

### Pestaña de metadatos {#metadata-tab}

![Pestaña de metadatos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-metadata.png)

* **Tipo de ajuste preestablecido**: define los tipos de ajustes preestablecidos de imagen disponibles, ya sea **Ajustes preestablecidos de imágenes** o **Recorte inteligente**, y solo está disponible cuando las [funciones de Dynamic Media](#dynamic-meida) están habilitadas.
   * **Ajuste preestablecido de imagen**: cuando se selecciona **Tipo de ajuste preestablecido** de **ajustes de imagen preestablecidos**, está disponible la opción desplegable **Ajustes de imagen preestablecidos**, que permite seleccionar entre los ajustes preestablecidos disponibles de Dynamic Media. Esto solo está disponible si se han definido ajustes preestablecidos para el recurso seleccionado.
   * **Recorte inteligente**: cuando se selecciona **Tipos de ajustes preestablecidos** de **recorte inteligente**, está disponible la lista desplegable **Representación**, que permite seleccionar entre las representaciones disponibles del recurso seleccionado. Esto solo está disponible si las representaciones están definidas para el recurso seleccionado.
   * **Modificadores de imagen**: los comandos de servidor de imágenes adicionales de Dynamic Media se pueden definir aquí separados por `&`, independientemente de los **tipos de ajustes preestablecidos** seleccionados.
* **La imagen es decorativa**: compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto alternativo**: texto alternativo del significado o la función de la imagen, para usuarios con problemas de visión.
   * **Obtener texto alternativo de DAM**: cuando se selecciona, el texto alternativo de la imagen se rellena con el valor de los metadatos `dc:description` en DAM.
* **Pie de ilustración**: información adicional sobre la imagen que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener pie de ilustración de DAM**: cuando se marca, el texto del pie de la imagen se rellena con el valor de los metadatos `dc:title` de DAM.
   * **Mostrar pie de ilustración como ventana emergente**: cuando esta opción está activada, el pie de ilustración no se mostrará debajo de la imagen, sino como una ventana emergente que se muestra en algunos exploradores al pasar el ratón por encima de la imagen.
* **Vínculo**: vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso de AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

>[!TIP]
>
>El **recorte inteligente** y los **ajustes preestablecidos de imagen** son opciones que se excluyen mutuamente. Si un autor necesita utilizar un ajuste preestablecido de imagen junto con una representación de recorte inteligente, el autor deberá utilizar los **Modificadores de imagen** para añadir ajustes preestablecidos manualmente.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido recortar, modificar el mapa de lanzamiento y ampliar la imagen.

>[!NOTE]
>
>Las funciones de recorte, rotación y zoom no se aplican a los recursos de Dynamic Media. Si las [características de Dynamic Media](#dynamic-media) están habilitadas, cualquier edición de los recursos de Dynamic Media debe realizarse a través del [Cuadro de diálogo de configuración.](#configure-dialog)

![Cuadro de diálogo de edición del componente de imagen](/help/assets/image-edit.png)

* Iniciar recorte

   ![Iniciar icono de recorte](/help/assets/image-start-crop.png)

   Al seleccionar esta opción, se abrirá una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano alzada** para definir su propio recorte.
   * Elija la opción **Quitar recorte** para mostrar el recurso original.

   Una vez seleccionada una opción de recorte, utilice los controladores azules para cambiar el tamaño del recorte en la imagen.

   ![Opciones de recorte](/help/assets/image-crop-options.png)

* Girar a la derecha

   ![Icono Rotar a la derecha](/help/assets/image-rotate-right.png)

   Utilice esta opción para girar la imagen 90° a la derecha (en el sentido de las agujas del reloj).

* Voltear horizontalmente

   ![Icono Voltear horizontalmente](/help/assets/image-flip-horizontal.png)

   Utilice esta opción para voltear la imagen horizontalmente o girar la imagen 180° a lo largo del eje y.

* Voltear verticalmente

   ![Icono Voltear verticalmente](/help/assets/image-flip-vertical.png)

   Utilice esta opción para voltear la imagen verticalmente o girar la imagen 180° a lo largo del eje x.

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
>Las operaciones de edición de imágenes (recortar, voltear, girar) no son compatibles con las imágenes GIF. Los cambios que se hagan en el modo de edición a los GIF no se mantendrán.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de recorte, carga y rotación que tiene el autor del contenido al utilizar este componente.

### Pestaña Principal {#main-tab}

En la pestaña **Principal** puede definir una lista de anchuras en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada en función del tamaño del explorador. Esta es una parte importante de las [funciones adaptables](#responsive-features) del componente de imagen.

Además, puede definir qué opciones generales de componentes se desactivan o se desactivan automáticamente cuando el autor agregue el componente a una página.

![Pestaña principal del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-main-v2.png)

* **Activar funciones de DM**: cuando esté marcada, las funciones de activación de [Dynamic Media](#dynamic-media) estarán disponibles.
* **Habilitar imágenes optimizadas para web**: cuando se selecciona, el [servicio de entrega de imágenes optimizadas para la web](/help/developing/web-optimized-image-delivery.md) ofrece las imágenes en formato WebP, lo que reduce su tamaño en un 25 % como promedio.
   * Esta opción solo está disponible en AEMaaCS.
   * Cuando está desmarcada o el servicio de entrega de imágenes optimizadas para la web no está disponible, se utiliza el [servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md).
* **Habilitar la carga a medida**: defina si la opción de carga diferida se habilita automáticamente al añadir el componente de imagen a una página.
* **La imagen es decorativa**: defina si la opción de imagen decorativa se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener texto alternativo de DAM**: defina si la opción para recuperar el texto alternativo de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener pie de ilustración de DAM**: defina si la opción para recuperar el pie de ilustración de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Mostrar pie de ilustración como ventana emergente**: defina si la opción para mostrar el pie de ilustración como elemento emergente se habilita automáticamente al agregar el componente de imagen a una página.
* **Deshabilitar el seguimiento de UUID**: márquelo para deshabilitar el seguimiento del UUID del recurso de imagen.
* **Anchuras**: define una lista de anchuras en píxeles para la imagen y el componente y carga automáticamente la anchura más adecuada en función del tamaño del explorador.
   * Pulse o haga clic en el botón **Añadir** para añadir otro tamaño.
      * Utilice los asideros para reorganizar el orden de los tamaños.
      * Utilice el icono **Eliminar** para eliminar una anchura.
   * De forma predeterminada, la carga de imágenes se aplazará hasta que se vuelva visible.
      * Seleccione la opción **Deshabilitar la carga a medida** para cargar las imágenes al cargar la página.
* **Calidad JPEG**: el factor de calidad (indicado en porcentajes de 0 a 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).

>[!TIP]
>
>Consulte el documento [Servlet de imagen adaptable](#adaptive-image-servlet) para obtener sugerencias y optimizar la selección de representaciones definiendo cuidadosamente las anchuras.

### Pestaña Características {#features-tab}

En la pestaña **Características** puede definir qué opciones están disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, orientación y recorte.

* Origen

   ![Pestaña de características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-source.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema de archivos** para permitir que los autores de contenido carguen imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, anule la selección de esta opción.

* Orientación

   ![Pestaña de características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-orientation.png)

* **Rotar**
Utilice esta opción para permitir que el autor de contenido utilice la opción de 
**Girar a la derecha**.
* **Voltear**
Utilice esta opción para permitir que el autor de contenido utilice las opciones 
**Voltear horizontalmente** y **voltear verticalmente**.

   >[!CAUTION]
   >
   >La opción **Voltear** está desactivada de forma predeterminada. Al activarla, se mostrarán los botones **Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen, pero la función no es compatible actualmente con AEM y los cambios realizados con estas opciones no se mantendrán.

* Recortar

   ![Pestaña de características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-cropping.png)

   Seleccione la opción **Activar recortar** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Añadir** para añadir una relación de aspecto de recorte predefinida.
   * Introduzca un nombre descriptivo que se mostrará en la lista desplegable **Iniciar recorte**.
   * Introduzca la relación numérica del aspecto.
   * Utilice los controles de arrastre para reorganizar el orden de las relaciones de aspecto
   * Utilice el icono de la papelera para eliminar una relación de aspecto.

   >[!CAUTION]
   >
   >Tenga en cuenta que, en AEM, las relaciones de aspecto de recorte se definen como **altura/anchura**. Esto es distinto de la definición convencional de anchura/altura y se realiza por motivos de compatibilidad con sistemas anteriores. Los autores de contenido no notarán ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la propia relación.

### Pestaña Estilos {#styles-tab-1}

El componente Imagen es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente de imagen es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
