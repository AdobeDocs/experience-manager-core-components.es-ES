---
title: Componente de imagen
seo-title: Componente de imagen
description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
seo-description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
uuid: 1 a 229 d 42-2428-43 aa -895 a -9 b 7 c 1 bf 02834
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 4684 f 33-2 fb 5-4 f 32-866 f -7136 cf 1800 d 7
translation-type: tm+mt
source-git-commit: 34ae30ca8be3ad290924b986acfac11d960f2ee0

---


# Componente de imagen{#image-component}

El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.

## Uso {#usage}

El componente de imagen incluye selección de imagen adaptable y comportamiento interactivo con carga diferida para el visitante de la página, así como una ubicación de imagen y recorte sencillos para el autor del contenido.

El autor de la plantilla puede definir los anchos de imagen, así como también los ajustes de recorte y otros ajustes [adicionales](#design-dialog). El editor de contenido puede cargar o seleccionar recursos en el cuadro de diálogo [de configuración](#configure-dialog) y recortar la imagen en el cuadro de diálogo [de edición](#edit-dialog). Para mayor comodidad, también hay disponible una modificación in-situ sencilla de la imagen.

## Funciones interactivas {#responsive-features}

El componente de imagen viene con potentes funciones adaptables listos para funcionar directamente en el cuadro. En el nivel de plantilla de página, el cuadro de diálogo [de diseño](#design-dialog) se puede utilizar para definir los anchos predeterminados del recurso de imagen. A continuación, el componente de imagen cargará automáticamente el ancho correcto para que se muestre según el tamaño de la ventana del explorador. A medida que se cambia el tamaño de la ventana, el componente Imaage carga dinámicamente el tamaño de imagen correcto sobre la marcha. No es necesario que los desarrolladores de componentes se preocupen por definir consultas de medios personalizadas, ya que el componente de imagen ya está optimizado para cargar el contenido.

Además, el componente Imagen admite la carga diferida para aplazar la carga del recurso de imagen real hasta que sea visible en el navegador, lo que aumenta la capacidad de respuesta de las páginas.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de imagen es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatible | Compatible | Compatible |
| [v1](image-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Compatibilidad con SVG {#svg-support}

Los gráficos vectoriales escalables (SVG) son compatibles con el componente de imagen.

* Ambos son compatibles con arrastrar y soltar un recurso SVG desde DAM y cargar una carga de archivo SVG desde un sistema de archivos local.
* El servlet de imagen adaptable se transmite en flujo continuo (se omiten las transformaciones).
* Para una imagen SVG, las «imágenes inteligentes» y los «tamaños inteligentes» se definen en una matriz vacía del modelo de imagen.

### Seguridad {#security}

Por razones de seguridad, el Editor de imágenes nunca llama directamente al SVG original. Se llama a través `<img src=“path-to-component”>`. Esto evita que el explorador ejecute secuencias de comandos incrustadas en el archivo SVG.

>[!CAUTION]
>
>La compatibilidad con SVG requiere la versión 2.1.0 de los componentes principales o superior, junto [con service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) para AEM 6.4 o [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para AEM 6.3 o superior para admitir [nuevas funciones de editor de imágenes](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) en AEM.

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de imagen, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/image.html).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

>[!NOTE]
>
>Desde la versión de componentes principales 2.1.0, el componente de imagen admite [schema.org microdata](https://schema.org).

## Configurar cuadro de diálogo {#configure-dialog}

Además del cuadro de diálogo [de edición](#edit-dialog) y [del cuadro de diálogo de edición estándar](#design-dialog), el componente de imagen ofrece un cuadro de diálogo de configuración donde la propia imagen se define junto con su descripción y sus propiedades básicas.

### Ficha Recursos {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Recurso de imagen**
   * Coloque un recurso desde el navegador [de recursos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) o toque la opción **de exploración** para cargar desde un sistema de archivos local.
   * Toque o haga clic **en Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic **en Editar** para [transferir las representaciones del recurso](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) en el editor de recursos.

### Ficha Metadatos {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

* **Image es decorativa**
si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto se aplica únicamente a imágenes decorativas.
* **Alternativa**textual textual
del significado o función de la imagen para los lectores con deficiencias visuales.
   * Obtener texto alternativo de DAM: cuando se marque, el texto alternativo de la imagen se rellenará con el valor de `dc:description` los metadatos en DAM.

* **Información**adicional sobre
la imagen, que se muestra debajo de la imagen de forma predeterminada.
   * **Obtenga un rótulo de DAM**
cuando se active el texto de rótulos de la imagen con el valor de `dc:title` los metadatos en DAM.
   * **Mostrar rótulo como ventana emergente** Cuando se active, el rótulo no se mostrará debajo de la imagen, sino como una ventana emergente mostrada por algunos exploradores al situar el ratón sobre la imagen.

* **Vínculo**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las URL no flotantes se interpretarán como relativas a AEM.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite que el autor del contenido recorte, modifique el mapa de inicio y aplique zoom a la imagen.

![](assets/chlimage_1-8.png)

* Iniciar recorte

   ![](assets/chlimage_1-9.png)

   Al seleccionar esta opción se abre una lista desplegable para proporciones de recorte predefinidas.

   * Elija la opción Mano **libre** para definir su propio recorte.
   * Elija la opción **Quitar recorte** para mostrar el recurso original.
   Una vez seleccionada la opción de recorte, utilice los controles azules para ajustar el tamaño del recorte en la imagen.

   ![](assets/chlimage_1-10.png)

* Rotar a la derecha

   ![](assets/chlimage_1-11.png)

   Utilice esta opción para rotar la imagen 90 ° a la derecha (en sentido de las agujas del reloj).

* Voltear horizontalmente

   ![](assets/screen_shot_2018-04-16at091404.png)

   Utilice esta opción para voltear la imagen horizontalmente o girar la imagen 180 ° a lo largo del eje Y.

* Voltear verticalmente

   ![](assets/screen_shot_2018-04-16at091410.png)

   Utilice esta opción para voltear la imagen verticalmente o girar la imagen 180 ° a lo largo del eje x.

* Iniciar mapa

   >[!CAUTION]
   >
   >La función Iniciar mapa requiere la versión 2.1.0 de los componentes principales o superior, junto [con service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) para AEM 6.4 o [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para AEM 6.3 o superior para admitir [nuevas funciones de editor de imágenes](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) en AEM.

   ![](assets/chlimage_1-12.png)

   Utilice esta opción para aplicar un mapa de inicio a la imagen. Al seleccionar esta opción, se abre una ventana nueva que permite al usuario seleccionar la forma del mapa:

   * **Agregar mapa rectangular**
   * **Agregar mapa circular**
   * **Agregar mapa poligonal**
      * De forma predeterminada, agrega un mapa triángulo. Haga doble clic en una línea de la forma para agregar un nuevo manipulador de cambio de tamaño azul en un nuevo lado.
   Cuando se selecciona una forma de mapa, se superpone en la imagen que permite el cambio de tamaño. Arrastre y suelte los controles de cambio de tamaño azul para ajustar la forma.

   ![](assets/chlimage_1-13.png)

   Después de cambiar el tamaño del mapa de inicio, haga clic en él para abrir una barra flotante para definir la ruta del vínculo.

   * **Ruta**
      * Utilice la opción Selector de rutas para seleccionar una ruta en AEM
      * Si la ruta no está en AEM, utilice la dirección URL absoluta. Las rutas no absolutas se interpretarán en relación con AEM.
   * **Texto**
alternativo Descripción alternativa del destino de ruta
   * **Destino**
      * **Misma ficha**
      * **Nueva ficha**
      * **Marco principal**
      * **Marco superior**
   Toque o haga clic en la marca de verificación azul para guardar, la x negra para cancelar y la papelera roja puede eliminar el mapa.

   ![](assets/chlimage_1-14.png)

* Restablecer zoom

   ![](assets/chlimage_1-15.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador de zoom

   ![](assets/chlimage_1-16.png)

   Utilice esta opción para mostrar un deslizador para controlar el nivel de zoom de la imagen.

   ![](assets/chlimage_1-17.png)

El editor in-situ también se puede utilizar para modificar la imagen. Debido a limitaciones de espacio, solo hay disponibles opciones básicas en línea. Para las opciones de edición completa, utilice el modo de pantalla completa.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, rotar) no son compatibles con las imágenes GIF. Los cambios realizados en el modo de edición a GIF no persistirán.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de recorte, carga y giro y de carga que tiene el autor del contenido al utilizar este componente.

### Ficha Principal {#main-tab}

En la ficha **Principal** , puede definir una lista de anchos en píxeles para la imagen y el componente cargará automáticamente la anchura más adecuada según el tamaño del navegador. Ésta es una parte importante de las funciones [adaptables](#responsive-features) del componente de imagen.

Además, puede definir qué opciones de componente general se encuentran automáticamente o desactivadas cuando el autor agrega el componente a una página.

![](assets/screenshot_2018-10-19at102756.png)

* **Habilite la carga
diferida** Definir si la opción de carga diferida se activa automáticamente al agregar el componente de imagen a una página.
* **La imagen es decorativa**
si la opción de imagen decorativa se activa automáticamente al agregar el componente de imagen a una página.
* **Obtener texto alternativo de DAM**
Definir si la opción para recuperar el texto alternativo del DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Obtenga un rótulo de DAM**
Definir si la opción para recuperar el rótulo del DAM se activa automáticamente al agregar el componente de imagen a una página.
* **Mostrar el rótulo como ventana emergente** Definir si la opción para mostrar el rótulo de imagen como ventana emergente se activa automáticamente al agregar el componente de imagen a una página.
* **Deshabilitar seguimiento de UUID**
Para deshabilitar el seguimiento del UUID del recurso de imagen.

* **Anchura**
Define una lista de anchos en píxeles para la imagen y el componente carga automáticamente el ancho más adecuado según el tamaño del navegador.
   * Toque o haga clic en el botón **Agregar** para agregar otro tamaño.
      * Utilice los controles de captura para reorganizar el orden de los tamaños.
      * Utilice el icono **Eliminar** para eliminar una anchura.
   * De forma predeterminada, las imágenes se cargan hasta que se vuelven visibles.
      * Seleccione la opción **Deshabilitar carga diferida** para cargar las imágenes al cargar la página.
* **Calidad
JPEG** El factor de calidad (en porcentaje entre 0 y 100) para las imágenes JPEG transformadas (p. ej., escaladas o recortadas).

>[!CAUTION]
>
>La opción Calidad JPEG está disponible desde la versión 2.2.0 de los componentes principales.

>[!NOTE]
>
>En la versión 2.2.0 de los componentes principales, el componente de imagen añade el atributo exclusivo UUID `data-asset-id` al recurso de imagen para permitir el seguimiento y el análisis de la cantidad de vistas que reciben los recursos individuales.

### Ficha Funciones {#features-tab}

En la ficha **Funciones** , puede definir las opciones disponibles para los autores de contenido al utilizar el componente, incluso opciones de carga, orientación y recorte.

* Origen

   ![](assets/chlimage_1-19.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema** de archivos para permitir que los autores de contenido carguen imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar únicamente recursos de AEM, anule la selección de esta opción.

* Orientación

   ![](assets/chlimage_1-20.png)

* **Rotarutilice**
esta opción para permitir que el autor del contenido utilice la **opción Rotar derecha** .
* **Voltear**
Utilice esta opción para permitir al autor del contenido utilizar **las opciones Voltear horizontalmente** y **Voltear verticalmente** .

   >[!CAUTION]
   >
   >**La** opción Voltear está deshabilitada de forma predeterminada. Si se activa, se mostrarán **los botones Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen. Sin embargo, la función no se admite actualmente en AEM y los cambios realizados con estas opciones no persistirán.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
 -->

* Recortar

   ![](assets/chlimage_1-21.png)

   Seleccione la opción **Permitir recorte** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic **en Agregar** para agregar una proporción de aspecto de recorte predefinida.
   * Introduzca un nombre descriptivo, que se mostrará en la lista desplegable **Iniciar recorte** .
   * Introduzca la proporción numérica del aspecto.
   * Utilice los controles de arrastrar para reorganizar el orden de las proporciones de aspecto
   * Utilice el icono de la papelera para eliminar una proporción de aspecto.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Esto difiere de la definición convencional de anchura y altura y se realiza por motivos de compatibilidad heredados. Los autores de contenido no tendrán constancia de ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la misma proporción.

### Ficha Estilos {#styles-tab-1}

El componente Imagen admite [el sistema de estilos AEM](authoring.md#component-styling).