---
title: Componente de imagen
description: El componente de imagen del componente principal es una función de edición in situ del componente de imagen adaptable.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 2%

---


# Componente de imagen{#image-component}

El componente de imagen del componente principal es un componente de imagen adaptable que incluye la edición in-situ.

## Uso {#usage}

El componente de imagen presenta una selección de imagen adaptable y un comportamiento interactivo con la carga diferida para el visitante de página, así como una colocación y recorte sencillos de la imagen para el autor del contenido.

El autor de la plantilla puede definir los anchos de la imagen, así como el recorte y la configuración adicional en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede cargar o seleccionar recursos en el [cuadro de diálogo de configuración](#configure-dialog) y recortar la imagen en el [cuadro de diálogo de edición](#edit-dialog). Para mayor comodidad, también está disponible una modificación simple in-situ de la imagen.

## Características interactivas {#responsive-features}

El componente de imagen incorpora funciones interactivas sólidas listas para usar. En el nivel de plantilla de página, se puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los anchos predeterminados del recurso de imagen. A continuación, el componente de imagen cargará automáticamente la anchura correcta para que se muestre en función del tamaño de la ventana del navegador. A medida que se cambia el tamaño de la ventana, el componente de imagen carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente de imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que esté visible en el navegador, lo que aumenta la capacidad de respuesta de las páginas.

## Soporte de Dynamic Media {#dynamic-media}

El componente Imagen (a partir de [versión 2.13.0](/help/versions.md)) admite [recursos de Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia). [Cuando están activadas, ](#design-dialog) estas funciones oferta la capacidad de agregar recursos de imagen de Dynamic Media con una simple operación de arrastrar y soltar o a través del navegador de recursos, como lo haría con cualquier otra imagen. Además, también se admiten modificadores de imagen, ajustes preestablecidos de imagen y recortes inteligentes.

Las experiencias web creadas con componentes principales no pueden ofrecer funciones de imagen Dynamic Media enriquecidas, potentes, sólidas, de alto rendimiento y multiplataforma.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de imagen es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente Imagen.

* Se admiten la función de arrastrar y soltar un recurso SVG desde DAM y la carga de un archivo SVG desde un sistema de archivos local.
* El servlet de imagen adaptable transmite el archivo SVG original (se omiten las transformaciones).
* Para una imagen SVG, las &quot;imágenes inteligentes&quot; y los &quot;tamaños inteligentes&quot; se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través de `<img src=“path-to-component”>`. Esto evita que el navegador ejecute secuencias de comandos incrustadas en el archivo SVG.

>[!CAUTION]
>
>La compatibilidad con SVG requiere la versión 2.1.0 de los componentes principales o superior, junto con el [service pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) para AEM 6.4 o superior, a fin de admitir las [funciones del editor de imágenes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html) dentro de AEM.

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de imagen y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

El componente Imagen admite [microdatos de esquema.org](https://schema.org).

## Configurar cuadro de diálogo {#configure-dialog}

Además del [cuadro de diálogo de edición](#edit-dialog) y [cuadro de diálogo de diseño](#design-dialog) estándar, el componente de imagen oferta un cuadro de diálogo de configuración donde la imagen misma se define junto con su descripción y propiedades básicas.

### Ficha Recurso {#asset-tab}

![Ficha Recurso del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-asset.png)

* **Recurso de imagen**
   * Suelte un recurso del [navegador de recursos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) o toque la opción **examinar** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para deseleccionar la imagen seleccionada actualmente.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Ficha Metadatos {#metadata-tab}

![Ficha Metadatos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-metadata.png)

* **Tipo**  de ajuste preestablecido: define los tipos de ajustes preestablecidos de imagen disponibles, ya sea  **de** ajuste preestablecido de imagen o de recorte **** inteligente, y solo está disponible cuando están activadas las funciones de  [Dynamic Media ](#dynamic-meida) .
   * **Ajuste preestablecido**  de imagen: cuando se selecciona  **Tipo** de ajuste preestablecido de  **ajustes preestablecidos de** imagen, está disponible el menú desplegable  **Ajustes preestablecidos de** imagen, lo que permite seleccionar los ajustes preestablecidos de Dynamic Media disponibles. Solo está disponible si se han definido ajustes preestablecidos para el recurso seleccionado.
   * **Recorte**  inteligente: cuando se selecciona  **Tipo** de  **recorte inteligente preestablecido, la opción de** recorte inteligente desplegable  **** Representación está disponible, lo que permite seleccionar las representaciones disponibles del recurso seleccionado. Solo está disponible si se definen representaciones para el recurso seleccionado.
   * **Modificadores**  de imagen: los comandos de servicio de imágenes adicionales de Dynamic Media se pueden definir aquí separados por  `&`, independientemente del tipo de  **ajuste** preestablecido seleccionado.
* **La imagen es decorativa** : compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto**  alternativo - Alternativa textual del significado o función de la imagen, para lectores con deficiencias visuales.
   * **Obtener texto alternativo de DAM** : cuando se selecciona, el texto alternativo de la imagen se rellena con el valor de los  `dc:description` metadatos en DAM.
* **Rótulo** : información adicional sobre la imagen, que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener rótulo de DAM** : al activarlo, el texto del rótulo de la imagen se rellenará con el valor de los  `dc:title` metadatos en DAM.
   * **Mostrar rótulo como elemento emergente** : al activarlo, el rótulo no se mostrará debajo de la imagen, sino como elemento emergente que muestran algunos exploradores al pasar el ratón por encima de la imagen.
* **Vínculo** : vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

>[!TIP]
>
>**El** ajuste preestablecido de  **imagen de** recorte inteligente son opciones que se excluyen mutuamente. Si un autor necesita utilizar un ajuste preestablecido de imagen junto con una representación de recorte inteligente, deberá utilizar los **modificadores de imagen** para agregar ajustes preestablecidos manualmente.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor recortar, modificar el mapa de inicio y aplicar zoom a la imagen.

>[!NOTE]
>
>Las funciones de recorte, rotación y zoom no se aplican a los recursos de Dynamic Media. Si las [características de Dynamic Media](#dynamic-media) están habilitadas, la edición de los recursos de Dynamic Media debe realizarse a través del [Cuadro de diálogo de configuración.](#configure-dialog)

![Cuadro de diálogo de edición del componente de imagen](/help/assets/image-edit.png)

* Recorte de inicio

   ![Icono de recorte de inicio](/help/assets/image-start-crop.png)

   Al seleccionar esta opción, se abre una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano libre** para definir su propio recorte.
   * Elija la opción **Eliminar recorte** para mostrar el recurso original.

   Una vez seleccionada la opción de recorte, utilice los controladores azules para ajustar el tamaño del recorte en la imagen.

   ![Opciones de recorte](/help/assets/image-crop-options.png)

* Girar a la derecha

   ![Icono Girar a la derecha](/help/assets/image-rotate-right.png)

   Utilice esta opción para rotar la imagen 90° hacia la derecha (en el sentido de las agujas del reloj).

* Voltear horizontalmente

   ![Icono de voltear horizontalmente](/help/assets/image-flip-horizontal.png)

   Utilice esta opción para voltear la imagen horizontalmente o girar la imagen 180° a lo largo del eje y.

* Voltear verticalmente

   ![Voltear icono vertical](/help/assets/image-flip-vertical.png)

   Utilice esta opción para voltear la imagen verticalmente o girar la imagen 180° a lo largo del eje x.

* Restablecer zoom

   ![Restablecer icono de zoom](/help/assets/image-reset-zoom.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador de zoom

   ![Abrir icono de deslizador de zoom](/help/assets/image-zoom.png)

   Utilice esta opción para mostrar un deslizador para controlar el nivel de zoom de la imagen.

   ![Control deslizante de zoom](/help/assets/image-zoom-slider.png)

El editor in-situ también puede utilizarse para modificar la imagen. Debido a las limitaciones de espacio, solo las opciones básicas están disponibles en línea. Para las opciones de edición completas, utilice el modo de pantalla completa.

![Opciones de edición in situ de imágenes](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, rotar) no son compatibles con las imágenes GIF. Los cambios que se realicen en el modo de edición a GIF no se mantendrán.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de recorte, carga, rotación y carga que tiene el autor del contenido al utilizar este componente.

### Ficha principal {#main-tab}

En la ficha **Main** puede definir una lista de anchuras en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada en función del tamaño del explorador. Esta es una parte importante de las [funciones adaptables](#responsive-features) del componente Imagen.

Además, puede definir qué opciones generales de componente se desactivan o se desactivan automáticamente cuando el autor agrega el componente a una página.

![Ficha principal del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-main.png)

* **Activar las funciones**  de DM: cuando se selecciona, las funciones de activación de  [Dynamic Media ](#dynamic-media) están disponibles.
* **Activar carga**  diferida: defina si la opción de carga diferida se activa automáticamente al agregar el componente de imagen a una página.
* **La imagen es decorativa** : defina si la opción de imagen decorativa se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener texto alternativo de DAM**: defina si la opción para recuperar el texto alternativo de DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener rótulo de DAM** : defina si la opción para recuperar el rótulo de DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Mostrar rótulo como elemento emergente** : defina si la opción para mostrar el rótulo de imagen como elemento emergente se activa automáticamente al agregar el componente de imagen a una página.
* **Deshabilitar el seguimiento**  UUID: marque esta opción para deshabilitar el seguimiento del UUID del recurso de imagen.
* **Anchos** : define una lista de anchuras en píxeles para la imagen y el componente carga automáticamente la anchura más adecuada en función del tamaño del navegador.
   * Toque o haga clic en el botón **Añadir** para agregar otro tamaño.
      * Use los asideros para reorganizar el orden de los tamaños.
      * Utilice el icono **Eliminar** para eliminar un ancho.
   * De forma predeterminada, la carga de imágenes se aplaza hasta que se hace visible.
      * Seleccione la opción **Deshabilitar la carga diferida** para cargar las imágenes al cargar la página.
* **Calidad**  JPEG: factor de calidad (en porcentaje de 0 a 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).

### Ficha Características {#features-tab}

En la ficha **Funciones** puede definir las opciones disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, orientación y recorte.

* Origen

   ![Ficha Características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-source.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema de archivos** para permitir a los autores de contenido cargar imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, desactive esta opción.

* Orientación

   ![Ficha Características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-orientation.png)

* ****
RotarUtilice esta opción para permitir que el autor del contenido utilice la variable 
**Opción Girar** a la derecha.
* ****
VoltearUtilice esta opción para permitir que el autor del contenido utilice la variable 
**Cambiar** horizontalmente y  **voltear** verticalmente.

   >[!CAUTION]
   >
   >La opción **Voltear** está deshabilitada de forma predeterminada. Al habilitarlo, se mostrarán los botones **Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen, aunque la función no se admite actualmente en AEM y no se conservarán los cambios realizados con estas opciones.

* Recortar

   ![Ficha Características del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-features-cropping.png)

   Seleccione la opción **Permitir recortar** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Añadir** para agregar una proporción de aspecto de recorte predefinida.
   * Escriba un nombre descriptivo, que se mostrará en la lista desplegable **Recortar Inicio**.
   * Introduzca la proporción numérica del aspecto.
   * Utilice los controladores de arrastre para reorganizar el orden de las proporciones de aspecto
   * Utilice el icono de papelera para eliminar una proporción de aspecto.

   >[!CAUTION]
   >
   >Tenga en cuenta que en AEM, las relaciones de aspecto de recorte se definen como **altura/anchura**. Esto es distinto de la definición convencional de anchura/altura y se realiza por motivos de compatibilidad con sistemas anteriores. Los autores de contenido no tendrán en cuenta ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la relación misma.

### Ficha Estilos {#styles-tab-1}

El componente Imagen admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Servlet de imagen adaptable {#adaptive-image-servlet}

El componente de imagen utiliza el servlet de imagen adaptable del componente principal. [El ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) servicio de imágenes adaptable es responsable del procesamiento y la transmisión de imágenes y puede ser utilizado por los desarrolladores en sus  [personalizaciones de los componentes](/help/developing/customizing.md) principales.

>[!NOTE]
>
>Las solicitudes condicionales mediante el encabezado `Last-Modified` son compatibles con el servlet de imagen adaptable, pero el almacenamiento en caché del encabezado `Last-Modified` [debe habilitarse en Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).
>
>[La configuración de despachante de ejemplo del Arquetipo](/help/developing/archetype/overview.md) de proyecto de AEM ya contiene esta configuración.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Imagen admite la capa de datos del cliente de Adobe [](/help/developing/data-layer/overview.md).
