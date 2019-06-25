---
title: Componente de navegación de idioma
seo-title: Componente de navegación de idioma
description: nulo
seo-description: El componente de navegación de idioma proporciona una navegación de idioma o país para un sitio, para que los visitantes puedan desplazarse a la misma página en una configuración regional distinta.
uuid: ce 736458-9 cdf -4 bc 2-b 90 f -9 c 5 a 62 fe 1 ca 0
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 8 f 232 eb 0-65 d 5-4075-8668-75 f 1366882 c 8
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Language Navigation Component{#language-navigation-component}

El componente de navegación de idioma proporciona una navegación de idioma o país para un sitio, para que los visitantes puedan desplazarse a la misma página en una configuración regional distinta.

## Uso {#usage}

A menudo, los sitios Web se proporcionan en varios idiomas para distintas regiones. El componente de navegación de idioma permite a un visitante ver la misma página en diferentes idiomas o configuraciones regionales.

The [edit dialog](#edit-dialog) allows the definition of the global site navigation root as well as how deep into the structure the navigation should go. Using the [design dialog](#design-dialog), the template author can set the default values for the same options.

## Version and Compatibility {#version-and-compatibility}

La versión actual del componente de navegación de idioma es v 1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/languagenavigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

El cuadro de diálogo de edición permite definir la raíz de navegación del sitio global, así como la profundidad con la que debe ir la navegación.

![](assets/screen_shot_2018-01-12at133353.png)

* **Raíz
de navegación** Define la página raíz de la estructura de navegación.
   * Use the **Open Selection Dialog** button to easily navigate the content structure and select the root.
* **Profundidad de profundidad**
de la estructura del idioma de la estructura de idioma global en relación con la raíz de navegación.

## Design Dialog {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones disponibles en el cuadro de diálogo de edición.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Valor predeterminado raíz**
de navegación de la raíz de navegación cuando un autor de contenido coloca el componente Conmutador de idioma en una página de contenido
* **Valor predeterminado de Profundidad**
de la estructura del idioma de la profundidad de la estructura de idioma cuando un autor de contenido coloca el componente Conmutador de idioma en una página de contenido

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](authoring.md#component-styling).