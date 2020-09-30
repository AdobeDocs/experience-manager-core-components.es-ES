---
title: Componente de texto
description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye edición in-situ.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de texto{#text-component}

El componente de texto del componente principal es un componente de composición y edición de texto enriquecido que incluye edición in situ.

## Uso {#usage}

El componente de texto oferta un potente editor de texto enriquecido que permite una edición de texto sencilla en un editor en línea simplificado y en un formato de pantalla completa.

El cuadro de diálogo [de](#edit-dialog) edición incluye edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición a pantalla completa. Mediante el cuadro de diálogo [de](#design-dialog)diseño, se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de texto es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/text-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente de texto y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_text)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_text_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## El componente de texto y el editor de texto enriquecido {#the-text-component-and-the-rich-text-editor}

El componente de texto Componentes principales aprovecha el Editor de texto enriquecido AEM (RTE). RTE proporciona a los autores de contenido una amplia gama de funciones para editar su contenido de texto. El RTE es muy flexible en su configuración y oferta una serie de opciones. Encontrará más información sobre cómo se puede configurar RTE en los artículos [Configurar el editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) de texto enriquecido y [Configurar los complementos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)del editor de texto enriquecido.

El resto de este artículo muestra la configuración estándar del componente de texto de componentes principales con la configuración RTE lista para usar.

>[!NOTE]
>
>En el componente de texto solo están disponibles las opciones activadas por las configuraciones de [IU de RTE](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) .

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición oferta las herramientas de formato de texto enriquecido estándar que un usuario espera que compongan texto.

![Cuadro de diálogo de edición del componente de texto](/help/assets/text-edit.png)

### Negrita

![Icono de negrita](/help/assets/text-bold.png)

Se utiliza para aplicar formato de negrita al texto seleccionado o para aplicar formato negrita al texto introducido después del cursor.

**Ctrl+B** se puede utilizar como método abreviado de teclado.

### Cursiva

![Icono cursiva](/help/assets/text-italic.png)

Se utiliza para aplicar formato en cursiva al texto seleccionado o texto en cursiva introducido después del cursor.

**Ctrl+I** se puede utilizar como método abreviado de teclado.

### Subrayado

![Icono Subrayado](/help/assets/text-underline.png)

Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

**Ctrl+U** se puede utilizar como método abreviado de teclado.

### Subíndice

![Icono de subíndice](/help/assets/text-subscript.png)

Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

### Superíndice

![Icono Superíndice](/help/assets/text-superscript.png)

Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como superíndice.

### Pegar como texto

![Pegar como icono de texto](/help/assets/text-paste-text.png)

Pega el texto copiado como texto sin formato sin ningún formato.

Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar como texto sin formato sin formato como previsualización antes de insertarlo en el texto. Acepte tocando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Pegar como ejemplo de texto](/help/assets/text-paste-text-example.png)

### Pegar desde Word

![Pegar desde el icono de Word](/help/assets/text-paste-word.png)

Al seleccionar esta opción, se abre una ventana en la que se puede pegar el texto manteniendo su formato como previsualización antes de insertarlo en el texto. Acepte tocando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Ejemplo de Pegar desde Word](/help/assets/text-paste-word-example.png)

### Hipervínculo

![Icono de hipervínculo](/help/assets/text-hyperlink.png)

Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando el texto ya está seleccionado y abre una ventana con opciones adicionales para configurar el vínculo.

![Ejemplo de hipervínculo](/help/assets/text-hyperlink-example.png)

* Introduzca la ruta
   * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
   * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta
      * Las rutas no absolutas se interpretan como relativas a AEM
* Escriba un texto descriptivo alternativo para el vínculo
* Seleccionar comportamiento de vínculo
   * Destino
   * Misma ficha
   * Nueva ficha
   * Marco principal
   * Marco superior

   Toque o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

### Desvincular

![Icono Desvincular](/help/assets/text-unlink.png)

Utilice esta opción para eliminar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

### Buscar

![Icono Buscar](/help/assets/text-find.png)

Utilice esta opción para buscar en el texto la aparición de una cadena de texto especificada. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda.

![Ejemplo de búsqueda](/help/assets/text-find-example.png)

