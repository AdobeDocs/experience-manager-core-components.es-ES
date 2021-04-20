---
title: Componente de texto
description: El componente Texto es un componente de composición y edición de texto enriquecido que incluye la edición in situ.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '2218'
ht-degree: 4%

---


# Componente de texto{#text-component}

El componente Texto de componente principal es un componente de composición y edición de texto enriquecido que incluye la edición in situ.

## Uso {#usage}

El componente Texto ofrece un editor de texto enriquecido robusto que permite editar texto fácilmente en un editor en línea simplificado, así como en un formato de pantalla completa.

El [cuadro de diálogo de edición](#edit-dialog) incluye edición en línea con opciones limitadas con funcionalidad completa disponible en el cuadro de diálogo de edición en pantalla completa. Mediante el [cuadro de diálogo de diseño](#design-dialog), se pueden configurar opciones de formato de texto como encabezados, caracteres especiales y estilos de párrafo para la plantilla del autor del contenido.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de texto es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/text-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida de componente de ejemplo {#sample-component-output}

Para experimentar el componente de texto, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_text).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de texto [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_text_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## El componente Texto y el editor de texto enriquecido {#the-text-component-and-the-rich-text-editor}

El componente Texto de componentes principales aprovecha el Editor de texto enriquecido AEM (RTE). RTE proporciona a los autores de contenido una amplia gama de funciones para editar su contenido de texto. El RTE es muy flexible en su configuración y ofrece una serie de opciones. Puede encontrar más información sobre cómo se puede configurar el RTE en los artículos [Configurar el editor de texto enriquecido](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) y [Configurar los complementos del editor de texto enriquecido](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

El resto de este artículo muestra la configuración estándar del componente de texto de componentes principales con la configuración RTE predeterminada.

>[!NOTE]
>
>En el componente Texto solo están disponibles las opciones activadas por las [configuraciones de interfaz de usuario de RTE](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) en .

## Editar cuadro de diálogo {#edit-dialog}

El cuadro de diálogo de edición ofrece las herramientas de formato de texto enriquecido estándar que un usuario esperaría para componer texto.

![Cuadro de diálogo de edición del componente de texto](/help/assets/text-edit.png)

### Negrita

![Icono Negrita](/help/assets/text-bold.png)

Se utiliza para aplicar formato de negrita al texto seleccionado o para dar formato negrita al texto introducido después del cursor.

**Ctrl+** Bcan se puede utilizar como método abreviado de teclado.

### Cursiva

![Icono de cursiva](/help/assets/text-italic.png)

Se utiliza para aplicar formato en cursiva al texto seleccionado o para aplicar cursiva al texto introducido después del cursor.

**Ctrl+** Ipuede utilizarse como método abreviado de teclado.

### Subrayado

![Icono Subrayado](/help/assets/text-underline.png)

Se utiliza para aplicar formato subrayado al texto seleccionado o para subrayar el texto introducido después del cursor.

**Ctrl+** Upuede utilizarse como método abreviado de teclado.

### Subíndice

![Icono de subíndice](/help/assets/text-subscript.png)

Se utiliza para dar formato al texto seleccionado o al texto introducido después del cursor como subíndice.

### Superíndice

![Icono de superíndice](/help/assets/text-superscript.png)

Se utiliza para dar formato de superíndice al texto seleccionado o al texto introducido después del cursor.

### Pegar como texto

![Pegar como icono de texto](/help/assets/text-paste-text.png)

Pega cualquier texto copiado como texto sin formato sin formato.

Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar como texto sin formato sin formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Pegar como ejemplo de texto](/help/assets/text-paste-text-example.png)

### Pegar desde Word

![Pegar desde el icono de Word](/help/assets/text-paste-word.png)

Al seleccionar esta opción, se abre una ventana en la que el texto se puede pegar manteniendo su formato como vista previa antes de insertarlo en el texto. Acepte pulsando o haciendo clic en la marca de verificación, cancele la acción tocando o haciendo clic en la x.

![Pegar desde el ejemplo de Word](/help/assets/text-paste-word-example.png)

### Hipervínculo

![Icono Hipervínculo](/help/assets/text-hyperlink.png)

Utilice esta opción para convertir el texto seleccionado en un hipervínculo o modificar un vínculo ya definido. Esta opción solo está activa cuando ya se ha seleccionado texto y abre una ventana con opciones adicionales para configurar el vínculo.

![Ejemplo de hipervínculo](/help/assets/text-hyperlink-example.png)

* Especifique la ruta
   * Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM
   * Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta
      * Las rutas no absolutas se interpretan como relativas a AEM
* Escriba un texto descriptivo alternativo para el vínculo
* Seleccionar el comportamiento del vínculo
   * Destino
   * Misma ficha
   * Nueva ficha
   * Marco principal
   * Marco superior

   Toque o haga clic en la marca de verificación para aplicar el vínculo o la x para cancelar.

### Desvincular

![Icono Desvincular](/help/assets/text-unlink.png)

Utilice esta opción para quitar un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado un vínculo.

### Buscar

![Icono Buscar](/help/assets/text-find.png)

Utilice esta opción para buscar la aparición de una cadena de texto especificada en el texto. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda.

![Buscar ejemplo](/help/assets/text-find-example.png)

Escriba el texto que desee buscar y toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.
Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Match Case** antes de iniciar la búsqueda.
Si se encuentra una coincidencia, esta se resalta y el cuadro de diálogo de búsqueda se atenúa. Toque o haga clic de nuevo en el botón **Find** del cuadro de diálogo tenue para buscar la siguiente aparición.

![Encontrar ejemplo](/help/assets/text-find-example-found.png)

Si no se encuentran más ocurrencias, se mostrará un mensaje y la búsqueda se reiniciará desde el principio del texto.

![Buscar ejemplo no más ocurrencias](/help/assets/text-find-example-found-end.png)

### Reemplazar

![Icono Reemplazar](/help/assets/text-replace.png)

Utilice esta opción para buscar en el texto ocurrencias de una cadena de texto especificada y reemplazar las coincidencias por otra cadena. Al seleccionar esta opción, se abre una ventana para especificar las opciones de búsqueda y reemplazo.

![Reemplazar ejemplo](/help/assets/text-replace-example.png)

Introduzca el texto para el que desea buscar, así como el texto con el que debe reemplazarse.

* Toque o haga clic en **Buscar** para comenzar la búsqueda. Toque o haga clic en la x para cancelar.
* Si desea hacer una coincidencia exacta según el caso, seleccione la opción **Match Case** antes de iniciar la búsqueda.
* Seleccione **Reemplazar todo** para reemplazar todas las apariciones del texto a la vez.

Si se encuentra una coincidencia, esta se resalta y el cuadro de diálogo de búsqueda se atenúa. Vuelva a hacer clic en el botón **Buscar** del cuadro de diálogo tenue para buscar la siguiente aparición o seleccione el botón **Reemplazar** para reemplazar el texto resaltado y coincidente. Tenga en cuenta que el botón **Replace** solo está activo una vez que se ha realizado una coincidencia.

El cuadro de diálogo buscar y reemplazar se vuelve transparente cuando se hace clic en buscar y se vuelve opaco cuando se hace clic en reemplazar. Esto permite al autor revisar el texto que reemplazará el autor.

>[!NOTE]
>
>Al utilizar la funcionalidad de reemplazo, la cadena de reemplazo que se va a reemplazar debe introducirse al mismo tiempo que la cadena de búsqueda. Sin embargo, puede hacer clic en Buscar para buscar la cadena antes de reemplazarla. Si se introduce la cadena de reemplazo después de hacer clic en Buscar, la búsqueda se restablece al principio del texto.


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

Se utiliza para dar formato al texto seleccionado como una lista con viñetas o comenzar la inserción de una lista con viñetas después del cursor.

Para finalizar una lista con viñetas, toque o haga clic en el botón **Bullet** de nuevo o introduzca dos retornos de carro.

### Numerado

![Icono de lista numerada](/help/assets/text-numbered.png)

Se utiliza para dar formato al texto seleccionado como una lista numerada o comenzar la inserción de una lista numerada después del cursor.

Para finalizar una lista numerada, toque o haga clic en el botón **Numerado** de nuevo o introduzca dos retornos de carro.

### Anular sangría

![Icono de anular la selección](/help/assets/text-outdent.png)

Se utiliza para reducir el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

Solo activa si el texto o la posición seleccionados del cursor ya tienen sangría.

### Sangría

![Icono de sangría](/help/assets/text-outdent.png)

Se utiliza para aumentar el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

### Tabla

![Icono de tabla](/help/assets/text-table.png)

Se utiliza para insertar una tabla en el texto. Al seleccionar esta opción, se abre una ventana para especificar los detalles de la tabla.

![Ejemplo de tabla](/help/assets/text-table-example.png)

* **Columnas** : el número de columnas de la tabla (obligatorio)
* **Filas** : el número de filas de la tabla (obligatorio).
* **Anchura** : Ancho de la tabla
* **Altura** : altura de la tabla
* **Margen de celdas** : el espacio alrededor del contenido de la celda.
* **Espaciado de celdas** : el espacio entre celdas
* **Borde** : el peso de las líneas de borde de la tabla.
   * Si para el encabezado de la tabla:
      * La primera fila debe usarse
      * La primera columna debe usarse
      * La primera fila y la primera columna deben usarse
      * O no se debe utilizar ningún encabezado.
* **Rótulo** : el rótulo de la tabla.

### Revisar ortografía

![Revisar el icono ortográfico](/help/assets/text-spellcheck.png)

Se utiliza para revisar la ortografía del contenido del texto. Los posibles errores ortográficos se subrayan con líneas rojas rotas y rotas.

Para obtener más información sobre la revisión ortográfica y la personalización de los diccionarios de revisión ortográfica, consulte el documento [Configurar los complementos del editor de texto enriquecido](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

### Caracteres especiales {#special-characters}

![Icono de caracteres especiales](/help/assets/text-special-characters.png)

Se utiliza para insertar caracteres especiales en el texto. Al seleccionar esta opción, se abre una ventana en la que se muestran los caracteres disponibles.

![Ejemplo de caracteres especiales](/help/assets/text-special-characters-example.png)

Toque o haga clic en el carácter deseado para insertarlo en el texto después del cursor. Se pueden insertar varios caracteres. Toque o haga clic en la x para cerrar la ventana de selección.

### Modificar código fuente

![Icono de edición de origen](/help/assets/text-source.png)

Se utiliza para ver y modificar el origen HTML del texto.

Toque o haga clic en el icono **Source Edit** para cambiar el contenido del texto desde la vista con formato para ver el HTML sin procesar. En este modo, todas las demás opciones de formato están desactivadas. Toque o haga clic en el icono **Source Edit** de nuevo para volver a la vista con formato.

>[!CAUTION]
>
>Como siempre con acceso a HTML sin procesar, se debe tener cuidado al utilizar la opción **Source Edit**.
>
>El HTML introducido mediante **Source Edit** se analiza para detectar riesgos XSS y todos los scripts insertados se eliminan y no aparecen en la página resultante. Sin embargo, el HTML mal formado introducido en **Source Edit** puede romper la plantilla de la página, lo que da como resultado un formato inesperado o que la página resultante quede inutilizable.

>[!NOTE]
>
>Dado que el HTML introducido a través de **Source Edit** se analiza para detectar riesgos XSS y cualquier secuencia de comandos, y elimina automáticamente los que se encuentran, el contenido real que persiste puede variar de lo introducido en **Source Edit**. Por este motivo, para guardar los cambios realizados con **Source Edit**, primero debe salir de **Source Edit** para ver el texto en el editor normal antes de guardarlo.

### Formato de párrafo

![Icono de formato de párrafo](/help/assets/text-paragraph.png)

Se utiliza para aplicar formato de párrafo al texto seleccionado o al texto insertado después del cursor. Al seleccionar esta opción, se abre una lista desplegable en la que se selecciona el formato de párrafo.

![Ejemplo de formato de párrafo](/help/assets/text-paragraph-example.png)

### Edición en línea {#in-line-editing}

El componente de texto también se puede editar en línea, pero debido a limitaciones de espacio, no todas las opciones de formato están disponibles en línea. Para ver todas las opciones, cambie al modo de pantalla completa.

![Ejemplo de edición en línea](/help/assets/text-edit-inline-example.png)

### Configuración e ID {#setting-id}

Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, automáticamente se genera un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y capa de datos.

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué opciones de formato de texto están disponibles para los autores de contenido.

### Pestaña Plugins {#plugins-tab}

La pestaña Plugins se utiliza para habilitar y deshabilitar varias opciones de formato de texto disponibles para los autores de contenido.

### Características {#features}

![Diseño de las funciones del cuadro de diálogo](/help/assets/text-design-features.png)

Las siguientes funciones se pueden activar o desactivar para el componente.

* Pegar texto sin formato
* Pasado desde la palabra
* Buscar y reemplazar
* Corrector ortográfico
* Opciones de modificación de imágenes insertadas
* Edición de código HTML

### Formato {#formatting}

![Formato del cuadro de diálogo Diseño](/help/assets/text-design-formatting.png)

Las siguientes opciones de formato se pueden activar o desactivar para el componente.

* Tabla
* Listas (viñeta, número, sangría, sangría, sangría)
* Alineación (izquierda, derecha, centrado)
* Negrita, cursiva, subrayado
* Vinculación (y desvinculación)
* Subíndice/superíndice

### Estilos de párrafo {#paragraph-styles}

![Estilos de párrafo del cuadro de diálogo Diseño](/help/assets/text-design-paragraph.png)

Los estilos de párrafo se pueden activar o desactivar para el componente. Cuando se activa, se pueden definir los formatos permitidos.

* Toque o haga clic en el botón **Add** para insertar un nuevo estilo.
* Introduzca el código del estilo y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un estilo, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los formatos, toque o haga clic en y arrastre los controladores.

### Caracteres especiales {#configuring-special-characters}

![Caracteres especiales del cuadro de diálogo Diseño](/help/assets/text-design-special-characters.png)

La opción para insertar caracteres especiales se puede activar o desactivar para el componente. Cuando se activa, se pueden definir los caracteres permitidos.

* Toque o haga clic en el botón **Add** para insertar un carácter nuevo.
* Introduzca el código HTML del carácter y una descripción que se mostrarán en el cuadro de diálogo de edición.
* Para quitar un carácter, toque o haga clic en el botón **Eliminar**.
* Para reorganizar el orden de los caracteres, toque o haga clic en y arrastre los controladores.

## Pestaña Estilos {#styles-tab}

El componente Texto admite el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Texto es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
