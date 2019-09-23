---
title: Componente de texto (v1)
seo-title: Componente de texto (v1)
description: nulo
seo-description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye edición in-situ.
uuid: b787ebac-fa85-416a-b96b-9d2ee85428ec
content-type: referencia
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: d5e37dc7-dfd4-4a44-89b6-c15651472c43
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
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Text Component (v1){#text-component-v}

El componente Texto es un componente de composición y edición de texto enriquecido que incluye edición in-situ.

## Uso {#usage}

El componente de texto ofrece un potente editor de texto enriquecido que permite una edición de texto sencilla en un editor en línea simplificado y en un formato de pantalla completa.

El cuadro de diálogo [de](text-v1.md#main-pars_title) edición incluye edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición a pantalla completa. Mediante el cuadro de diálogo [de](text-v1.md#main-pars_title_1995166862)diseño, se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de texto, introducida originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

En la tabla siguiente se muestra la compatibilidad de v1 del componente de texto.

| Versión de AEM | Componente de texto v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de texto.
>
>Para obtener más información sobre la versión actual del componente de texto, consulte el documento Componente [de](text.md) texto.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la información de [compatibilidad de los componentes principales v1](versions.md#main-pars_title_236368006) para obtener más información.

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que un usuario espera que compongan texto.

![](assets/chlimage_1-52.png)

* Negrita

   ![](assets/chlimage_1-53.png)

   Se utiliza para aplicar formato de negrita al texto seleccionado o para aplicar formato negrita al texto introducido después del cursor.

   **Ctrl+B** se puede utilizar como método abreviado de teclado.

* Cursiva

   ![](assets/chlimage_1-54.png)

   Se utiliza para aplicar formato en cursiva al texto seleccionado o texto en cursiva introducido después del cursor.

   **Ctrl+I** se puede utilizar como método abreviado de teclado.

* Subrayado

   ![](assets/chlimage_1-55.png)

   Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

   **Ctrl+U** se puede utilizar como método abreviado de teclado.

* Subíndice

   ![](assets/chlimage_1-56.png)

   Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

* Superíndice

   ![](assets/chlimage_1-57.png)

   Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como superíndice.

* Pegar como texto

   ![](assets/chlimage_1-58.png)

   Pega el texto copiado como texto sin formato sin ningún formato.

   Al seleccionar esta opción, se abre una ventana donde el texto se puede pegar como texto sin formato sin formato como vista previa antes de insertarlo en el texto. Acepte tocando o haciendo clic en la marca de verificación y cancele la acción tocando o haciendo clic en la x.

   ![](assets/chlimage_1-59.png)

* Pegar desde Word

   ![](assets/chlimage_1-60.png)

   Al seleccionar esta opción, se abre una ventana donde se puede pegar el texto manteniendo su formato como una vista previa antes de insertarlo en el texto. Acepte tocando o haciendo clic en la marca de verificación y cancele la acción tocando o haciendo clic en la x.

   ![](assets/chlimage_1-61.png)

* Hipervínculo

   ![](assets/chlimage_1-62.png)

   Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando el texto ya está seleccionado y abre una ventana con opciones adicionales para configurar el vínculo.

   ![](assets/chlimage_1-63.png)

   * Introduzca la ubicación

      * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
      * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta (las rutas no absolutas se interpretan como relativas a AEM)
   * Escriba un texto descriptivo alternativo para el vínculo
   * Seleccionar comportamiento de vínculo

      * Destino
      * Misma ficha
      * Nueva ficha
      * Marco principal
      * Marco superior
   Toque o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

* Desvincular

   ![](assets/chlimage_1-64.png)

   Utilice esta opción para eliminar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

* Buscar

   ![](assets/chlimage_1-65.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda.

   ![](assets/chlimage_1-66.png)

   Escriba el texto para el cual desee buscar y toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidir mayúsculas y minúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, ésta se resalta y el cuadro de diálogo de búsqueda se atenúa. Toque o haga clic de nuevo en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente incidencia.

   ![](assets/chlimage_1-67.png)

   Si no se encuentran más incidencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

   ![](assets/chlimage_1-68.png)

* Reemplazar

   ![](assets/chlimage_1-69.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazar las coincidencias por otra cadena. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda y reemplazo.

   ![](assets/chlimage_1-70.png)

   Escriba el texto para el que desea buscar, así como el texto con el que debe reemplazarse.

   Toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidir mayúsculas y minúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, ésta se resalta y el cuadro de diálogo de búsqueda se atenúa. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente incidencia o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Reemplazar** solo está activo una vez que se ha realizado una coincidencia.

   Seleccione **Reemplazar todo** para reemplazar todas las apariciones del texto a la vez.

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

   Se utiliza para dar formato al texto seleccionado como una lista con viñetas o para comenzar la inserción de una lista con viñetas después del cursor.

   Para finalizar una lista con viñetas, toque o haga clic de nuevo en el botón **Viñeta** o introduzca dos retornos de carro.

* Numerado

   ![](assets/chlimage_1-75.png)

   Se utiliza para dar formato al texto seleccionado como una lista numerada o para comenzar la inserción de una lista numerada después del cursor.

   Para finalizar una lista numerada, toque o haga clic de nuevo en el botón **Numerado** o introduzca dos retornos de carro.

* Anular sangría

   ![](assets/chlimage_1-76.png)

   Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

   Solo activa si el texto o la posición seleccionados del cursor ya están sangrados.

* Sangría

   ![](assets/chlimage_1-77.png)

   Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

* Tabla

   ![](assets/chlimage_1-78.png)

   Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción se abre una ventana para especificar los detalles de la tabla.

   ![](assets/chlimage_1-79.png)

   * **Columnas** : el número de columnas de la tabla (obligatorio)
   * **Filas** : el número de filas de la tabla (obligatorio)
   * **Anchura** : anchura de la tabla
   * **Altura** : altura de la tabla
   * **Relleno** de celdas: el espacio alrededor del contenido de la celda
   * **Espaciado** de celdas: el espacio entre celdas
   * **Borde** : el peso de las líneas de borde de la tabla
   * Si para el encabezado de la tabla:

      * Se debe utilizar la primera fila
      * Debe utilizarse la primera columna
      * Debe utilizarse la primera fila y la primera columna
      * O bien, no se debe utilizar ningún encabezado.
   * **Rótulo** : rótulo de la tabla


* Revisar ortografía

   ![](assets/chlimage_1-80.png)

   Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se ven subrayados con líneas rojas rotas rotas.

* Caracteres especiales

   ![](assets/chlimage_1-81.png)

   Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana donde se muestran los caracteres disponibles.

   ![](assets/chlimage_1-82.png)

   Toque o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

* Modificar código fuente

   ![](assets/chlimage_1-83.png)

   Se utiliza para ver y modificar el origen HTML del texto.

   Toque o haga clic en el icono Editar **** origen para cambiar el contenido del texto desde la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic en el icono Editar **** origen de nuevo para volver a la vista con formato.

   >[!CAUTION]
   >
   >Como siempre sucede con el acceso a HTML sin procesar, hay que tener cuidado al usar la opción Editar **** origen.
   >
   >
   >El código HTML introducido mediante la edición **de** código fuente se analiza para detectar riesgos XSS y las secuencias de comandos insertadas se eliminan y no aparecerán en la página resultante. Sin embargo, el HTML mal formado introducido en la edición **de** origen puede dañar la plantilla de la página, lo que da como resultado un formato inesperado o que la página resultante quede inutilizable.

* Formato de párrafo

   ![](assets/chlimage_1-84.png)

   Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar estas opciones se abre una lista desplegable desde la que se selecciona el formato de párrafo.

   ![](assets/chlimage_1-85.png)

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![](assets/chlimage_1-86.png)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Características {#features}

![](assets/chlimage_1-28.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pasado de la palabra
* Buscar y reemplazar
* Corrector ortográfico
* Edición de origen

### Formato {#formatting}

![](assets/chlimage_1-29.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas
* Alineación
* Negrita, cursiva, subrayado
* Vínculos
* Subíndice/superíndice

### Estilos de párrafo {#paragraph-styles}

![](assets/chlimage_1-30.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Toque o haga clic en el botón **Agregar** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrará en el cuadro de diálogo de edición.
* Para eliminar un estilo, toque o haga clic en el botón **Eliminar** .
* Para reorganizar el orden de los formatos, toque o haga clic y arrastre los controladores.

### Caracteres especiales {#special-characters}

![](assets/chlimage_1-31.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Agregar** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrará en el cuadro de diálogo de edición.
* Para eliminar un carácter, toque o haga clic en el botón **Eliminar** .
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controladores.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.