Escriba el texto para el cual desee buscar y toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.
Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidir mayúsculas y minúsculas** antes de iniciar la búsqueda.
Si se encuentra una coincidencia, ésta se resalta y el cuadro de diálogo de búsqueda se atenúa. Toque o haga clic en el botón **Buscar** de nuevo en el cuadro de diálogo atenuado para buscar la siguiente incidencia.

![Encontrar ejemplo](/help/assets/text-find-example-found.png)

Si no se encuentran más incidencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

![Buscar ejemplo sin más ocurrencias](/help/assets/text-find-example-found-end.png)

### Reemplazar

![Reemplazar icono](/help/assets/text-replace.png)

Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazar las coincidencias por otra cadena. Al seleccionar esta opción se abre una ventana para especificar las opciones de búsqueda y reemplazo.

![Reemplazar ejemplo](/help/assets/text-replace-example.png)

Escriba el texto para el que desea buscar, así como el texto con el que debe reemplazarse.

* Toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.
* Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Coincidir mayúsculas y minúsculas** antes de iniciar la búsqueda.
* Seleccione **Reemplazar todo** para reemplazar todas las apariciones del texto a la vez.

Si se encuentra una coincidencia, ésta se resalta y el cuadro de diálogo de búsqueda se atenúa. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente incidencia o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Reemplazar** solo está activo una vez que se ha realizado una coincidencia.

El cuadro de diálogo Buscar y reemplazar se vuelve transparente cuando se hace clic en Buscar y se vuelve opaco cuando se hace clic en reemplazar. Esto permite al autor revisar el texto que sustituirá.

>[!NOTE]
>
>Al utilizar la funcionalidad de reemplazo, la cadena de reemplazo que se va a reemplazar debe introducirse al mismo tiempo que la cadena de búsqueda. Sin embargo, puede seguir haciendo clic en buscar para buscar la cadena antes de reemplazarla. Si se introduce la cadena de reemplazo después de hacer clic en Buscar, la búsqueda se restablece al principio del texto.


### Alinear texto a la izquierda

![Icono Alinear a la izquierda](/help/assets/text-left.png)

Se utiliza para alinear el texto con el margen izquierdo.

### Centrar texto

![Icono Centrar texto](/help/assets/text-center.png)

Se utiliza para centrar el texto.

### Alinear texto a la derecha

![Icono Alinear a la derecha](/help/assets/text-right.png)

Se utiliza para alinear el texto con el margen derecho.

### Viñeta

![Icono de viñeta](/help/assets/text-bullet.png)

Se utiliza para dar formato al texto seleccionado como una lista con viñetas o iniciar la inserción de una lista con viñetas después del cursor.

Para finalizar una lista con viñetas, toque o haga clic de nuevo en el botón **Viñeta** o introduzca dos retornos de carro.

### Numerado

![Icono de lista numerada](/help/assets/text-numbered.png)

Se utiliza para dar formato al texto seleccionado como una lista numerada o para comenzar la inserción de una lista numerada después del cursor.

Para finalizar una lista numerada, toque o haga clic de nuevo en el botón **Numerado** o introduzca dos retornos de carro.

### Anular sangría

![Icono de Anular sangría](/help/assets/text-outdent.png)

Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

Solo se activa si el texto o la posición seleccionados del cursor ya están sangrados.

### Sangría

![Icono de sangría](/help/assets/text-outdent.png)

Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

### Tabla

![Icono de tabla](/help/assets/text-table.png)

Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción se abre una ventana para especificar los detalles de la tabla.

![Ejemplo de tabla](/help/assets/text-table-example.png)

* **Columnas** : el número de columnas de la tabla (obligatorio)
* **Filas** : el número de filas de la tabla (obligatorio)
* **Anchura** : anchura de la tabla
* **Altura** : altura de la tabla
* **Relleno** de celdas: el espacio alrededor del contenido de la celda
* **Espaciado** de celdas: el espacio entre celdas
* **Borde** : peso de las líneas de borde de la tabla
   * Si para el encabezado de la tabla:
      * Se debe utilizar la primera fila
      * Debe utilizarse la primera columna
      * Debe utilizarse la primera fila y la primera columna
      * O bien, no se debe utilizar ningún encabezado.
