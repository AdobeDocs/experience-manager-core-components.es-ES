---
title: Componente Contenedor
seo-title: Componente Contenedor
description: nulo
seo-description: El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# Container Component{#container-component}

El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página.

## Uso {#usage}

El componente Contenedor de componentes principales permite crear un contenedor para varios componentes adicionales en una página y se puede utilizar para agrupar otros componentes y aplicar un diseño o diseño común.

* The container&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the Container Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente Contenedor es v 1, introducida con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/container.html).

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de contenedor y cómo se comportará y aparecerá para un visitante de la página.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **Diseño** : Esta opción define el comportamiento o el comportamiento de diseño del componente Contenedor.
   * **Simple** : Define un contenedor como una simple colección de componentes
   * **Cuadrícula** adaptable: define un contenedor como cuadrícula adaptable [de AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** - Utilice esta opción para definir el atributo de ID HTML que se aplicará al componente.
* **Color** de fondo: definición como valores RGB de forma libre o mediante el selector de color, [según la configuración](#background-tab)
* **Imagen** de fondo: define un color de fondo para el contenedor [, según la configuración](#background-tab)

## Design Dialog {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Contenedor.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to the Container Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Default Components Tab {#default-components-tab}

The Default Components tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors).

### Responsive Settings Tab {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **Columnas** : define el número de columnas de la cuadrícula del contenedor resultante.

### Background Tab {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **Imagen de fondo**
   * **Activar imagen** de fondo: Seleccione esta opción para permitir al autor de contenido definir una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Activar color** de fondo: seleccione esta opción para permitir al autor de contenido definir un color de fondo para el contenedor.
   * **Muestras solo** : seleccione esta opción para permitir que el autor de contenido seleccione de forma predefinida las muestras de color predefinidas para el color de fondo del contenedor.
      * Only available when **Enable background color** is selected
* **Muestras** permitidas: defina colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo contenedor
   * Use the **Add** button to add a pre-defined color swatch. Una vez agregado, se agrega una entrada a la lista, que contiene las columnas siguientes:
   * **Valor** : definir el color manualmente a través de valores RGB
      * Toque o haga clic en el selector de color para seleccionar un color más fácilmente ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar** : toque o haga clic para eliminar una muestra.
   * **Reorganizar** : Toque o haga clic y arrastre para cambiar el orden de las muestras.

### Styles Tab {#styles-tab}

The Container Component supports the AEM [Style System](authoring.md#component-styling).
