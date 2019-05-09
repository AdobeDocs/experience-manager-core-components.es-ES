---
title: Componente Teaser
seo-title: Componente Teaser
description: El componente teaser puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, vincular a otro contenido.
seo-description: El componente teaser puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, vincular a otro contenido.
uuid: 46989314-df 37-448 b -8562-c 707043 f 2160
contentOwner: bohnert
content-type: referencia
topic-tags: componentes principales
discoiquuid: e 597 c 18 e -3643-41 be -9878-4 a 7872 f 1 ab 90
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente Teaser{#teaser-component}

El componente Teaser del componente principal puede mostrar una imagen, un título, un texto enriquecido y, opcionalmente, un vínculo a otro contenido.

## Uso {#usage}

El componente Teaser permite que el autor de contenido cree fácilmente un teaser para más contenido utilizando una imagen, un título o un texto enriquecido y vinculando a contenido u otras acciones.

El autor de la plantilla puede utilizar el cuadro de diálogo [de diseño](#design-dialog) para definir si hay disponibles las opciones para crear llamadas a acción y agregar vínculos, así como desactivar varias opciones de visualización. El autor de contenido puede utilizar el cuadro [de diálogo](#configure-dialog) de configuración para definir una imagen, definir CTAS, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro](image.md#edit-dialog) de [diálogo de edición del componente](image.md) de imagen para modificar la imagen de teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es v 1, introducida con la versión 2.1.0 de los componentes principales en julio de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v1 | Compatible | Compatible | Compatible |

## Salida de componente de muestra {#sample-component-output}

A continuación se muestra una muestra tomada de [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### Captura de pantalla {#screenshot}

![](assets/screen_shot_2018-07-04at145042.png)

### Biblioteca de componentes

Para experimentar el componente Teaser, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/teaser.html).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

## Configurar cuadro de diálogo {#configure-dialog}

El autor de contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También hay un cuadro [de diálogo](#edit-dialog) de edición para modificar la imagen de teaser si se selecciona uno.

### Imagen {#image}

![](assets/screen_shot_2018-07-03at104125.png)

* **Recurso de imagen**
   * Coloque un recurso desde el navegador [de recursos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) o toque la opción **de exploración** para cargar desde un sistema de archivos local.
   * Toque o haga clic **en Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Toque o haga clic **en Editar** para [transferir las representaciones del recurso](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) en el editor de recursos.

### Texto {#text}

![](assets/screen_shot_2018-07-03at104138.png)

* **Title**
Define un título para mostrarlo como el titular del teaser.
* **Obtener título de página
vinculada** Cuando se marque, el título se rellenará con el título de la página vinculada.
* **Descripcióndefine**
una descripción para mostrar como subtítulo del teaser.
* **Obtener descripción de la página**
vinculada Cuando se marque, la descripción se rellenará con la descripción de la página vinculada.

### Vínculos y acciones {#links-actions}

![](assets/screen_shot_2018-07-03at104146.png)

* **Vínculo de vínculo**
aplicado al teaser. Utilice el navegador de rutas para seleccionar el destino del vínculo.
* **Activar llamadas a acción**
Cuando se selecciona, habilita la definición de llamadas a acción. El primer vínculo de llamada a acción de la lista se usa como vínculo para otros elementos teaser.

## Editar cuadro de diálogo {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el componente [de imagen](image.md). Por lo tanto, [el cuadro de diálogo]de edición (image. md # edit-dialog del componente de imagen está disponible para el autor de contenido para manipular la imagen de teaser.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones de teaser que tiene el autor del contenido al utilizar este componente.

### Ficha Teaser {#teaser-tab}

![](assets/screen_shot_2018-07-03at105958.png)

* **Llamadas a la acción**
   * **Deshabilitar la opción Llamada a acción**
Oculta la **opción Llamada a acciones** para los autores de contenido
* **Elementos**
   * **Ocultar título**
      * Oculta la opción **Título** para los autores de contenido
      * Cuando se selecciona, el tipo **de título** está oculto
   * **Ocultar descripción**
Oculta la **opción Descripción** para los autores de contenido
* **Tipo
de título** Define la etiqueta H que utilizará el título del teaser.
* **Vínculos**
   * **No vincular la imagen**
cuando se selecciona, la imagen de teaser no está vinculada
   * **No vincular el título**
cuando se selecciona, el título del teaser no está vinculado

### Ficha Estilos {#styles-tab}

El componente Teaser admite [el sistema de estilos AEM](authoring.md#component-styling).
