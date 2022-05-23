---
title: Componente Texto
description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.
role: Architect, Developer, Admin, User
exl-id: bcea202a-9ecb-4dcd-99b6-0848cbb9d500
source-git-commit: c041439e31a7da62739b6d5130c52dea36662a0c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 100%

---

# Componente Texto{#text-component}

El componente Texto del componente principal es un componente de composición y edición de texto enriquecido que incluye la edición in situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido robusto que permite editar texto fácilmente en un editor en línea simplificado, así como en formato de pantalla completa.

El [cuadro de diálogo de edición](#edit-dialog) incluye la edición en línea con opciones limitadas con la funcionalidad completa disponible en el cuadro de diálogo de edición en pantalla completa. Mediante el [cuadro de diálogo de diseño](#design-dialog) se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Texto es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| Versión 2 | Compatible  con la <br>[versión 2.17.4](/help/versions.md) y anterior | Compatible | Compatible |
| [Versión 1](v1/text-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Texto y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_text_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Texto [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_text_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## El componente Texto y el editor de texto enriquecido {#the-text-component-and-the-rich-text-editor}

El componente Texto de los componentes principales aprovecha el Editor de texto enriquecido de AEM (RTE). El RTE proporciona a los autores de contenido una amplia gama de funciones para editar su contenido de texto. El RTE es muy flexible en su configuración y ofrece una serie de opciones. Puede encontrar más información sobre cómo se puede configurar el RTE en los artículos [Configurar el editor de texto enriquecido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html?lang=es) y [Configurar los complementos del editor de texto enriquecido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=es).

El resto de este artículo muestra la configuración estándar del componente Texto de componentes principales con la configuración del RTE predeterminada.

>[!NOTE]
>
>En el componente Texto solo están disponibles las opciones activadas por las [configuraciones de interfaz de usuario de RTE](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que esperaría un usuario para componer textos.

![Cuadro de diálogo de edición del componente Texto](/help/assets/text-edit.png)

### Negrita

![Icono de negrita](/help/assets/text-bold.png)

Se utiliza para aplicar formato de negrita al texto seleccionado o para dar formato negrita al texto introducido después del cursor.

**Ctrl+B** se puede utilizar como método abreviado de teclado.

### Cursiva

![Icono de cursiva](/help/assets/text-italic.png)

Se utiliza para aplicar formato de cursiva al texto seleccionado o para aplicar cursiva al texto introducido después del cursor.

**Ctrl+I** puede utilizarse como método abreviado de teclado.

### Subrayado

![Icono de subrayado](/help/assets/text-underline.png)

Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

**Ctrl+U** puede utilizarse como método abreviado de teclado.

### Subíndice

![Icono de subíndice](/help/assets/text-subscript.png)

Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

### Superíndice

![Icono de superíndice](/help/assets/text-superscript.png)

Se utiliza para dar formato de superíndice al texto seleccionado o al texto introducido después del cursor.

### Pegar como texto

![Pegar como icono de texto](/help/assets/text-paste-text.png)

Pega cualquier texto copiado como texto sin formato.

Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar como texto sin formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Pegar como ejemplo de texto](/help/assets/text-paste-text-example.png)

### Pegar desde Word

![Pegar desde el icono de Word](/help/assets/text-paste-word.png)

Al seleccionar esta opción, se abrirá una ventana en la que el texto se puede pegar manteniendo su formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Pegar desde el ejemplo de Word](/help/assets/text-paste-word-example.png)

### Hipervínculo

![Icono de hipervínculo](/help/assets/text-hyperlink.png)

Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando ya se ha seleccionado el texto y se abre una ventana con opciones adicionales para configurar el vínculo.

![Ejemplo de hipervínculo](/help/assets/text-hyperlink-example.png)

* Especifique la ruta
   * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
   * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta
      * Las rutas no absolutas se interpretan como relativas a AEM
* Escriba un texto descriptivo alternativo para el vínculo
* Seleccione el comportamiento del vínculo
   * Destino
   * Misma pestaña
   * Nueva pestaña
   * Marco principal
   * Marco superior

   Pulse o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

### Desvincular

![Icono de desvincular](/help/assets/text-unlink.png)

Utilice esta opción para quitar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

### Buscar

![Icono de buscar](/help/assets/text-find.png)

Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda.

![Buscar ejemplo](/help/assets/text-find-example.png)

Escriba el texto que quiera buscar y toque o haga clic en **Buscar** para comenzar. Pulse o haga clic en la x para cancelar.
Si desea buscar una coincidencia exacta teniendo en cuenta las minúsculas y las mayúsculas, seleccione la opción **Coincidir minúsculas y mayúsculas** antes de iniciar la búsqueda.
Si se encuentra una coincidencia, esta se resaltará y el cuadro de diálogo de búsqueda se atenuará. Pulse o haga clic de nuevo en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente ocurrencia.

![Buscar ejemplo](/help/assets/text-find-example-found.png)

Si no se encuentran más ocurrencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

![Buscar ejemplo no más ocurrencias](/help/assets/text-find-example-found-end.png)

### Reemplazar

![Icono de reemplazar](/help/assets/text-replace.png)

Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazarlas por otra cadena. Al seleccionar esta opción, se abrirá una ventana para especificar las opciones de búsqueda y de reemplazo.

![Reemplazar ejemplo](/help/assets/text-replace-example.png)

Introduzca el texto para que quiera buscar, así como el texto con el que debe reemplazarse.

* Pulse o haga clic en **Buscar** para comenzar la búsqueda. Pulse o haga clic en la x para cancelar.
* Si desea buscar una coincidencia exacta teniendo en cuenta las minúsculas y las mayúsculas, seleccione la opción **Coincidir minúsculas y mayúsculas** antes de iniciar la búsqueda.
* Seleccione **Reemplazar todo** para reemplazar todas las apariciones del texto a la vez.

Si se encuentra una coincidencia, esta se resaltará y el cuadro de diálogo de búsqueda se atenuará. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo atenuado para buscar la siguiente ocurrencia o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Reemplazar** solo estará activo una vez que se haya encontrado una coincidencia.

El cuadro de diálogo buscar y reemplazar se volverá transparente cuando se haga clic en buscar y se volverá opaco cuando se haga clic en reemplazar. Esto permitirá al autor revisar el texto que reemplazará.

>[!NOTE]
>
>Al utilizar la funcionalidad de reemplazo, la cadena de reemplazo que se va a reemplazar debe introducirse al mismo tiempo que la cadena de búsqueda. Sin embargo, puede hacer clic en Buscar para buscar la cadena antes de reemplazarla. Si se introduce la cadena de reemplazo después de hacer clic en Buscar, la búsqueda se restablecerá al principio del texto.


### Alinear texto a la izquierda

![Icono de alinear a la izquierda](/help/assets/text-left.png)

Se utiliza para alinear el texto con el margen izquierdo.

### Centrar texto

![Icono de centrar texto](/help/assets/text-center.png)

Se utiliza para centrar el texto.

### Alinear texto a la derecha

![Icono de alinear a la derecha](/help/assets/text-right.png)

Se utiliza para alinear el texto con el margen derecho.

### Viñeta

![Icono de viñeta](/help/assets/text-bullet.png)

Se utiliza para dar formato al texto seleccionado como una lista con viñetas o comenzar la inserción de una lista con viñetas después del cursor.

Para finalizar una lista con viñetas, toque o haga clic en el botón **Viñeta** de nuevo o introduzca dos retornos de carro.

### Numeración

![Icono de lista numerada](/help/assets/text-numbered.png)

Se utiliza para dar formato al texto seleccionado como una lista numerada o comenzar la inserción de una lista numerada después del cursor.

Para finalizar una lista numerada, toque o haga clic en el botón **Numeración** de nuevo o introduzca dos retornos de carro.

### Anular sangría

![Icono de anular la selección](/help/assets/text-outdent.png)

Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

Solo se activará si el texto o la posición seleccionados del cursor ya tienen sangría.

### Sangría

![Icono de sangría](/help/assets/text-indent.png)

Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

### Tabla

![Icono de tabla](/help/assets/text-table.png)

Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abrirá una ventana para especificar los detalles de la tabla.

![Ejemplo de tabla](/help/assets/text-table-example.png)

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

### Revisar ortografía

![Revisar el icono ortográfico](/help/assets/text-spellcheck.png)

Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se subrayarán con líneas rojas y rotas.

Para obtener más información sobre la revisión ortográfica y la personalización de los diccionarios de revisión ortográfica, consulte el documento [Configurar los complementos del editor de texto enriquecido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

### Caracteres especiales {#special-characters}

![Icono de caracteres especiales](/help/assets/text-special-characters.png)

Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abrirá una ventana en la que se mostrarán los caracteres disponibles.

![Ejemplo de caracteres especiales](/help/assets/text-special-characters-example.png)

Pulse o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Pulse o haga clic en la x para cerrar la ventana de selección.

### Modificar código fuente

![Icono de modificar el código fuente](/help/assets/text-source.png)

Se utiliza para ver y modificar el origen HTML del texto.

Pulse o haga clic en el icono **Modificar código fuente** para cambiar el contenido del texto desde la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Pulse o haga clic en el icono **Modificar código fuente** de nuevo para volver a la vista con formato.

>[!CAUTION]
>
>Como siempre, con el acceso al HTML sin procesar, se debe tener cuidado al utilizar la opción **Modificar código fuente**.
>
>El HTML introducido mediante **Modificar código fuente** se analizará para detectar riesgos XSS y todos los scripts insertados se eliminarán y no aparecerán en la página resultante. Sin embargo, el HTML mal formado introducido en **Modificar código fuente** puede romper la plantilla de la página, dando como resultado un formato inesperado o que la página quede inutilizable.

>[!NOTE]
>
>Dado que el HTML introducido a través de **Modificar código fuente** se analiza para detectar riesgos XSS y cualquier script, y elimina automáticamente los que se encuentran, el contenido real que persiste puede variar de lo introducido en **Modificar código fuente**. Por este motivo, para guardar los cambios realizados con **Modificar código fuente**, primero debe salir de **Modificar código fuente** para ver el texto en el editor normal antes de guardarlo.

### Formato de párrafo

![Icono de formato de párrafo](/help/assets/text-paragraph.png)

Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción, se abrirá una lista desplegable en la que se selecciona el formato de párrafo.

![Ejemplo de formato de párrafo](/help/assets/text-paragraph-example.png)

### Edición en línea {#in-line-editing}

El componente Texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles. Para ver todas las opciones, cambie al modo de pantalla completa.

![Ejemplo de edición en línea](/help/assets/text-edit-inline-example.png)

### Configuración e ID {#setting-id}

Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Pestaña Plugins {#plugins-tab}

La pestaña Plugins se utiliza para habilitar y deshabilitar varias opciones de formato de texto disponibles para los autores de contenido.

### Características {#features}

![Diseño de las funciones del cuadro de diálogo](/help/assets/text-design-features.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pegar desde Word
* Buscar y reemplazar
* Corrector ortográfico
* Opciones de modificación de la imagen insertada
* Edición de código HTML

### Formato {#formatting}

![Formato del cuadro de diálogo de diseño](/help/assets/text-design-formatting.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas (viñeta, número, menos sangría, más sangría)
* Alineación (izquierda, derecha, centrado)
* Negrita, cursiva, subrayado
* Vinculación (y desvinculación)
* Subíndice/superíndice

### Estilos de párrafo {#paragraph-styles}

![Estilos de párrafo del cuadro de diálogo de diseño](/help/assets/text-design-paragraph.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Pulse o haga clic en el botón **Añadir** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un estilo, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los formatos, toque o haga clic y arrastre los controladores.

### Caracteres especiales {#configuring-special-characters}

![Caracteres especiales del cuadro de diálogo de diseño](/help/assets/text-design-special-characters.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Pulse o haga clic en el botón **Añadir** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un carácter, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los caracteres, toque o haga clic y arrastre los controladores.

## Pestaña Estilos {#styles-tab}

El componente Texto es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Texto es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
