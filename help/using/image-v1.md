---
title: Componente de imagen (v 1)
seo-title: Componente de imagen (v 1)
description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
seo-description: El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.
uuid: 20 ea 7921-511 d -4 d 3 a-b 3 df-c 2 f 2 c 1 d 8455 d
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: ab 9041 ab-e 29 e -4277-b 326-85 ab 37 df 8413
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente de imagen (v 1){#image-component-v}

El componente de imagen de componente principal es un componente de imagen adaptable que incluye edición in-situ.

## Uso {#usage}

El componente Imagen permite una fácil colocación de recursos de imagen y la edición in situ. Presenta la selección de imágenes adaptables con carga diferida, además de recortar para el autor del contenido.

El autor de la plantilla puede definir los anchos de imagen permitidos como también los recortes y ajustes adicionales en el cuadro de diálogo [de diseño](image-v1.md#main-pars_title_1995166862). El editor de contenido puede cargar o seleccionar recursos en el cuadro de diálogo [de configuración](image-v1.md#main-pars_title_55926120) y recortar la imagen en el cuadro de diálogo [de edición](image-v1.md#main-pars_title). Para mayor comodidad, también hay disponible una modificación in-situ sencilla de la imagen.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de imagen, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v 1 del componente de imagen.

| Versión de AEM | Componente de imagen v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de imagen.
>
>Para obtener más información sobre la versión actual del componente de imagen, consulte [el documento Componente](image.md) de imagen.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

Además del cuadro de diálogo [de edición](image-v1.md#main-pars_title) y [del cuadro de diálogo de edición estándar](image-v1.md#main-pars_title_1995166862), el componente de imagen ofrece un cuadro de diálogo de configuración donde la propia imagen se define junto con su descripción y sus propiedades básicas.

![](assets/chlimage_1-50.png)

* **Recurso de imagen**
   * Coloque un recurso desde el navegador [de recursos](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) o toque la opción **de exploración** para cargar desde un sistema de archivos local.
   * Toque o haga clic **en Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic **en Editar** para [transferir las representaciones del recurso](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) en el editor de recursos.

* **Image es decorativa** : compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto se aplica únicamente a imágenes decorativas.
* **Texto** alternativoo: alternativa textual del significado o función de la imagen para los lectores con deficiencias visuales.
* **Vínculo**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las URL no flotantes se interpretarán como relativas a AEM.

* **Rótulo** : información adicional sobre la imagen, que se muestra debajo de la imagen.
* **Mostrar rótulo como ventana emergente** : cuando se marque, el rótulo no se mostrará debajo de la imagen, sino como una ventana emergente mostrada por algunos exploradores al situar el ratón sobre la imagen.

## Editar cuadro de diálogo {#edit-dialog}

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

* Iniciar mapa

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

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las cargas de recorte, carga y rotación que tiene el autor del contenido cuando utilice este componente.

### Principal {#main}

En la ficha **Principal** , puede definir una lista de anchos permitidos en píxeles para que la imagen cargue automáticamente el ancho más adecuado desde la lista.

![](assets/chlimage_1-51.png)

Toque o haga clic en el botón Agregar para agregar otro tamaño.

* Utilice los controles de captura para reorganizar el orden de los tamaños.
* Utilice el icono Eliminar para eliminar una anchura.

De forma predeterminada, la carga de imágenes se pospone hasta que se vuelven visibles. Seleccione la opción **Deshabilitar carga diferida** para cargar las imágenes al cargar la página.

### Características {#features}

En la ficha **Funciones** , puede definir las opciones disponibles para los autores de contenido al utilizar el componente, incluso opciones de carga, orientación y recorte.

* Origen

   ![](assets/chlimage_1-19.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema** de archivos para permitir que los autores de contenido carguen imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar únicamente recursos de AEM, anule la selección de esta opción.

* Orientación

   ![](assets/chlimage_1-20.png)

   * **Rotar** : utilice esta opción para permitir que el autor del contenido utilice la **opción Rotar derecha** .
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
   >Tenga en cuenta que en AEM, las proporciones de aspecto de recorte se definen como **height/width**. Esto difiere de la definición convencional de anchura y altura y se realiza por motivos de compatibilidad heredados. Los autores de contenido no tendrán constancia de ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la misma proporción.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
