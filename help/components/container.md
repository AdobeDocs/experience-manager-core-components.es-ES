---
title: Componente Contenedor
description: El componente principal Contenedor permite crear un contenedor para varios componentes adicionales en una página.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Contenedor{#container-component}

El componente principal Contenedor permite crear un contenedor para varios componentes adicionales en una página.

{{traditional-aem}}

## Uso {#usage}

El componente principal Contenedor permite crear un contenedor para varios componentes adicionales en una página y se puede utilizar para agrupar otros componentes y aplicar un estilo o diseño común.

* Las propiedades del contenedor se pueden seleccionar en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente Contenedor al agregarlo a una página se pueden definir en el [cuadro de diálogo de diseño](#design-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor es la versión 1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Contenedor, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_container_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_container_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento contenedor y cómo se comportará y aparecerá para un visitante de la página.

![Cuadro de diálogo de edición del componente Contenedor](/help/assets/container-edit.png)

* **Diseño**: esta opción define el comportamiento o el comportamiento de diseño del componente Contenedor.
   * **Simple**: define un contenedor como una simple colección de componentes.
   * **Cuadrícula interactiva**: define un contenedor como un diseño interactivo de [AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=es)
* **Color de fondo**: se puede definir como valores RGB de forma libre o utilizando el selector de color, [según la configuración](#background-tab)
* **Imagen de fondo**: define un color de fondo para el contenedor, [según la configuración](#background-tab)
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Contenedor.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente Contenedor.

La pestaña Componentes permitidos funciona del mismo modo que la del mismo nombre cuando [define la directiva y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Componentes predeterminados {#default-components-tab}

La pestaña Componentes predeterminados se utiliza para definir qué componente se añade al componente cuando se coloca un tipo de recurso en particular en el contenedor, de forma similar a [cómo se definen los componentes predeterminados en la plantilla de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

### Pestaña Configuración interactiva {#responsive-settings-tab}

![Pestaña Configuración interactiva del cuadro de diálogo de diseño del componente Contenedor](/help/assets/container-design-responsive.png)

* **Columnas**: define el número de columnas de la cuadrícula del contenedor resultante.

### Pestaña Fondo {#background-tab}

![Pestaña Fondo del cuadro de diálogo de diseño del componente Contenedor](/help/assets/container-design-background.png)

* **Imagen de fondo**
   * **Habilitar la imagen de fondo**: seleccione esta opción para permitir que el autor del contenido defina una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Habilitar el color de fondo**: seleccione esta opción para permitir que el autor del contenido defina un color de fondo para el contenedor.
   * **Solo muestras**: seleccione esta opción para permitir que el autor del contenido seleccione únicamente muestras de color predefinidas para el color de fondo del contenedor.
      * Solo está disponible cuando se selecciona **Habilitar el color de fondo**
* **Muestras permitidas**: defina los colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo del contenedor
   * Utilice el botón **Añadir** para añadir una muestra de color predefinida. Una vez añadida, se añade una entrada a la lista, que contiene las siguientes columnas:
   * **Valor**: defina el color manualmente mediante valores RGB.
      * Pulse o haga clic en el selector de color para seleccionar más fácilmente un color ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar**: pulse o haga clic para eliminar una muestra.
   * **Reorganizar**: pulse o haga clic y arrastre para reorganizar el orden de las muestras.

### Pestaña Estilos {#styles-tab}

El componente Contenedor es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).
