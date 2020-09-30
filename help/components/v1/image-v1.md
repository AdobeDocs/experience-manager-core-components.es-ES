---
title: Componente de imagen (v1)
description: El componente de imagen del componente principal es una función de edición in situ del componente de imagen adaptable.
index: n
translation-type: tm+mt
source-git-commit: 78202dc777b90f795f66873921c55e21ef8a239c
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 3%

---


# Image Component (v1) {#image-component-v}

El componente de imagen del componente principal es una función de edición in situ del componente de imagen adaptable.

## Uso {#usage}

El componente de imagen permite colocar fácilmente recursos de imagen y ofertas en la edición in-situ. Incluye selección de imágenes adaptables con carga diferida, así como recorte para el autor del contenido.

El autor de la plantilla puede definir los anchos de imagen permitidos, así como el recorte y la configuración adicional en el cuadro de diálogo [de](#design-dialog)diseño. El editor de contenido puede cargar o seleccionar recursos en el cuadro de diálogo [de](#configure-dialog) configuración y recortar la imagen en el cuadro de diálogo [de](#edit-dialog)edición. Para mayor comodidad, también está disponible una modificación simple in-situ de la imagen.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de imagen, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla lista la compatibilidad de v1 del componente de imagen.

| Versión de AEM | Componente de imagen v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de imagen.
>
>Para obtener más información sobre la versión actual del componente de imagen, consulte el documento del componente [de](/help/components/image.md) imagen.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](/help/versions.md) para obtener más información.

## Configurar cuadro de diálogo {#configure-dialog}

Además del cuadro de diálogo [de](#edit-dialog) edición estándar y del cuadro de diálogo [de](#design-dialog)diseño, el componente de imagen oferta un cuadro de diálogo de configuración en el que la imagen misma se define junto con su descripción y sus propiedades básicas.

![](/help/assets/chlimage_1-50.png)

* **Recurso de imagen**
   * Suelte un recurso del navegador [de](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) recursos o toque la opción de **exploración** para cargarlo desde un sistema de archivos local.
   * Toque o haga clic en **Borrar** para anular la selección de la imagen seleccionada.
   * Toque o haga clic en **Editar** para [administrar las representaciones del recurso](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) en el editor de recursos.

* **La imagen es decorativa** : compruebe si la tecnología de asistencia debe ignorar la imagen y, por lo tanto, no requiere un texto alternativo. Esto solo se aplica a imágenes decorativas.
* **Texto** alternativo - Alternativa textual del significado o función de la imagen, para lectores con problemas de visión.
* **Vínculo**
   * Vincule la imagen a otro recurso.
   * Utilice el cuadro de diálogo de selección para vincular a otro recurso AEM.
   * Si no se vincula a un recurso AEM, introduzca la dirección URL absoluta. Las direcciones URL no resueltas se interpretarán como relativas a AEM.

* **Rótulo** : la información adicional sobre la imagen que se muestra debajo de la imagen es predeterminada.
* **Mostrar rótulo como elemento emergente** : al activarlo, el rótulo no se mostrará debajo de la imagen, sino como elemento emergente que muestran algunos exploradores al pasar el ratón por encima de la imagen.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite al autor recortar, modificar el mapa de inicio y aplicar zoom a la imagen.

![](/help/assets/chlimage_1-8.png)

* Recorte de inicio

   ![](/help/assets/chlimage_1-9.png)

   Al seleccionar esta opción, se abre una lista desplegable para las proporciones de recorte predefinidas.

   * Elija la opción **Mano** libre para definir su propio recorte.
   * Elija la opción **Eliminar recorte** para mostrar el recurso original.

   Una vez seleccionada la opción de recorte, utilice los controladores azules para ajustar el tamaño del recorte en la imagen.

   ![](/help/assets/chlimage_1-10.png)

* Girar a la derecha

   ![](/help/assets/chlimage_1-11.png)

   Utilice esta opción para rotar la imagen 90° hacia la derecha (en el sentido de las agujas del reloj).

* Iniciar mapa

   ![](/help/assets/chlimage_1-12.png)

   Utilice esta opción para aplicar un mapa de inicio a la imagen. Al seleccionar esta opción se abre una nueva ventana que permite al usuario seleccionar la forma del mapa:

   * **Añadir mapa rectangular**
   * **Añadir mapa circular**
   * **Añadir mapa poligonal**

      * De forma predeterminada, agrega un mapa de triángulo. Haga clic con el botón doble en una línea de la forma para agregar un nuevo controlador azul de cambio de tamaño en un lado nuevo.

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

El cuadro de diálogo de diseño permite al autor de la plantilla definir las cargas de recorte, carga y rotación que el autor tiene al utilizar este componente.

### Principal {#main}

On the **Main** tab you can define a list of allowed widths in pixels for the image to automatically load the most appropriate width from the list.

![](/help/assets/chlimage_1-51.png)

Toque o haga clic en el botón Añadir para agregar otro tamaño.

* Use los asideros para reorganizar el orden de los tamaños.
* Utilice el icono Eliminar para eliminar un ancho.

De forma predeterminada, la carga de imágenes se aplaza hasta que se hace visible. Seleccione la opción **Deshabilitar la carga** diferida para cargar las imágenes al cargar la página.

### Características {#features}

En la ficha **Funciones** puede definir las opciones disponibles para los autores de contenido al utilizar el componente, incluidas las opciones de carga, la orientación y el recorte.

* Origen

   ![](/help/assets/chlimage_1-19.png)

   Seleccione la opción **Permitir la carga de recursos desde el sistema** de archivos para permitir a los autores de contenido cargar imágenes desde su equipo local. Para obligar a los autores de contenido a seleccionar solo recursos de AEM, desactive esta opción.

* Orientación

   ![](/help/assets/chlimage_1-20.png)

   * **Rotar** : Utilice esta opción para permitir que el autor del contenido utilice la opción **Girar a la derecha** .
   * **Voltear** Utilice esta opción para permitir que el autor del contenido utilice la variable 
**Opciones de voltear horizontalmente** y **voltear verticalmente** .
   >[!CAUTION]
   >
   >La opción **Voltear** está desactivada de forma predeterminada. Al habilitarla, se mostrarán los botones **Voltear verticalmente** y **Voltear horizontalmente** en el cuadro de diálogo de edición del componente de imagen; sin embargo, la función no es compatible actualmente con AEM y los cambios realizados con estas opciones no se mantendrán.

* Recortar

   ![](/help/assets/chlimage_1-21.png)

   Seleccione la opción **Permitir recortar** para permitir que el autor del contenido recorte la imagen en el componente en el cuadro de diálogo de edición.
   * Haga clic en **Añadir** para agregar una proporción de aspecto de recorte predefinida.
   * Escriba un nombre descriptivo, que se mostrará en la lista desplegable Recortar **** Inicio.
   * Introduzca la proporción numérica del aspecto.
   * Utilice los controladores de arrastre para reorganizar el orden de las proporciones de aspecto
   * Utilice el icono de papelera para eliminar una proporción de aspecto.

   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Esto es distinto de la definición convencional de anchura/altura y se realiza por motivos de compatibilidad con sistemas anteriores. Los autores de contenido no tendrán en cuenta ninguna diferencia siempre que proporcione un nombre claro de la relación, ya que el nombre se muestra en la interfaz de usuario y no en la relación misma.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de imagen [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.
