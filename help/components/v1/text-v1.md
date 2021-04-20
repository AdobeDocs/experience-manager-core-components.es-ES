---
title: Componente de texto (v1)
description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 3%

---


# Componente de texto (v1) {#text-component-v}

El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido robusto que permite editar texto fácilmente en un editor en línea simplificado, así como en un formato de pantalla completa.

El [cuadro de diálogo de edición](#edit-dialog) incluye edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición en pantalla completa. Mediante el [cuadro de diálogo de diseño](#design-dialog), se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente de texto, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de v1 del componente de texto.

| Versión de AEM | Componente de texto v1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente de texto.
>
>Para obtener más información sobre la versión actual del componente de texto, consulte el documento [Componente de texto](/help/components/text.md).

## Salida de componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1-27.png)

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales v1](/help/versions.md) para obtener más información.

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que un usuario esperaría para componer texto.

![](/help/assets/chlimage_1-52.png)

* Negrita

   ![](/help/assets/chlimage_1-53.png)

   Se utiliza para aplicar formato de negrita al texto seleccionado o para dar formato negrita al texto introducido después del cursor.

   **Ctrl+** Bcan se puede utilizar como método abreviado de teclado.

* Cursiva

   ![](/help/assets/chlimage_1-54.png)

   Se utiliza para aplicar formato en cursiva al texto seleccionado o para aplicar cursiva al texto introducido después del cursor.

   **Ctrl+** Ipuede utilizarse como método abreviado de teclado.

* Subrayado

   ![](/help/assets/chlimage_1-55.png)

   Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

   **Ctrl+** Upuede utilizarse como método abreviado de teclado.

* Subíndice

   ![](/help/assets/chlimage_1-56.png)

   Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

* Superíndice

   ![](/help/assets/chlimage_1-57.png)

   Se utiliza para dar formato de superíndice al texto seleccionado o al texto introducido después del cursor.

* Pegar como texto

   ![](/help/assets/chlimage_1-58.png)

   Pega cualquier texto copiado como texto sin formato sin formato.

   Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar como texto sin formato sin formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación y cancele la acción tocando o haciendo clic en la x.

   ![](/help/assets/chlimage_1-59.png)

* Pegar desde Word

   ![](/help/assets/chlimage_1-60.png)

   Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar manteniendo su formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación y cancele la acción tocando o haciendo clic en la x.

   ![](/help/assets/chlimage_1-61.png)

* Hipervínculo

   ![](/help/assets/chlimage_1-62.png)

   Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando ya se ha seleccionado texto y abre una ventana con opciones adicionales para configurar el vínculo.

   ![](/help/assets/chlimage_1-63.png)

   * Introduzca la ubicación

      * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
      * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta (las rutas no absolutas se interpretan como relativas a AEM)
   * Escriba un texto descriptivo alternativo para el vínculo
   * Seleccionar el comportamiento del vínculo

      * Destino
      * Misma ficha
      * Nueva ficha
      * Marco principal
      * Marco superior

   Toque o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

* Desvincular

   ![](/help/assets/chlimage_1-64.png)

   Utilice esta opción para quitar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

