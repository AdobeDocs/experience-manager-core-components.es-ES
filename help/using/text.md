---
title: Componente de texto
seo-title: Componente de texto
description: El componente de texto es un componente de compositor y edición enriquecido que incluye edición in-situ.
seo-description: El componente de texto es un componente de compositor y edición enriquecido que incluye edición in-situ.
uuid: 5 f 8 eee 8 f -7317-4712-a 77 f-e 34 e 8 a 024187
contentOwner: Usuario
content-type: referencia
topic-tags: componentes principales
discoiquuid: 9 a 290584-565 e -4392-999 c -999 ee 4 a 93 da 1
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Componente de texto{#text-component}

El componente de texto de componente principal es un componente de edición y edición enriquecido que incluye edición in-situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido sólido que permite editar texto fácilmente en un editor en línea simplificado, así como en un formato de pantalla completa.

El cuadro de diálogo [de edición](#edit-dialog) incluye la edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición de pantalla completa. Con el cuadro de diálogo [de diseño](#design-dialog), se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla para el autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de texto es v 2, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](text-v1.md) | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

A continuación se muestra una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/chlimage_1-27.png)

### Biblioteca de componentes

Para experimentar el componente de texto, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/text.html).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Componente de texto y Editor de texto enriquecido {#the-text-component-and-the-rich-text-editor}

El componente de texto de componentes principales aprovecha el editor de texto enriquecido AEM (RTE). RTE proporciona a los autores de contenido una amplia gama de funcionalidades para editar su contenido de texto. RTE es muy flexible en su configuración y ofrece diversas opciones. En los artículos puede encontrar más detalles sobre cómo se puede configurar RTE en los artículos [Configurar el editor de texto enriquecido](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/rich-text-editor.html) y [configurar los complementos del Editor de texto enriquecido](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

El resto de este artículo muestra la configuración estándar del componente de texto de componentes principales con la configuración predeterminada de RTE.

>[!NOTE]
>
>En el componente Texto solo están disponibles las opciones activadas por [configuraciones de IU de RTE](https://chl-author-preview.corp.adobe.com/content/help/en/experience-manager/6-5/sites/administering/using/rich-text-editor.html) .

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que un usuario espera componer texto.

![](assets/screen_shot_2018-01-11at143025.png)

### Negrita

![](assets/screen_shot_2018-01-11at125602.png)

Se utiliza para aplicar formato de negrita al texto seleccionado o al texto de formato negrita que se introduce después del cursor.

**Ctrl + B** se puede utilizar como método abreviado de teclado.

### Cursiva

![](assets/screen_shot_2018-01-11at125609.png)

Se utiliza para aplicar formato en cursiva al texto en cursiva o texto seleccionado tras el cursor.

**Ctrl + I** se puede utilizar como método abreviado de teclado.

### Subrayado

![](assets/screen_shot_2018-01-11at125615.png)

Se utiliza para aplicar el formato subrayado al texto seleccionado o para subrayar el texto especificado después del cursor.

**Ctrl + U** se puede utilizar como método abreviado de teclado.

### Subíndice

![](assets/screen_shot_2018-01-11at125703.png)

Se utiliza para dar formato al texto o texto seleccionado después del cursor como subíndice.

### Superíndice

![](assets/screen_shot_2018-01-11at125708.png)

Se utiliza para dar formato al texto o texto seleccionado después del cursor como superíndice.

### Pegar como texto

![](assets/screen_shot_2018-01-11at125713.png)

Pega cualquier texto copiado como texto sin formato sin ningún formato.

Al seleccionar esta opción, se abre una ventana donde el texto se puede pegar como texto sin formato sin formato como vista previa antes de insertarse en el texto. Para aceptar o hacer clic en la marca de verificación, toque o haga clic en la x.

![](assets/screen_shot_2018-01-11at143234.png)

### Pegar desde Word

![](assets/screen_shot_2018-01-11at125717.png)

Al seleccionar esta opción, se abre una ventana donde se puede pegar el texto manteniendo su formato como vista previa antes de insertarlo en el texto. Para aceptar o hacer clic en la marca de verificación, toque o haga clic en la x.

![](assets/screen_shot_2018-01-11at143250.png)

### Hipervínculo

![](assets/screen_shot_2018-01-11at125839.png)

Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando el texto ya está seleccionado y abre una ventana con opciones adicionales para configurar el vínculo.

![](assets/screen_shot_2018-01-11at130003.png)

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

### Desvincular

![](assets/screen_shot_2018-01-11at125901.png)

Utilice esta opción para eliminar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando un vínculo ya está seleccionado.

### Buscar

![](assets/screen_shot_2018-01-11at125906.png)

Utilice esta opción para buscar en el texto una cadena de texto especificada. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda.

![](assets/screen_shot_2018-01-11at130107.png)

Escriba el texto para el que desea buscar y tocar, o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.
Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidencia entre mayúsculas y minúsculas** antes de iniciar la búsqueda.
Si se encuentra una coincidencia, se resalta y el cuadro de diálogo de búsqueda aparece atenuado. Toque o haga clic en el **botón Buscar** de nuevo en el cuadro de diálogo atenuado para buscar la siguiente aparición.

![](assets/screen_shot_2018-01-11at130145.png)

Si no se encuentran ocurrencias adicionales, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

![](assets/screen_shot_2018-01-11at130241.png)

### Reemplazar

![](assets/screen_shot_2018-01-11at125910.png)

Utilice esta opción para buscar en el texto las incidencias de una cadena de texto específica y reemplazar las coincidencias con otra cadena. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda y reemplazo.

![](assets/screen_shot_2018-01-11at130441.png)

Escriba el texto para el que desea buscar así como el texto con el que debe reemplazarse.

Toque o haga clic **en Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.

Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidencia entre mayúsculas y minúsculas** antes de iniciar la búsqueda.

Si se encuentra una coincidencia, se resalta y el cuadro de diálogo de búsqueda aparece atenuado. Vuelva a hacer clic en **el** botón Buscar en el cuadro de diálogo atenuado para buscar la siguiente aparición o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y resaltado. Tenga en cuenta que **el** botón Reemplazar solo está activo cuando se realiza una coincidencia.

Seleccione **Reemplazar todo** para reemplazar todas las incidencias del texto a la vez.

### Alinear texto a la izquierda

![](assets/screen_shot_2018-01-11at142012.png)

Se utiliza para alinear el texto con el margen izquierdo.

### Centrar texto

![](assets/screen_shot_2018-01-11at142017.png)

Se utiliza para centrar el texto.

### Alinear texto a la derecha

![](assets/screen_shot_2018-01-11at142021.png)

Se utiliza para alinear el texto con el margen derecho.

### Viñeta

![](assets/screen_shot_2018-01-11at142025.png)

Se utiliza para dar formato al texto seleccionado como una lista con viñetas o empezar la inserción de una lista con viñetas después del cursor.

Para finalizar una lista con viñetas, toque o haga clic en el **botón Viñeta** de nuevo o introduzca dos retornos de carro.

### Numerado

![](assets/screen_shot_2018-01-11at142030.png)

Se utiliza para dar formato al texto seleccionado como una lista numerada o empezar la inserción de una lista numerada después del cursor.

Para finalizar una lista numerada, toque o haga clic en el **botón Numerado** de nuevo o introduzca dos retornos de carro.

### Anular sangría

![](assets/screen_shot_2018-01-11at141917.png)

Se utiliza para reducir el nivel de sangría del texto o texto seleccionado tras el cursor.

Solo activo si el texto o la posición seleccionados del cursor ya están sangrados.

### Sangría

![](assets/screen_shot_2018-01-11at141922.png)

Se utiliza para aumentar el nivel de sangría del texto o texto seleccionado tras el cursor.

### Tabla

![](assets/screen_shot_2018-01-11at141928.png)

Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abre una ventana para especificar los detalles de la tabla.

![](assets/screen_shot_2018-01-11at142405.png)

* **Columnas**
El número de columnas de la tabla (obligatorio)
* **Filas**
El número de filas de la tabla (obligatorio)
* **Anchura**
La anchura de la tabla
* **Altura**
La altura de la tabla
* **Margen
de celda** El espacio alrededor del contenido de la celda
* **Espaciado
de celdas** El espacio entre celdas
* **Borde**
El grosor de las líneas de borde de la tabla
* Si para el encabezado de la tabla:
   * Se debe utilizar la primera fila
   * Se debe utilizar la primera columna
   * Se debe utilizar la primera fila y la primera columna
   * O no debe usarse ningún encabezado.
* **Rótulo**
El rótulo de la tabla

### Revisar ortografía

![](assets/screen_shot_2018-01-11at141935.png)

Se utiliza para revisar la ortografía del contenido del texto. Los errores ortográficos pueden subrayarse con líneas rotas y rojas.

En el documento [encontrará más detalles sobre la revisión ortográfica y la personalización de diccionarios de revisión ortográfica](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

### Caracteres especiales {#special-characters}

![](assets/screen_shot_2018-01-11at142600.png)

Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana donde se muestran los caracteres disponibles.

![](assets/screen_shot_2018-01-11at142635.png)

Toque o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

### Modificar código fuente

![](assets/screen_shot_2018-01-11at142746.png)

Se utiliza para ver y modificar el origen HTML del texto.

Toque o haga clic en **el icono Editar** fuente para cambiar el contenido del texto de la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic **en el icono Editar** fuente para volver a la vista formateada.

>[!CAUTION]
>
>Como siempre sucede con el acceso a HTML sin procesar, se debe tener cuidado al utilizar **la opción Editar** fuente.
>
>El HTML especificado mediante **la edición** de origen se escanea para los riesgos XSS y las secuencias de comandos insertadas se eliminan y no aparecerán en la página resultante. Sin embargo, el HTML incorrecto introducido en **Editar** código fuente puede dañar la plantilla de la página como un formato inesperado o procesar la página resultante inutilizable.

>[!NOTE]
>
>Dado que HTML ingresado mediante **la edición** de origen se escanea para riesgos XSS y cualquier secuencia de comandos y elimina automáticamente los encontrados, el contenido real persistirá de acuerdo con lo introducido en **Editar fuente**. Por este motivo, para guardar los cambios realizados mediante **la Edición de origen**, primero debe salir **de Editar** código fuente para ver el texto en el editor normal antes de guardar.

### Formato de párrafo

![](assets/screen_shot_2018-01-11at142752.png)

Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción se abre una lista desplegable desde la que se selecciona el formato de párrafo.

![](assets/screen_shot_2018-01-11at142828.png)

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![](assets/screen_shot_2018-01-11at142921.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de formato de texto disponibles para los autores de contenido.

### Ficha Complementos {#plugins-tab}

La ficha Complementos se utiliza para habilitar y deshabilitar diversas opciones de formato de texto disponibles para los autores de contenido.

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

### Configuración de caracteres especiales {#configuring-special-characters}

![](assets/chlimage_1-31.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Una vez activados, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Agregar** para insertar un nuevo carácter.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para eliminar un toque de caracteres o haga clic en **el** botón Eliminar.
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controles.

## Ficha Estilos {#styles-tab}

El componente de texto admite el sistema [de estilos AEM](authoring.md#component-styling).