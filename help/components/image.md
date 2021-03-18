---
title: Componente de imagen
description: El componente de imagen del componente principal es una función de componente de imagen adaptable que se edita in situ.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '2175'
ht-degree: 2%

---


# Componente de imagen{#image-component}

El componente de imagen del componente principal es un componente de imagen adaptable que incluye la edición in situ.

## Uso {#usage}

El componente Imagen presenta una selección de imágenes adaptativa y un comportamiento interactivo con carga diferida para el visitante de la página, así como una ubicación y un recorte sencillos de la imagen para el autor del contenido.

El autor de la plantilla puede definir los anchos de la imagen, así como el recorte y la configuración adicional en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede cargar o seleccionar recursos en el [cuadro de diálogo de configuración](#configure-dialog) y recortar la imagen en el [cuadro de diálogo de edición](#edit-dialog). Para mayor comodidad, también está disponible una modificación simple in situ de la imagen.

## Funciones adaptables {#responsive-features}

El componente de imagen incluye funciones adaptables sólidas listas para usar. En el nivel de plantilla de página, se puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir los anchos predeterminados del recurso de imagen. El componente Imagen cargará automáticamente la anchura correcta para mostrarla según el tamaño de la ventana del explorador. A medida que cambia el tamaño de la ventana, el componente de imagen carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente de imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que sea visible en el explorador, lo que aumenta la capacidad de respuesta de las páginas.

## Soporte de Dynamic Media {#dynamic-media}

El componente Imagen (a partir de [versión 2.13.0](/help/versions.md)) admite [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia) recursos. [Cuando está habilitada, ](#design-dialog)  estas funciones permiten agregar recursos de imagen de Dynamic Media con tan solo arrastrar y soltar o mediante el navegador de recursos como lo haría con cualquier otra imagen. Además, también se admiten modificadores de imagen, ajustes preestablecidos de imagen y cultivos inteligentes.

Las experiencias web creadas con los componentes principales no pueden ofrecer funciones de imagen de Dynamic Media enriquecidas, potentes, sólidas y de alto rendimiento en varias plataformas.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de imagen es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Soporte de SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente de imagen.

* Se admiten la función de arrastrar y soltar un recurso SVG desde DAM y cargar un archivo SVG cargado desde un sistema de archivos local.
* El servlet de imagen adaptable transmite el archivo SVG original en flujo (las transformaciones se omiten).
* Para una imagen SVG, las &quot;imágenes inteligentes&quot; y los &quot;tamaños inteligentes&quot; se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través de `<img src=“path-to-component”>`. Esto evita que el navegador ejecute cualquier secuencia de comandos incrustada en el archivo SVG.

>[!CAUTION]
>
>La compatibilidad con SVG requiere la versión 2.1.0 de los componentes principales o superiores junto con el [Service Pack 2](https://docs.adobe.com/content/help/es-ES/experience-manager-64/release-notes/sp-release-notes.html) para AEM 6.4 o superior para admitir las [funciones del editor de imágenes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html) dentro de AEM.

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de imagen y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

El componente Imagen admite [schema.org microdata](https://schema.org).

## Configurar diálogo {#configure-dialog}

Además del [cuadro de diálogo de edición](#edit-dialog) y [cuadro de diálogo de diseño](#design-dialog) estándar, el componente de imagen ofrece un cuadro de diálogo de configuración en el que la propia imagen se define junto con su descripción y propiedades básicas.

### Pestaña Activo {#asset-tab}

![Pestaña Recurso del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-asset.png)

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Pestaña Metadatos {#metadata-tab}

![Pestaña Metadatos del cuadro de diálogo de configuración del componente de imagen](/help/assets/image-configure-metadata.png)

* **Tipo de ajuste preestablecido** : define los tipos de ajustes preestablecidos de imagen disponibles, ya sea  **Selector de** imágenes o Recorte  **inteligente**, y solo está disponible cuando las funciones de  [Dynamic Media ](#dynamic-meida) están habilitadas.
   * **Ajuste preestablecido de imagen** : cuando se selecciona  **Tipo** de ajuste preestablecido de  **ajustes** preestablecidos de imagen, está disponible la opción desplegable  **Ajustes preestablecidos de** imagen, que permite seleccionar entre los ajustes preestablecidos de Dynamic Media disponibles. Esto solo está disponible si se han definido ajustes preestablecidos para el recurso seleccionado.
   * **Recorte inteligente** : cuando  **se selecciona** Tipo de recorte  **inteligente** , está disponible la lista desplegable  **** Representación , que permite seleccionar entre las representaciones disponibles del recurso seleccionado. Esto solo está disponible si las representaciones están definidas para el recurso seleccionado.
   * **Modificadores de imagen** : los comandos de servidor de imágenes adicionales de Dynamic Media se pueden definir aquí separados por  `&`, independientemente de los  **tipos de** ajustes preestablecidos seleccionados.
* **La imagen es decorativa** : compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto alternativo**  - Alternativa textual del significado o función de la imagen, para lectores con deficiencias visuales.
   * **Obtener texto alternativo de DAM** : cuando se selecciona, el texto alternativo de la imagen se rellena con el valor de los  `dc:description` metadatos en DAM.
* **Rótulo** : información adicional sobre la imagen que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener rótulo de DAM** : cuando se marca, el texto del rótulo de la imagen se rellena con el valor de los  `dc:title` metadatos en DAM.
   * **Mostrar rótulo como elemento emergente** : si se selecciona, el rótulo no se muestra debajo de la imagen, sino como una ventana emergente que muestran algunos exploradores al pasar el ratón por encima de la imagen.
* **Vínculo** : vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.
* **ID** : esta opción permite controlar el identificador único del componente en el HTML y en la capa de  [datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

>[!TIP]
>
>**El** ajuste preestablecido de  **imagen de** recorte inteligente es una opción que se excluye mutuamente. Si un autor necesita utilizar un ajuste preestablecido de imagen junto con una representación de recorte inteligente, el autor deberá utilizar los **Modificadores de imagen** para añadir ajustes preestablecidos manualmente.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido recortar, modificar el mapa de lanzamiento y ampliar la imagen.

>[!NOTE]
>
>Las funciones de recorte, rotación y zoom no se aplican a los recursos de Dynamic Media. Si las [características de Dynamic Media](#dynamic-media) están habilitadas, cualquier edición de los recursos de Dynamic Media debe realizarse a través del [Cuadro de diálogo de configuración.](#configure-dialog)

![Cuadro de diálogo de edición del componente de imagen](/help/assets/image-edit.png)

* Iniciar recorte

   ![Iniciar icono de recorte](/help/assets/image-start-crop.png)

   Al seleccionar esta opción, se abre una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano libre** para definir su propio recorte.
   * Elija la opción **Quitar recorte** para mostrar el recurso original.

   Una vez seleccionada una opción de recorte, utilice los controladores azules para cambiar el tamaño del recorte en la imagen.

   ![Opciones de recorte](/help/assets/image-crop-options.png)

* Girar a la derecha

   ![Icono Girar a la derecha](/help/assets/image-rotate-right.png)

   Utilice esta opción para girar la imagen 90° a la derecha (en el sentido de las agujas del reloj).

* Girar horizontalmente

   ![Icono Girar horizontalmente](/help/assets/image-flip-horizontal.png)

   Utilice esta opción para girar la imagen horizontalmente o girar la imagen 180° a lo largo del eje y.

* Girar verticalmente

   ![Icono Girar verticalmente](/help/assets/image-flip-vertical.png)

   Utilice esta opción para girar la imagen verticalmente o girar la imagen 180° a lo largo del eje x.

* Restablecer zoom

   ![Icono Restablecer zoom](/help/assets/image-reset-zoom.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador de zoom

   ![Icono de control deslizante de zoom abierto](/help/assets/image-zoom.png)

   Utilice esta opción para mostrar un control deslizante para controlar el nivel de zoom de la imagen.

   ![Control deslizante de zoom](/help/assets/image-zoom-slider.png)

El editor in situ también se puede utilizar para modificar la imagen. Debido a las limitaciones de espacio, solo las opciones básicas están disponibles en línea. Para obtener opciones de edición completas, utilice el modo de pantalla completa.

![Opciones de edición in situ de imágenes](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, rotar) no son compatibles con las imágenes GIF. Los cambios que se hagan en el modo de edición a los GIF no se mantendrán.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de recorte, carga, rotación y carga que tiene el autor del contenido al utilizar este componente.

### Pestaña principal {#main-tab}

En la pestaña **Main** puede definir una lista de anchuras en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada en función del tamaño del explorador. Esta es una parte importante de las [funciones adaptables](#responsive-features) del componente de imagen.

Además, puede definir qué opciones generales de componentes se desactivan o se desactivan automáticamente cuando el autor agrega el componente a una página.

![Pestaña principal del cuadro de diálogo de diseño del componente de imagen](/help/assets/image-design-main.png)

* **Habilitar funciones**  de DM: cuando está marcada, las funciones de activación de  [Dynamic Media ](#dynamic-media) están disponibles.
* **Habilitar carga diferida** : defina si la opción de carga diferida está activada automáticamente al añadir el componente de imagen a una página.
* **La imagen es decorativa** : defina si la opción de imagen decorativa está activada automáticamente al añadir el componente de imagen a una página.
* **Obtener texto alternativo de DAM**: defina si la opción para recuperar el texto alternativo de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Obtener rótulo de DAM** : defina si la opción para recuperar el rótulo de DAM se habilita automáticamente al añadir el componente de imagen a una página.
* **Mostrar rótulo como elemento emergente** : defina si la opción para mostrar el rótulo de imagen como elemento emergente se activa automáticamente al agregar el componente de imagen a una página.
* **Deshabilitar el seguimiento UUID** : compruebe para deshabilitar el seguimiento del UUID del recurso de imagen.
* **Anchura** : define una lista de anchuras en píxeles para la imagen y el componente carga automáticamente la anchura más adecuada en función del tamaño del explorador.
   * Toque o haga clic en el botón **Add** para añadir otro tamaño.
      * Utilice los asideros para reorganizar el orden de los tamaños.
      * Utilice el icono **Delete** para eliminar una anchura.
   * De forma predeterminada, la carga de imágenes se aplaza hasta que se vuelve visible.
      * Seleccione la opción **Disable lazy loading** para cargar las imágenes al cargar la página.
* **Calidad JPEG** : factor de calidad (en porcentaje desde 0 y 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).

### Pestaña Características {#features-tab}

En la pestaña **Features** puede definir qué opciones están disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, orientación y recorte.

* Origen

   ![Cuadro de diálogo de diseño del componente de imagen Ficha Características](/help/assets/image-design-features-source.png)

   Seleccione la opción **Permitir carga de recursos desde el sistema de archivos** para permitir que los autores de contenido carguen imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, anule la selección de esta opción.

* Orientación

   ![Cuadro de diálogo de diseño del componente de imagen Ficha Características](/help/assets/image-design-features-orientation.png)

* ****
RotarUtilice esta opción para permitir que el autor de contenido utilice la variable 
**Opción Girar** a la derecha .
* ****
FlipUtilice esta opción para permitir que el autor de contenido utilice la variable 
**Girar** horizontalmente y  **voltear** verticalmente.

   >[!CAUTION]
   >
   >La opción **Flip** está desactivada de forma predeterminada. Al activarlo, se mostrarán los botones **Girar verticalmente** y **Girar horizontalmente** en el cuadro de diálogo de edición del componente de imagen, pero la función no es compatible actualmente con AEM y los cambios realizados con estas opciones no se mantendrán.

* Recortar

   ![Cuadro de diálogo de diseño del componente de imagen Ficha Características](/help/assets/image-design-features-cropping.png)

   Seleccione la opción **Permitir recorte** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Add** para añadir una relación de aspecto de recorte predefinida.
   * Introduzca un nombre descriptivo que se mostrará en la lista desplegable **Iniciar recorte**.
   * Introduzca la relación numérica del aspecto.
   * Utilice los controles de arrastre para reorganizar el orden de las relaciones de aspecto
   * Utilice el icono de papelera para eliminar una relación de aspecto.

   >[!CAUTION]
   >
   >Tenga en cuenta que en AEM, las relaciones de aspecto de recorte se definen como **height/width**. Esto es distinto de la definición convencional de anchura/altura y se realiza por motivos de compatibilidad con sistemas anteriores. Los autores de contenido no notarán ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la propia relación.

### Pestaña Estilos {#styles-tab-1}

El componente Imagen es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Servlet de imagen adaptable {#adaptive-image-servlet}

El componente de imagen utiliza el servlet de imagen adaptable del componente principal. [El servicio de imagen adaptable ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) es responsable del procesamiento y la transmisión de imágenes y los desarrolladores pueden aprovecharlo en sus  [personalizaciones de los componentes principales](/help/developing/customizing.md).

>[!NOTE]
>
>Las solicitudes condicionales a través del encabezado `Last-Modified` son compatibles con el servlet de imagen adaptable, pero el almacenamiento en caché del encabezado `Last-Modified` [debe habilitarse en Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).
>
>[La configuración de Dispatcher de muestra](/help/developing/archetype/overview.md) del tipo de archivo del proyecto de AEM ya contiene esta configuración.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Imagen es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