* **Rótulo** : el rótulo de la tabla

### Revisar ortografía

![Revisar el icono ortográfico](/help/assets/text-spellcheck.png)

Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se ven subrayados con líneas rojas rotas rotas.

Encontrará más información sobre la revisión ortográfica y la personalización de los diccionarios de revisión ortográfica en el documento [Configurar los complementos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)del editor de texto enriquecido.

### Caracteres especiales {#special-characters}

![Icono de caracteres especiales](/help/assets/text-special-characters.png)

Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana donde se muestran los caracteres disponibles.

![Ejemplo de caracteres especiales](/help/assets/text-special-characters-example.png)

Toque o haga clic en el carácter que desee para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

### Modificar código fuente

![Icono de edición de origen](/help/assets/text-source.png)

Se utiliza para vista y modificación del origen HTML del texto.

Toque o haga clic en el icono Editar **** origen para cambiar el contenido del texto de la vista con formato a la vista del HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic de nuevo en el icono Editar **** origen para volver a la vista con formato.

>[!CAUTION]
>
>Como siempre sucede con el acceso a HTML sin procesar, hay que tener cuidado al usar la opción Editar **** origen.
>
>El código HTML introducido mediante la edición **de** código fuente se analiza para detectar riesgos XSS y las secuencias de comandos insertadas se eliminan y no aparecerán en la página resultante. Sin embargo, el HTML mal formado introducido en la edición **de** origen puede dañar la plantilla de la página, lo que da como resultado un formato inesperado o que la página resultante quede inutilizable.

>[!NOTE]
>
>Dado que el HTML introducido mediante la edición **de** origen se analiza para detectar riesgos XSS y cualquier secuencia de comandos y elimina automáticamente los encontrados, el contenido real que se mantenga puede variar de lo que se introdujo en la edición **de** origen. Por este motivo, para guardar los cambios realizados con Edición **** de origen, primero debe salir de Editar **** origen para vista del texto en el editor normal antes de guardarlo.

### Formato de párrafo

![Icono de formato de párrafo](/help/assets/text-paragraph.png)

Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar estas opciones se abre una lista desplegable desde la que se selecciona el formato de párrafo.

![Ejemplo de formato de párrafo](/help/assets/text-paragraph-example.png)

### Edición en línea {#in-line-editing}

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![Ejemplo de edición en línea](/help/assets/text-edit-inline-example.png)

### Configuración e ID {#setting-id}

Esta opción permite controlar el identificador único del componente en el HTML y en la capa [](/help/developing/data-layer/overview.md)de datos.

* Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Ficha Complementos {#plugins-tab}

La ficha Complementos se utiliza para habilitar y deshabilitar varias opciones de formato de texto disponibles para los autores de contenido.

### Características {#features}

![Funciones del cuadro de diálogo Diseño](/help/assets/text-design-features.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pasado de la palabra
* Buscar y reemplazar
* Corrector ortográfico
* Opciones de modificación de imágenes insertadas
* Edición de código HTML

### Formato {#formatting}

![Formato del cuadro de diálogo Diseño](/help/assets/text-design-formatting.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas (viñeta, número, sangría, sangría)
* Alineación (izquierda, derecha, centrada)
* Negrita, cursiva, subrayado
* Vinculación (y desvinculación)
* Subíndice/superíndice

### Estilos de párrafo {#paragraph-styles}

![Estilos de párrafo del cuadro de diálogo Diseño](/help/assets/text-design-paragraph.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Toque o haga clic en el botón **Añadir** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrará en el cuadro de diálogo de edición.
* Para eliminar un estilo, toque o haga clic en el botón **Eliminar** .
* Para reorganizar el orden de los formatos, toque o haga clic y arrastre los controladores.

### Caracteres especiales {#configuring-special-characters}

![Caracteres especiales del cuadro de diálogo Diseño](/help/assets/text-design-special-characters.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Añadir** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrará en el cuadro de diálogo de edición.
* Para eliminar un carácter, toque o haga clic en el botón **Eliminar** .
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controladores.

## Ficha Estilos {#styles-tab}

El componente Texto admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
