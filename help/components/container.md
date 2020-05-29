---
title: Componente Contenedor
description: El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 2%

---


# Componente Contenedor{#container-component}

El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página.

## Uso {#usage}

El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página y se puede utilizar para agrupar otros componentes y aplicar un estilo o una presentación comunes.

* Las propiedades del contenedor se pueden seleccionar en el cuadro de diálogo [Configurar](#configure-dialog).
* Los valores predeterminados del componente Contenedor al agregarlo a una página se pueden definir en el cuadro de diálogo [](#design-dialog)de diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor es la v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Contenedor, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [](https://adobe.com/go/aem_cmp_library_container)de componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_container_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de contenedor y cómo se comportará y aparecerá para un visitante de la página.

![Cuadro de diálogo de edición del componente Contenedor](/help/assets/container-edit.png)

* **Diseño** : esta opción define el comportamiento o el comportamiento de maquetación del componente Contenedor.
   * **Simple** : define un contenedor como una simple colección de componentes
   * **Cuadrícula** adaptable: define un contenedor como un diseño adaptable de [AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Color** de fondo: se puede definir como valores RGB de forma libre o mediante el selector de color, [según la configuración](#background-tab)
* **Imagen** de fondo: define un color de fondo para el contenedor, [según la configuración](#background-tab)
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Contenedor.

### Allowed Components Tab {#allowed-components-tab}

La ficha Componentes **** permitidos se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente Contenedor.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre al [definir la política y las propiedades de un Contenedor de diseño en el Editor de plantillas.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Default Components Tab {#default-components-tab}

La ficha Componentes predeterminados se utiliza para definir qué componente se agrega al componente cuando se suelta un tipo de recurso concreto en el contenedor, de forma similar a [cómo se definen los componentes predeterminados en la plantilla](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de página.

### Ficha Configuración adaptable {#responsive-settings-tab}

![Ficha Ajustes interactivos del cuadro de diálogo de diseño del componente Contenedor](/help/assets/container-design-responsive.png)

* **Columnas** : define el número de columnas en la cuadrícula del contenedor resultante.

### Ficha Fondo {#background-tab}

![Ficha Fondo del cuadro de diálogo de diseño del componente Contenedor](/help/assets/container-design-background.png)

* **Imagen de fondo**
   * **Activar imagen** de fondo: seleccione esta opción para permitir que el autor del contenido defina una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Activar color** de fondo: seleccione esta opción para permitir que el autor del contenido defina un color de fondo para el contenedor.
   * **Solo** muestras: seleccione esta opción para permitir que el autor del contenido seleccione solo muestras de color predefinidas para el color de fondo del contenedor.
      * Solo está disponible cuando se selecciona **Activar color** de fondo
* **Muestras** permitidas: defina los colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo del contenedor
   * Utilice el botón **Añadir** para agregar una muestra de color predefinida. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:
   * **Valor** : defina el color manualmente mediante valores RGB
      * Toque o haga clic en el selector de color para seleccionar un color más fácilmente ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar** : toque o haga clic para eliminar una muestra.
   * **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de las muestras.

### Ficha Estilos {#styles-tab}

El componente Contenedor es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
