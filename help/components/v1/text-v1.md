---
title: Componente Texto (versión 1)
description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.
index: n
role: Architect, Developer, Admin, User
exl-id: c9fe3052-a33d-412e-9456-52c9a0cea292
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '1657'
ht-degree: 100%

---

# Componente Texto (versión 1) {#text-component-v}

El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido robusto que permite editar texto fácilmente en un editor en línea simplificado, así como en formato de pantalla completa.

El [cuadro de diálogo de edición](#edit-dialog) incluye la edición en línea con opciones limitadas con la funcionalidad completa disponible en el cuadro de diálogo de edición en pantalla completa. Mediante el [cuadro de diálogo de diseño](#design-dialog) se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Texto, introducido originalmente con la versión 1.0.0 de los componentes principales con AEM 6.3.

La siguiente tabla enumera la compatibilidad de la versión 1 del componente Texto.

| Versión de AEM | Componente Texto versión 1 |
|--- |--- |
| 6.3 | Compatible |
| 6.4 | Compatible |

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Texto.
>
>Para obtener más información sobre la versión actual del componente Texto, consulte el documento [Componente Texto](/help/components/text.md).

## Salida del componente de ejemplo {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=es).

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
>La exportación de JSON desde los componentes principales requiere la versión 1.1.0 de los componentes principales. Consulte la [información de compatibilidad para los componentes principales (versión 1)](/help/versions.md) para obtener más información.

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que esperaría un usuario para componer textos.

![](/help/assets/chlimage_1-52.png)

* Negrita

   ![](/help/assets/chlimage_1-53.png)

   Se utiliza para aplicar formato de negrita al texto seleccionado o para dar formato negrita al texto introducido después del cursor.

   **Ctrl+B** se puede utilizar como método abreviado de teclado.

* Cursiva

   ![](/help/assets/chlimage_1-54.png)

   Se utiliza para aplicar formato de cursiva al texto seleccionado o para aplicar cursiva al texto introducido después del cursor.

   **Ctrl+I** puede utilizarse como método abreviado de teclado.

* Subrayado

   ![](/help/assets/chlimage_1-55.png)

   Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

   **Ctrl+U** puede utilizarse como método abreviado de teclado.

* Subíndice

   ![](/help/assets/chlimage_1-56.png)

   Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

* Superíndice

   ![](/help/assets/chlimage_1-57.png)

   Se utiliza para dar formato de superíndice al texto seleccionado o al texto introducido después del cursor.

* Pegar como texto

   ![](/help/assets/chlimage_1-58.png)

   Pega cualquier texto copiado como texto sin formato.

   Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar como texto sin formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación o cancele tocando o haciendo clic en la x.

   ![](/help/assets/chlimage_1-59.png)

* Pegar desde Word

   ![](/help/assets/chlimage_1-60.png)

   Al seleccionar esta opción, se abrirá una ventana en la que el texto se puede pegar manteniendo su formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación o cancele tocando o haciendo clic en la x.

   ![](/help/assets/chlimage_1-61.png)

* Hipervínculo

   ![](/help/assets/chlimage_1-62.png)

   Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando ya se ha seleccionado el texto y se abre una ventana con opciones adicionales para configurar el vínculo.

   ![](/help/assets/chlimage_1-63.png)

   * Introducir la ubicación

      * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
      * Si el vínculo no está en AEM, introduzca la dirección URL absoluta (las rutas no absolutas se interpretan como relativas a AEM)
   * Escriba un texto descriptivo alternativo para el vínculo
   * Seleccione el comportamiento del vínculo

      * Destino
      * Misma pestaña
      * Nueva pestaña
      * Marco principal
      * Marco superior

   Pulse o haga clic en la marca de verificación para aplicar el vínculo o en la x para cancelar.

* Desvincular

   ![](/help/assets/chlimage_1-64.png)

   Utilice esta opción para quitar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

* Buscar

   ![](/help/assets/chlimage_1-65.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda.

   ![](/help/assets/chlimage_1-66.png)

   Escriba el texto que quiera buscar y toque o haga clic en **Buscar** para comenzar. Pulse o haga clic en la x para cancelar.

   Si desea buscar una coincidencia exacta teniendo en cuenta las minúsculas y las mayúsculas, seleccione la opción **Coincidir minúsculas y mayúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, esta se resaltará y el cuadro de diálogo de búsqueda se atenuará. Pulse o haga clic de nuevo en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente ocurrencia.

   ![](/help/assets/chlimage_1-67.png)

   Si no se encuentran más ocurrencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

   ![](/help/assets/chlimage_1-68.png)

* Reemplazar

   ![](/help/assets/chlimage_1-69.png)

   Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazarlas por otra cadena. Al seleccionar esta opción, se abrirá una ventana para especificar las opciones de búsqueda y de reemplazo.

   ![](/help/assets/chlimage_1-70.png)

   Introduzca el texto para que quiera buscar, así como el texto con el que debe reemplazarse.

   Pulse o haga clic en **Buscar** para comenzar la búsqueda. Pulse o haga clic en la x para cancelar.

   Si desea buscar una coincidencia exacta teniendo en cuenta las minúsculas y las mayúsculas, seleccione la opción **Coincidir minúsculas y mayúsculas** antes de iniciar la búsqueda.

   Si se encuentra una coincidencia, esta se resaltará y el cuadro de diálogo de búsqueda se atenuará. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente ocurrencia o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Reemplazar** solo estará activo una vez que se haya encontrado una coincidencia.

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

   Para finalizar una lista con viñetas, toque o haga clic en el botón **Viñeta** de nuevo o introduzca dos retornos de carro.

* Numeración

   ![](/help/assets/chlimage_1-75.png)

   Se utiliza para dar formato al texto seleccionado como una lista numerada o comenzar la inserción de una lista numerada después del cursor.

   Para finalizar una lista numerada, toque o haga clic en el botón **Numeración** de nuevo o introduzca dos retornos de carro.

* Anular sangría

   ![](/help/assets/chlimage_1-76.png)

   Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

   Solo se activará si el texto o la posición seleccionados del cursor ya tienen sangría.

* Sangría

   ![](/help/assets/chlimage_1-77.png)

   Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

* Tabla

   ![](/help/assets/chlimage_1-78.png)

   Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abrirá una ventana para especificar los detalles de la tabla.

   ![](/help/assets/chlimage_1-79.png)

   * **Columnas**: el número de columnas de la tabla (obligatorio)
   * **Filas**: el número de filas de la tabla (obligatorio).
   * **Anchura**
La anchura de la tabla
   * **Altura**
La altura de la tabla
   * **Margen de celdas**: el espacio alrededor del contenido de la celda
   * **Espaciado de celdas**: el espacio entre celdas
   * **Borde**: el peso de las líneas de borde de la tabla.
   * Si para el encabezado de la tabla:

      * Debe usarse la primera fila
      * Debe usarse la primera columna
      * Debe usarse la primera fila y la primera columna
      * O no se debe utilizar ningún encabezado
   * **Pie**: el pie de la tabla.


* Revisar ortografía

   ![](/help/assets/chlimage_1-80.png)

   Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se subrayarán con líneas rojas y rotas.

* Caracteres especiales

   ![](/help/assets/chlimage_1-81.png)

   Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abrirá una ventana en la que se mostrarán los caracteres disponibles.

   ![](/help/assets/chlimage_1-82.png)

   Pulse o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Pulse o haga clic en la x para cerrar la ventana de selección.

* Modificar código fuente

   ![](/help/assets/chlimage_1-83.png)

   Se utiliza para ver y modificar el origen HTML del texto.

   Pulse o haga clic en el icono **Modificar código fuente** para cambiar el contenido del texto desde la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Pulse o haga clic en el icono **Modificar código fuente** de nuevo para volver a la vista con formato.

   >[!CAUTION]
   >
   >Como siempre, con el acceso al HTML sin procesar, se debe tener cuidado al utilizar la opción **Modificar código fuente**.
   >
   >
   >El HTML introducido mediante **Modificar código fuente** se analizará para detectar riesgos XSS y todos los scripts insertados se eliminarán y no aparecerán en la página resultante. Sin embargo, el HTML mal formado introducido en **Modificar código fuente** puede romper la plantilla de la página, dando como resultado un formato inesperado o que la página quede inutilizable.

* Formato de párrafo

   ![](/help/assets/chlimage_1-84.png)

   Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción, se abrirá una lista desplegable en la que se selecciona el formato de párrafo.

   ![](/help/assets/chlimage_1-85.png)

El componente Texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles. Para ver todas las opciones, cambie al modo de pantalla completa.

![](/help/assets/chlimage_1-86.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Características {#features}

![](/help/assets/chlimage_1-28.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pegar desde Word
* Buscar y reemplazar
* Corrector ortográfico
* Modificar el código fuente

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

* Pulse o haga clic en el botón **Añadir** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un estilo, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los formatos, toque o haga clic y arrastre los controladores.

### Caracteres especiales {#special-characters}

![](/help/assets/chlimage_1-31.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Pulse o haga clic en el botón **Añadir** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un carácter, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controladores.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Texto [se encuentra en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo el proyecto de componentes principales se puede descargar desde GitHub.

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).