* Buscar

   ![](/help/assets/chlimage_1-65.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda.

   ![](/help/assets/chlimage_1-66.png)

   Escriba el texto que desee buscar y toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Match Case** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, esta se resalta y el cuadro de diálogo de búsqueda se atenúa. Toque o haga clic de nuevo en el botón **Find** del cuadro de diálogo tenue para buscar la siguiente aparición.

   ![](/help/assets/chlimage_1-67.png)

   Si no se encuentran más ocurrencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

   ![](/help/assets/chlimage_1-68.png)

* Reemplazar

   ![](/help/assets/chlimage_1-69.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazar las coincidencias por otra cadena. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda y reemplazo.

   ![](/help/assets/chlimage_1-70.png)

   Introduzca el texto para el que desea buscar, así como el texto con el que debe reemplazarse.

   Toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

   Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Match Case** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, esta se resalta y el cuadro de diálogo de búsqueda se atenúa. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo tenue para buscar la siguiente aparición o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Replace** solo está activo una vez que se ha realizado una coincidencia.

   Seleccione **Reemplazar todo** para reemplazar todas las apariciones del texto a la vez.

* Alinear texto a la izquierda

   ![](/help/assets/chlimage_1-71.png)

   Se utiliza para alinear el texto con el margen izquierdo.

* Centrar texto

   ![](/help/assets/chlimage_1-72.png)

   Se utiliza para centrar el texto.

* Alinear texto a la derecha

   ![](/help/assets/chlimage_1-73.png)

   Se utiliza para alinear el texto con el margen derecho.

* Viñeta

   ![](/help/assets/chlimage_1-74.png)

   Se utiliza para dar formato al texto seleccionado como una lista con viñetas o comenzar la inserción de una lista con viñetas después del cursor.

   Para finalizar una lista con viñetas, toque o haga clic en el botón **Bullet** de nuevo o introduzca dos retornos de carro.

* Numerado

   ![](/help/assets/chlimage_1-75.png)

   Se utiliza para dar formato al texto seleccionado como una lista numerada o comenzar la inserción de una lista numerada después del cursor.

   Para finalizar una lista numerada, toque o haga clic en el botón **Numerado** de nuevo o introduzca dos retornos de carro.

* Anular sangría

   ![](/help/assets/chlimage_1-76.png)

   Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

   Solo activa si el texto o la posición seleccionados del cursor ya tienen sangría.

* Sangría

   ![](/help/assets/chlimage_1-77.png)

   Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

* Tabla

   ![](/help/assets/chlimage_1-78.png)

   Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abre una ventana para especificar los detalles de la tabla.

   ![](/help/assets/chlimage_1-79.png)

   * **Columnas** : el número de columnas de la tabla (obligatorio)
   * **Filas** : el número de filas de la tabla (obligatorio).
   * **Anchura** : Ancho de la tabla
   * **Altura** : altura de la tabla
   * **Margen de** celdas: el espacio alrededor del contenido de la celda
   * **Espaciado de celdas** : el espacio entre celdas
   * **Borde** : el peso de las líneas de borde de la tabla.
   * Si para el encabezado de la tabla:

      * La primera fila debe usarse
      * La primera columna debe usarse
      * La primera fila y la primera columna deben usarse
      * O no se debe utilizar ningún encabezado.
   * **Rótulo** : el rótulo de la tabla.


* Revisar ortografía

   ![](/help/assets/chlimage_1-80.png)

   Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se subrayan con líneas rojas rotas y rotas.

* Caracteres especiales

   ![](/help/assets/chlimage_1-81.png)

   Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana en la que se muestran los caracteres disponibles.

   ![](/help/assets/chlimage_1-82.png)

   Toque o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

* Modificar código fuente

   ![](/help/assets/chlimage_1-83.png)

   Se utiliza para ver y modificar el origen HTML del texto.

   Toque o haga clic en el icono **Source Edit** para cambiar el contenido del texto desde la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic en el icono **Source Edit** de nuevo para volver a la vista con formato.

   >[!CAUTION]
   >
   >Como siempre con acceso a HTML sin procesar, se debe tener cuidado al utilizar la opción **Source Edit**.
   >
   >
   >El HTML introducido mediante **Source Edit** se analiza para detectar riesgos XSS y todos los scripts insertados se eliminan y no aparecen en la página resultante. Sin embargo, el HTML mal formado introducido en **Source Edit** puede romper la plantilla de la página, lo que da como resultado un formato inesperado o que la página resultante quede inutilizable.

* Formato de párrafo

   ![](/help/assets/chlimage_1-84.png)

   Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción, se abre una lista desplegable en la que se selecciona el formato de párrafo.

   ![](/help/assets/chlimage_1-85.png)

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![](/help/assets/chlimage_1-86.png)

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Características {#features}

![](/help/assets/chlimage_1-28.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pasado desde la palabra
* Buscar y reemplazar
* Corrector ortográfico
* Edición de origen

### Formato {#formatting}

![](/help/assets/chlimage_1-29.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas
* Alineación
* Negrita, cursiva, subrayado
* Vínculos
* Subíndice/superíndice

### Estilos de párrafo {#paragraph-styles}

![](/help/assets/chlimage_1-30.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Toque o haga clic en el botón **Add** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un estilo, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los formatos, toque o haga clic en y arrastre los controladores.

### Caracteres especiales {#special-characters}

![](/help/assets/chlimage_1-31.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Add** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un carácter, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los caracteres, toque o haga clic en y arrastre los controladores.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
