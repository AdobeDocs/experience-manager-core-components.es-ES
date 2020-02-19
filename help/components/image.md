---
title: Componente de imagen
description: El componente de imagen del componente principal es una función de edición in situ del componente de imagen adaptable.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de imagen{#image-component}

El componente de imagen del componente principal es un componente de imagen adaptable que incluye la edición in-situ.

## Uso {#usage}

El componente de imagen presenta una selección de imagen adaptable y un comportamiento interactivo con carga diferida para el visitante de la página, así como una colocación y recorte sencillos de la imagen para el autor del contenido.

El autor de la plantilla puede definir el ancho de la imagen, así como el recorte y la configuración adicional en el cuadro de diálogo [de](#design-dialog)diseño. El editor de contenido puede cargar o seleccionar recursos en el cuadro de diálogo [de](#configure-dialog) configuración y recortar la imagen en el cuadro de diálogo [de](#edit-dialog)edición. Para mayor comodidad, también está disponible una modificación simple in-situ de la imagen.

## Funciones adaptables {#responsive-features}

El componente de imagen incorpora funciones interactivas sólidas listas para usar. En el nivel de plantilla de página, el cuadro de diálogo [de](#design-dialog) diseño se puede utilizar para definir los anchos predeterminados del recurso de imagen. A continuación, el componente de imagen cargará automáticamente la anchura correcta para que se muestre en función del tamaño de la ventana del navegador. A medida que se cambia el tamaño de la ventana, el componente de imagen carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente de imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que esté visible en el navegador, lo que aumenta la capacidad de respuesta de las páginas.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de imagen es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](v1/image-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente Imagen.

* Se admiten la función de arrastrar y soltar un recurso SVG desde DAM y la carga de un archivo SVG desde un sistema de archivos local.
* El velet de imagen adaptable transmite el archivo SVG original (las transformaciones se omiten).
* Para una imagen SVG, las &quot;imágenes inteligentes&quot; y los &quot;tamaños inteligentes&quot; se establecen en una matriz vacía en el modelo de imagen.

### Seguridad {#security}

Por motivos de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través `<img src=“path-to-component”>`. Esto evita que el navegador ejecute secuencias de comandos incrustadas en el archivo SVG.

>[!CAUTION]
>
>La compatibilidad con SVG requiere la versión 2.1.0 de los componentes principales o superior, junto con el [Service Pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) para AEM 6.4 o el [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para AEM 6.3 o superior, para admitir [nuevas funciones](https://docs.adobe.com/content/help/en/experience-manager-64/developing/components/image-editor.html) del editor de imágenes en AEM.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de imagen, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_image)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente de imagen admite microdatos [de](https://schema.org)schema.org.

## Configurar cuadro de diálogo {#configure-dialog}

Además del cuadro de diálogo [de](#edit-dialog) edición estándar y del cuadro de diálogo [de](#design-dialog)diseño, el componente de imagen ofrece un cuadro de diálogo de configuración en el que la imagen misma se define junto con su descripción y sus propiedades básicas.

### Ficha Recurso {#asset-tab}

![](/help/assets/screen_shot_2018-01-08at114245.png)

* **Recurso de imagen**
   * Suelte un recurso del navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) recursos o toque la opción de **exploración** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) en el editor de recursos.

### Ficha Metadatos {#metadata-tab}

![](/help/assets/screen_shot_2018-01-08at114527.png)

* **La imagen es decorativa** Compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto** alternativo Alternativa textual del significado o función de la imagen, para lectores con problemas de visión.
   * Obtener texto alternativo de DAM: cuando se selecciona, el texto alternativo de la imagen se rellena con el valor de los metadatos en DAM `dc:description` .

* **Rótulo** Información adicional sobre la imagen, que se muestra debajo de la imagen de forma predeterminada.
   * **Obtener rótulo de DAM** Cuando se selecciona, el texto del rótulo de la imagen se rellena con el valor de los `dc:title` metadatos en DAM.
   * **Mostrar rótulo como emergente** Cuando está activado, el rótulo no se mostrará debajo de la imagen, sino como una ventana emergente que muestran algunos navegadores al pasar el ratón por encima de la imagen.

* **Vínculo**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso de AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor recortar, modificar el mapa de inicio y aplicar zoom a la imagen.

![](/help/assets/chlimage_1-8.png)

* Iniciar recorte

   ![](/help/assets/chlimage_1-9.png)

   Al seleccionar esta opción, se abre una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano** libre para definir su propio recorte.
   * Elija la opción **Eliminar recorte** para mostrar el recurso original.
   Una vez seleccionada la opción de recorte, utilice los controladores azules para ajustar el tamaño del recorte en la imagen.

   ![](/help/assets/chlimage_1-10.png)

* Girar a la derecha

   ![](/help/assets/chlimage_1-11.png)

   Utilice esta opción para rotar la imagen 90° hacia la derecha (en el sentido de las agujas del reloj).

* Voltear horizontalmente

   ![](/help/assets/screen_shot_2018-04-16at091404.png)

   Utilice esta opción para voltear la imagen horizontalmente o girar la imagen 180° a lo largo del eje y.

* Voltear verticalmente

   ![](/help/assets/screen_shot_2018-04-16at091410.png)

   Utilice esta opción para voltear la imagen verticalmente o girar la imagen 180° a lo largo del eje x.

* Iniciar mapa

   >[!CAUTION]
   >
   >La función de mapa de inicio requiere la versión 2.1.0 de los componentes principales o superior, junto con el [Service Pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) para AEM 6.4 o el [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para AEM 6.3 o superior para admitir [nuevas funciones](https://docs.adobe.com/content/help/en/experience-manager-64/developing/components/image-editor.html) de editor de imágenes en AEM.

   ![](/help/assets/chlimage_1-12.png)

   Utilice esta opción para aplicar un mapa de inicio a la imagen. Al seleccionar esta opción se abre una nueva ventana que permite al usuario seleccionar la forma del mapa:

   * **Agregar mapa rectangular**
   * **Agregar mapa circular**
   * **Agregar mapa poligonal**
      * De forma predeterminada, agrega un mapa de triángulo. Haga doble clic en una línea de la forma para añadir un nuevo controlador azul de cambio de tamaño en un lado nuevo.
   Una vez seleccionada una forma de mapa, se superpone a la imagen, lo que permite cambiar el tamaño. Arrastre y suelte los controladores de tamaño azules para ajustar la forma.

   ![](/help/assets/chlimage_1-13.png)

   Después de ajustar el tamaño del mapa de inicio, haga clic en él para abrir una barra de herramientas flotante para definir la ruta del vínculo.

   * **Ruta**
      * Utilice la opción Selector de ruta para seleccionar una ruta en AEM
      * Si la ruta no está en AEM, utilice la dirección URL absoluta. Las rutas no absolutas se interpretarán en relación con AEM.
   * **Texto** alternativo Descripción alternativa del destino de ruta
   * **Destino**
      * **Misma ficha**
      * **Nueva ficha**
      * **Marco principal**
      * **Marco superior**
   Toque o haga clic en la marca de verificación azul para guardar, la x negra para cancelar y la papelera roja para eliminar el mapa.

   ![](/help/assets/chlimage_1-14.png)

* Restablecer zoom

   ![](/help/assets/chlimage_1-15.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador de zoom

   ![](/help/assets/chlimage_1-16.png)

   Utilice esta opción para mostrar un deslizador para controlar el nivel de zoom de la imagen.

   ![](/help/assets/chlimage_1-17.png)

El editor in-situ también puede utilizarse para modificar la imagen. Debido a las limitaciones de espacio, solo las opciones básicas están disponibles en línea. Para las opciones de edición completas, utilice el modo de pantalla completa.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, rotar) no son compatibles con las imágenes GIF. Los cambios que se realicen en el modo de edición a GIF no se mantendrán.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de recorte, carga, rotación y carga que tiene el autor del contenido al utilizar este componente.

### Ficha Principal {#main-tab}

En la ficha **Principal** puede definir una lista de anchuras en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada en función del tamaño del navegador. Esta es una parte importante de las funciones [](#responsive-features) interactivas del componente de imagen.

Además, puede definir qué opciones generales de componente se desactivan o se desactivan automáticamente cuando el autor agrega el componente a una página.

![](/help/assets/screenshot_2018-10-19at102756.png)

* **Activar carga** diferidaDefina si la opción de carga diferida se activa automáticamente al agregar el componente de imagen a una página.
* **La imagen es decorativa** Defina si la opción de imagen decorativa se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener texto alternativo de DAM** Defina si la opción para recuperar el texto alternativo de DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener rótulo de DAM** Defina si la opción para recuperar el rótulo de DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Mostrar rótulo como elemento emergente** Defina si la opción para mostrar el rótulo de imagen como elemento emergente se activa automáticamente al agregar el componente de imagen a una página.
* **Desactive la** comprobación de seguimiento UUID para desactivar el seguimiento del UUID del recurso de imagen.

* **Anchos** Define una lista de anchuras en píxeles para la imagen y el componente carga automáticamente la anchura más adecuada en función del tamaño del navegador.
   * Toque o haga clic en el botón **Agregar** para agregar otro tamaño.
      * Use los asideros para reorganizar el orden de los tamaños.
      * Utilice el icono **Eliminar** para eliminar un ancho.
   * De forma predeterminada, la carga de imágenes se aplaza hasta que se hace visible.
      * Seleccione la opción **Deshabilitar la carga** diferida para cargar las imágenes al cargar la página.
* **Calidad** JPEG Factor de calidad (en porcentaje de 0 a 100) para imágenes JPEG transformadas (por ejemplo, escaladas o recortadas).

>[!CAUTION]
>
>La opción Calidad JPEG está disponible desde la versión 2.2.0 de los componentes principales.

>[!NOTE]
>
>A partir de la versión 2.2.0 de los componentes principales, el componente de imagen agrega el atributo UUID exclusivo `data-asset-id` al recurso de imagen para permitir el seguimiento y el análisis del número de vistas que reciben los recursos individuales.

### Ficha Características {#features-tab}

En la ficha **Funciones** puede definir las opciones disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, la orientación y el recorte.

* Origen

   ![](/help/assets/chlimage_1-19.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema** de archivos para permitir a los autores de contenido cargar imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, desactive esta opción.

* Orientación

   ![](/help/assets/chlimage_1-20.png)

* **Rotar** Utilice esta opción para permitir que el autor del contenido utilice la opción **Girar a la derecha** .
* **Voltear** Utilice esta opción para permitir que el autor del contenido utilice las opciones **Voltear horizontalmente** y **Voltear verticalmente** .

   >[!CAUTION]
   >
   >La opción **Voltear** está desactivada de forma predeterminada. Al habilitarla, se mostrarán los botones **Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen; sin embargo, AEM no admite actualmente la función y los cambios realizados con estas opciones no se mantendrán.

* Recortar

   ![](/help/assets/chlimage_1-21.png)

   Seleccione la opción **Permitir recortar** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Agregar** para agregar una proporción de aspecto de recorte predefinida.
   * Escriba un nombre descriptivo que se mostrará en la lista desplegable **Iniciar recorte** .
   * Introduzca la proporción numérica del aspecto.
   * Utilice los controladores de arrastre para reorganizar el orden de las proporciones de aspecto
   * Utilice el icono de papelera para eliminar una proporción de aspecto.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Esto difiere de la definición convencional de anchura y altura y se realiza por motivos de compatibilidad heredados. Los autores de contenido no tendrán en cuenta ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la relación misma.

### Ficha Estilos {#styles-tab-1}

El componente Imagen admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.

## Visor de imágenes adaptable {#adaptive-image-servelet}

El componente de imagen utiliza el velet de imagen adaptable del componente principal. [El servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) de imagen adaptable es responsable del procesamiento y la transmisión de imágenes y puede ser aprovechado por los desarrolladores en sus [personalizaciones de los componentes](/help/developing/customizing.md)principales.

>[!NOTE]
>
>Las solicitudes condicionales a través del `Last-Modified` encabezado son compatibles con el velet de imágenes adaptable, pero el almacenamiento en caché del `Last-Modified` encabezado [debe habilitarse en Dispatcher](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#caching-http-response-headers).
>
>[La configuración de despachante de ejemplo de AEM Project Archetype](/help/developing/archetype/overview.md)ya contiene esta configuración.
