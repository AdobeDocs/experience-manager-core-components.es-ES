---
title: Componente de texto (v 1)
seo-title: Componente de texto (v 1)
description: nulo
seo-description: El componente de texto es un componente de compositor y edición enriquecido que incluye edición in-situ.
uuid: b 787 ebac-fa 85-416 a-b 96 b -9 d 2 ee 85428 ec
content-type: referencia
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 5 e 37 dc 7-dfd 4-4 a 44-89 b 6-c 15651472 c 43
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
noindex: verdadero
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de texto (v 1){#text-component-v}

El componente de texto es un componente de compositor y edición enriquecido que incluye edición in-situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido sólido que permite editar texto fácilmente en un editor en línea simplificado, así como en un formato de pantalla completa.

El cuadro de diálogo [de edición](text-v1.md#main-pars_title) incluye la edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición de pantalla completa. Con el cuadro de diálogo [de diseño](text-v1.md#main-pars_title_1995166862), se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla para el autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de texto, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla muestra la compatibilidad de v 1 del componente de texto.

| Versión de AEM | Componente de texto v 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la v 1 del componente de texto.
>
>Para obtener más información sobre la versión actual del componente de texto, consulte [el documento Componente](text.md) de texto.

## Salida de componente de muestra {#sample-component-output}

La siguiente es una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>La exportación JSON de los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información [de compatibilidad de Componentes principales v 1](versions.md#main-pars_title_236368006) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que un usuario espera componer texto.

![](assets/chlimage_1-52.png)

* Negrita

   ![](assets/chlimage_1-53.png)

   Se utiliza para aplicar formato de negrita al texto seleccionado o al texto de formato negrita que se introduce después del cursor.

   **Ctrl + B** se puede utilizar como método abreviado de teclado.

* Cursiva

   ![](assets/chlimage_1-54.png)

   Se utiliza para aplicar formato en cursiva al texto en cursiva o texto seleccionado tras el cursor.

   **Ctrl + I** se puede utilizar como método abreviado de teclado.

* Subrayado

   ![](assets/chlimage_1-55.png)

   Se utiliza para aplicar el formato subrayado al texto seleccionado o para subrayar el texto especificado después del cursor.

   **Ctrl + U** se puede utilizar como método abreviado de teclado.

* Subíndice

   ![](assets/chlimage_1-56.png)

   Se utiliza para dar formato al texto o texto seleccionado después del cursor como subíndice.

* Superíndice

   ![](assets/chlimage_1-57.png)

   Se utiliza para dar formato al texto o texto seleccionado después del cursor como superíndice.

* Pegar como texto

   ![](assets/chlimage_1-58.png)

   Pega cualquier texto copiado como texto sin formato sin ningún formato.

   Al seleccionar esta opción, se abre una ventana donde el texto se puede pegar como texto sin formato sin formato como vista previa antes de insertarse en el texto. Para aceptar o hacer clic en la marca de verificación, toque o haga clic en la x.

   ![](assets/chlimage_1-59.png)

* Pegar desde Word

   ![](assets/chlimage_1-60.png)

   Al seleccionar esta opción, se abre una ventana donde se puede pegar el texto manteniendo su formato como vista previa antes de insertarlo en el texto. Para aceptar o hacer clic en la marca de verificación, toque o haga clic en la x.

   ![](assets/chlimage_1-61.png)

* Hipervínculo

   ![](assets/chlimage_1-62.png)

   Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando el texto ya está seleccionado y abre una ventana con opciones adicionales para configurar el vínculo.

   ![](assets/chlimage_1-63.png)

   * Introduzca la ubicación

      * Utilizar el cuadro de diálogo Abrir selección para elegir una ruta en AEM
      * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta (las rutas no absolutas se interpretan en relación con AEM)
   * Introducción de texto descriptivo alternativo para el vínculo
   * Seleccionar comportamiento de vínculo

      * Destino
      * Misma ficha
      * Nueva ficha
      * Marco principal
      * Marco superior
   Toque o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

* Desvincular

   ![](assets/chlimage_1-64.png)

   Utilice esta opción para eliminar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando un vínculo ya está seleccionado.

* Buscar

   ![](assets/chlimage_1-65.png)

   Utilice esta opción para buscar en el texto las incidencias de una cadena de texto especificada. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda.

   ![](assets/chlimage_1-66.png)

   Escriba el texto para el que desea buscar y tocar, o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidencia entre mayúsculas y minúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, se resalta y el cuadro de diálogo de búsqueda aparece atenuado. Toque o haga clic en el **botón Buscar** de nuevo en el cuadro de diálogo atenuado para buscar la siguiente aparición.

   ![](assets/chlimage_1-67.png)

   Si no se encuentran ocurrencias adicionales, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

   ![](assets/chlimage_1-68.png)

* Reemplazar

   ![](assets/chlimage_1-69.png)

   Utilice esta opción para buscar en el texto las incidencias de una cadena de texto específica y reemplazar las coincidencias con otra cadena. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda y reemplazo.

   ![](assets/chlimage_1-70.png)

   Escriba el texto para el que desea buscar así como el texto con el que debe reemplazarse.

   Toque o haga clic **en Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidencia entre mayúsculas y minúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, se resalta y el cuadro de diálogo de búsqueda aparece atenuado. Vuelva a hacer clic en **el** botón Buscar en el cuadro de diálogo atenuado para buscar la siguiente aparición o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y resaltado. Tenga en cuenta que **el** botón Reemplazar solo está activo cuando se realiza una coincidencia.

   Seleccione **Reemplazar todo** para reemplazar todas las incidencias del texto a la vez.

* Alinear texto a la izquierda

   ![](assets/chlimage_1-71.png)

   Se utiliza para alinear el texto con el margen izquierdo.

* Centrar texto

   ![](assets/chlimage_1-72.png)

   Se utiliza para centrar el texto.

* Alinear texto a la derecha

   ![](assets/chlimage_1-73.png)

   Se utiliza para alinear el texto con el margen derecho.

* Viñeta

   ![](assets/chlimage_1-74.png)

   Se utiliza para dar formato al texto seleccionado como una lista con viñetas o empezar la inserción de una lista con viñetas después del cursor.

   Para finalizar una lista con viñetas, toque o haga clic en el **botón Viñeta** de nuevo o introduzca dos retornos de carro.

* Numerado

   ![](assets/chlimage_1-75.png)

   Se utiliza para dar formato al texto seleccionado como una lista numerada o empezar la inserción de una lista numerada después del cursor.

   Para finalizar una lista numerada, toque o haga clic en el **botón Numerado** de nuevo o introduzca dos retornos de carro.

* Anular sangría

   ![](assets/chlimage_1-76.png)

   Se utiliza para reducir el nivel de sangría del texto o texto seleccionado tras el cursor.

   Solo activo si el texto o la posición seleccionados del cursor ya están sangrados.

* Sangría

   ![](assets/chlimage_1-77.png)

   Se utiliza para aumentar el nivel de sangría del texto o texto seleccionado tras el cursor.

* Tabla

   ![](assets/chlimage_1-78.png)

   Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abre una ventana para especificar los detalles de la tabla.

   ![](assets/chlimage_1-79.png)

   * **Columnas** : número de columnas de la tabla (obligatorio)
   * **Filas** : número de filas de la tabla (obligatorio)
   * **Ancho** : ancho de la tabla
   * **Altura** : altura de la tabla
   * **Margen** de celdas: espacio alrededor del contenido de la celda
   * **Espaciado** de celdas: espacio entre celdas
   * **Borde** : grosor de las líneas de borde de la tabla
   * Si para el encabezado de la tabla:

      * Se debe utilizar la primera fila
      * Se debe utilizar la primera columna
      * Se debe utilizar la primera fila y la primera columna
      * O no debe usarse ningún encabezado.
   * **Rótulo** : rótulo de la tabla


* Revisar ortografía

   ![](assets/chlimage_1-80.png)

   Se utiliza para revisar la ortografía del contenido del texto. Los errores ortográficos pueden subrayarse con líneas rotas y rojas.

* Caracteres especiales

   ![](assets/chlimage_1-81.png)

   Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana donde se muestran los caracteres disponibles.

   ![](assets/chlimage_1-82.png)

   Toque o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

* Modificar código fuente

   ![](assets/chlimage_1-83.png)

   Se utiliza para ver y modificar el origen HTML del texto.

   Toque o haga clic en **el icono Editar** fuente para cambiar el contenido del texto de la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic **en el icono Editar** fuente para volver a la vista formateada.

   >[!CAUTION]
   >
   >Como siempre sucede con el acceso a HTML sin procesar, se debe tener cuidado al utilizar **la opción Editar** fuente.
   >
   >
   >El HTML especificado mediante **la edición** de origen se escanea para los riesgos XSS y las secuencias de comandos insertadas se eliminan y no aparecerán en la página resultante. Sin embargo, el HTML incorrecto introducido en **Editar** código fuente puede dañar la plantilla de la página como un formato inesperado o procesar la página resultante inutilizable.

* Formato de párrafo

   ![](assets/chlimage_1-84.png)

   Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción se abre una lista desplegable desde la que se selecciona el formato de párrafo.

   ![](assets/chlimage_1-85.png)

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![](assets/chlimage_1-86.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de formato de texto disponibles para los autores de contenido.

### Características {#features}

![](assets/chlimage_1-28.png)

Las siguientes funciones pueden activarse o desactivarse para el componente.

* Pegar texto sin formato
* Pasado desde Word
* Buscar y reemplazar
* Corrección ortográfica
* Edición de origen

### Formato {#formatting}

![](assets/chlimage_1-29.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas
* Alineación
* Negrita, cursiva, subrayado
* Vínculos
* Subíndice

### Estilos de párrafo {#paragraph-styles}

![](assets/chlimage_1-30.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Toque o haga clic en el botón **Agregar** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para eliminar un estilo de estilo o haga clic en **el** botón Eliminar.
* Para reorganizar el orden de los formatos, toque o haga clic y arrastre los controles.

### Caracteres especiales {#special-characters}

![](assets/chlimage_1-31.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Una vez activados, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Agregar** para insertar un nuevo carácter.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para eliminar un toque de caracteres o haga clic en **el** botón Eliminar.
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controles.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde github.

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).
