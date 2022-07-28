---
title: Componente de imagen (versión 1)
description: El componente principal Imagen es una función del componente de imagen adaptable que se edita in situ.
index: n
role: Architect, Developer, Admin, User
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 5f25aee6ebcb7a5c6b8db0df5b8b853f15af97d0
workflow-type: ht
source-wordcount: '1323'
ht-degree: 100%

---

# Componente de imagen (versión 1) {#image-component-v}

El componente principal Imagen es una función del componente de imagen adaptable que se edita in situ.

## Uso {#usage}

El componente de imagen permite colocar fácilmente los recursos de imagen y ofrece opciones de edición in situ. Incluye una selección de imágenes adaptables con carga diferida, así como recorte para el autor del contenido.

El autor de la plantilla puede definir los anchos de imagen permitidos, el recorte y la configuración adicional en el [cuadro de diálogo de diseño](#design-dialog). El editor de contenido puede cargar o seleccionar recursos en el [cuadro de diálogo de configuración](#configure-dialog) y recortar la imagen en el [cuadro de diálogo de edición](#edit-dialog). Para una mayor comodidad, también está disponible una modificación simple in situ de la imagen.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de imagen, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de la versión 1 del componente de imagen.

| Versión de AEM | Componente de imagen versión 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de imagen.
>
>Para obtener más información sobre la versión actual del componente de imagen, consulte el documento [Componente de imagen](/help/components/image.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/es/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-7.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de configuración {#configure-dialog}

Además del [cuadro de diálogo de edición](#edit-dialog) y del [cuadro de diálogo de diseño](#design-dialog) estándar, el componente de imagen ofrece un cuadro de diálogo de configuración en el que la propia imagen se define junto con su descripción y propiedades básicas.

![](/help/assets/chlimage_1-50.png)

* **Recurso de imagen**
   * Coloque un recurso desde el [navegador de recursos](https://helpx.adobe.com/es/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) o pulse la opción **examinar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://helpx.adobe.com/es/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) en el editor de recursos.

* **La imagen es decorativa**: compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto alternativo**: texto alternativo del significado o la función de la imagen, para usuarios con problemas de visión.
* **Vincular**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso de AEM.
   * Si no se vincula a un recurso de AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.

* **Pie de ilustración**: la información adicional sobre la imagen que se muestra debajo de la misma es predeterminada.
* **Mostrar pie de ilustración como elemento emergente**: cuando esta opción está activada, el pie de ilustración no se mostrará debajo de la imagen, sino como una ventana emergente que se muestra en algunos exploradores al pasar el ratón por encima de la imagen.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido recortar, modificar el mapa de lanzamiento y ampliar la imagen.

![](/help/assets/chlimage_1-8.png)

* Iniciar recorte

   ![](/help/assets/chlimage_1-9.png)

   Al seleccionar esta opción, se abrirá una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano alzada** para definir su propio recorte.
   * Elija la opción **Quitar recorte** para mostrar el recurso original.

   Una vez seleccionada una opción de recorte, utilice los controladores azules para cambiar el tamaño del recorte en la imagen.

   ![](/help/assets/chlimage_1-10.png)

* Girar a la derecha

   ![](/help/assets/chlimage_1-11.png)

   Utilice esta opción para girar la imagen 90° a la derecha (en el sentido de las agujas del reloj).

* Iniciar mapa

   ![](/help/assets/chlimage_1-12.png)

   Utilice esta opción para aplicar un mapa de lanzamiento a la imagen. Al seleccionar esta opción, se abre una nueva ventana que permite al usuario seleccionar la forma del mapa:

   * **Agregar mapa rectangular**
   * **Agregar mapa circular**
   * **Agregar mapa poligonal**

      * De forma predeterminada, añade un mapa triangular. Haga doble clic en una línea de la forma para agregar un nuevo controlador azul de cambio de tamaño en un lado nuevo.

   Una vez seleccionada una forma del mapa, se superpone a la imagen para permitir el cambio de tamaño. Arrastre y suelte los controladores de tamaño azules para ajustar la forma.

   ![](/help/assets/chlimage_1-13.png)

   Después de cambiar el tamaño del mapa de lanzamiento, haga clic en él para abrir una barra de herramientas flotante y definir la ruta del vínculo.

   * **Ruta**
      * Utilice la opción Selector de rutas para seleccionar una ruta en AEM
      * Si la ruta no está en AEM, utilice la dirección URL absoluta. Las rutas no absolutas se interpretarán en relación con AEM.

      * **Texto alternativo**
Descripción alternativa del destino de la ruta
      * **Destino**
         * **Misma pestaña**
         * **Nueva pestaña**
         * **Marco principal**
         * **Marco superior**

   Pulse o haga clic en la marca de verificación azul para guardar, en la x negra para cancelar y en la papelera roja para eliminar el mapa.

   ![](/help/assets/chlimage_1-14.png)

* Restablecer zoom

   ![](/help/assets/chlimage_1-15.png)

   Si la imagen ya se ha ampliado, utilice esta opción para restablecer el nivel de zoom.

* Abrir deslizador del zoom

   ![](/help/assets/chlimage_1-16.png)

   Utilice esta opción para mostrar un control deslizante para controlar el nivel de zoom de la imagen.

   ![](/help/assets/chlimage_1-17.png)

El editor in situ también se puede utilizar para modificar la imagen. Debido a las limitaciones de espacio, solo las opciones básicas están disponibles en línea. Para obtener opciones de edición completas, utilice el modo de pantalla completa.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Las operaciones de edición de imágenes (recortar, voltear, girar) no son compatibles con las imágenes GIF. Los cambios que se hagan en el modo de edición a los GIF no se mantendrán.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las cargas de recorte, carga y rotación que tiene el autor del contenido al utilizar este componente.

### Principal {#main}

En la pestaña **Principal** puede definir una lista de anchos en píxeles permitidos para que la imagen cargue automáticamente el ancho más adecuado de la lista.

![](/help/assets/chlimage_1-51.png)

Pulse o haga clic en el botón Añadir para añadir otro tamaño.

* Utilice los asideros para reorganizar el orden de los tamaños.
* Utilice el icono Eliminar para eliminar una anchura.

De forma predeterminada, la carga de imágenes se aplazará hasta que se vuelva visible. Seleccione la opción **Deshabilitar la carga lenta** para cargar las imágenes al cargar la página.

* **Habilitar imágenes optimizadas para web**: cuando se selecciona, el [servicio de entrega de imágenes optimizadas para la web](/help/developing/web-optimized-image-delivery.md) ofrece las imágenes en formato WebP, lo que reduce su tamaño en un 25 % como promedio.
   * Esta opción solo está disponible en AEMaaCS.
   * Cuando está desmarcada o el servicio de entrega de imágenes optimizadas para la web no está disponible, se utiliza el [servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md).

### Características {#features}

En la pestaña **Características** puede definir qué opciones están disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, orientación y recorte.

* **Habilitar imágenes optimizadas para web**: cuando se selecciona, el servicio de entrega de imágenes optimizadas para la web ofrece las imágenes en formato WebP, lo que reduce su tamaño en un 25 % como promedio.
   * Esta opción solo está disponible en AEMaaCS.
   * Cuando está desmarcada o el servicio de entrega de imágenes optimizadas para la web no está disponible, se utiliza el [servlet de imagen adaptable](/help/developing/adaptive-image-servlet.md).

* Origen

   ![](/help/assets/chlimage_1-19.png)

   Seleccione la opción **Permitir carga de recursos desde el sistema de archivos** para permitir que los autores de contenido carguen imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, anule la selección de esta opción.

* Orientación

   ![](/help/assets/chlimage_1-20.png)

   * **Rotar**: utilice esta opción para permitir que el autor del contenido utilice la opción **Rotar hacia la derecha**.
   * **Voltear**
Utilice esta opción para permitir que el autor de contenido utilice las opciones 
**Voltear horizontalmente** y **voltear verticalmente**.
   >[!CAUTION]
   >
   >La opción **Voltear** está desactivada de forma predeterminada. Al activarla, se mostrarán los botones **Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen, pero la función no es compatible actualmente con AEM y los cambios realizados con estas opciones no se mantendrán.

* Recortar

   ![](/help/assets/chlimage_1-21.png)

   Seleccione la opción **Permitir recorte** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Añadir** para añadir una relación de aspecto de recorte predefinida.
   * Introduzca un nombre descriptivo que se mostrará en la lista desplegable **Iniciar recorte**.
   * Introduzca la relación numérica del aspecto.
   * Utilice los controles de arrastre para reorganizar el orden de las relaciones de aspecto
   * Utilice el icono de la papelera para eliminar una relación de aspecto.

   >[!CAUTION]
   >
   >Tenga en cuenta que, en AEM, las relaciones de aspecto de recorte se definen como **altura/anchura**. Esto es distinto de la definición convencional de anchura/altura y se realiza por motivos de compatibilidad con sistemas anteriores. Los autores de contenido no notarán ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la propia relación.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
