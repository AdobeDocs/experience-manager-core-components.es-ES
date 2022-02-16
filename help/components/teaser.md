---
title: Componente Teaser
description: El componente Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, vincular a contenido adicional.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 69%

---

# Componente Teaser {#teaser-component}

El componente principal Teaser puede mostrar una imagen, un título, texto enriquecido y, opcionalmente, un vínculo a más contenido.

## Uso {#usage}

El componente Teaser permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a más contenido u otras acciones.

El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir si las opciones para crear llamadas a acción y agregar vínculos están disponibles, así como para desactivar las distintas opciones de visualización. El autor del contenido puede utilizar el [cuadro de diálogo de configuración](#configure-dialog) para establecer una imagen, definir CTA, definir títulos y descripciones y configurar vínculos al teaser individual. Se puede acceder al [cuadro de diálogo de edición](image.md#edit-dialog) del [Componente Imagen](image.md) para modificar la imagen del teaser.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Teaser es v2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| Versión 2 | - | Compatible | Compatible |
| [Versión 1](v1/teaser.md) | Compatible | Compatible | Compatible |

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Teaser, así como ver ejemplos de sus opciones de configuración, así como HTML y salida JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_teaser_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Teaser [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El autor del contenido puede utilizar el cuadro de diálogo de configuración para definir las propiedades del teaser individual. También existe un [cuadro de diálogo de edición](#edit-dialog) para modificar la imagen de teaser si se selecciona una.

### Ficha Vínculos {#links-tab}

![Ficha Vínculos del cuadro de diálogo de edición del componente teaser](/help/assets/teaser-edit-links.png)

El título, la descripción y la imagen del teaser se pueden heredar de la página vinculada o de la página vinculada en la primera llamada a la acción. Si no se especifica ni un vínculo ni una llamada a la acción, el título, la descripción y la imagen se heredarán de la página actual.

* **Vínculo** : este archivo vincula a una página de contenido, una URL externa o un anclaje de página.
* **Abrir vínculo en una pestaña nueva** - Si está activado, el vínculo se abre en una nueva pestaña del explorador.
* **Llamada a acción** : esta opción permite la vinculación a varios destinos.
   * La página vinculada en la primera llamada a la acción se utiliza al heredar el título, la descripción o la imagen del teaser.

### Ficha Texto {#text-tab}

![Pestaña de texto del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-text.png)

* **Pretítulo**: el pretítulo se mostrará antes del título del teaser.
* **Título**: texto que se mostrará como el titular del teaser.
   * **Obtener título de la página vinculada**: cuando se activa, el título se rellena con el título de la página vinculada.
* **Descripción**: define una descripción para mostrarla como el subencabezado del teaser.
   * **Obtener descripción de la página vinculada**: cuando está marcada, la descripción se rellena con la descripción de la página vinculada.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Recurso {#asset-tab}

![Pestaña de imagen del cuadro de diálogo de edición del componente Teaser](/help/assets/teaser-edit-image.png)

* **Heredar imagen destacada de la página** - Utilice la imagen definida en las propiedades de página de la página vinculada o la página actual si no se encuentra ninguna.
* **Recurso de imagen** - Coloque un recurso desde la variable [navegador de recursos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=es) o toque el **navegar** para cargar desde un sistema de archivos local.
   * Pulse o haga clic en **Borrar** para anular la selección de la imagen seleccionada actualmente.
   * Pulse o haga clic en **Editar** para [administrar las representaciones del recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=es) en el editor de recursos.
* **Texto alternativo para accesibilidad** - Este campo le permite definir una descripción de la imagen para los usuarios con deficiencias visuales.
   * **Heredar texto alternativo de la página** - Esta opción utiliza la descripción alternativa del valor de recurso vinculado del `dc:description` metadatos en DAM o de la página actual si no hay ningún recurso vinculado.
* **No proporcionar un texto alternativo** - Esta opción marca la imagen que tecnologías de asistencia ignoran, como lectores de pantalla, en casos en los que la imagen es puramente decorativa o no transmite información adicional a la página.

>[!NOTE]
>
>Actualmente, las [funciones de Dynamic Media](image.md#dynamic-media) no están disponibles en el componente Teaser.

### Pestaña Estilos {#styles-tab-edit}

![Pestaña Estilos del cuadro de diálogo de edición del componente Lista de teaser](/help/assets/teaser-edit-styles.png)

El componente Teaser es compatible con el sistema de estilos de [AEM.](/help/get-started/authoring.md#component-styling).

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en la variable [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

## Cuadro de diálogo de edición {#edit-dialog}

El componente Teaser delega el procesamiento de imágenes en el [Componente de imagen](image.md). Por lo tanto, el [cuadro de diálogo de edición](image.md#edit-dialog) del componente de imagen está disponible para que el autor del contenido manipule la imagen de teaser.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones de teaser que tiene el autor de contenido al utilizar este componente.

### Pestaña Teaser {#teaser-tab}

![Cuadro de diálogo de diseño del componente Teaser](/help/assets/teaser-design.png)

* **Llamadas a la acción**
   * **Deshabilitar llamadas a la acción**: oculta la opción **Llamadas a la acción** para autores de contenido
* **Elementos**
   * **Ocultar pretítulo**: oculta la opción **Pretítulo** para autores de contenido
   * **Ocultar título**: oculta la opción **Título** para autores de contenido
      * Cuando se selecciona, el **Tipo de título** está oculto
   * **Ocultar descripción**: oculta la opción **Descripción** para autores de contenido
* **Tipo de título predeterminado** - Define la etiqueta H que utilizará el título del teaser.
* **Delegado de imágenes**: visualización informativa que indica a qué componente delega el teaser la administración de las imágenes.

### Pestaña Estilos {#styles-tab}

El componente Teaser es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Teaser es compatible con la [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md).
