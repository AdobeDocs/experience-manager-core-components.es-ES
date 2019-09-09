---
title: Características de localización de los componentes principales
seo-title: Características de localización de los componentes principales
description: Características de localización de los componentes principales
seo-description: Características de localización de los componentes principales
content-type: referencia
topic-tags: componentes principales
index: y
internal: n
translation-type: tm+mt
source-git-commit: 4af4873edf290f93733b0997b0e7a19c6c9e26f2

---


# Características de localización de los componentes principales {#localization-features-of-the-core-components}

Muchos sitios web requieren que el contenido se entregue en un formato localizado en varios idiomas y regiones geográficas. Los componentes principales hacen referencia a la resotación de referencia inteligente para facilitar la creación de una plantilla unificada para todo el contenido localizado que se adapta automáticamente en función de la estructura localizada del sitio.

## Ejemplo: página localizada con navegación y pies de página {#example}

La mayoría de los sitios requieren que un pie de página esté presente en todas las páginas. Estos pies de página son generalmente coherentes en todo el contenido de la página. Sin embargo, para una página de contenido localizado, se debe mostrar una versión localizada de ese encabezado o pie de página.

Del mismo modo, un componente de navegación suele mostrarse en todas las páginas. Sin embargo, también tendrá que reflejar el contenido de las páginas localizadas.

Uso de las funciones de localización del componente Core de [navegación](navigation.md) y del [componente Core Fragment Core](experience-fragment.md) junto con [las plantillas editables de AEM](https://docs.adobe.com/content/help/en/experience-manager-64/authoring/siteandpage/templates.html).

## Estructura de contenido {#content-structure}

Todas las funciones de localización de AEM y sus componentes principales dependen de una estructura de contenido lógica y clara para el contenido localizado.

Digamos que se llama simplemente al sitio `my-site` y se encuentra aquí:

```
/content/my-site
```

También supongamos que usted crea su sitio en inglés y lo ofrece en francés. Por lo tanto, si tiene una página simple denominada `my-page` , se encuentra en dos ramas de localización en el árbol de contenido del sitio:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

Es en estas ramas de localización donde creará páginas adicionales de sitios.

Generalmente, los pies de página se realizan utilizando Fragmentos de experiencia, por lo que necesitará una versión en inglés y en francés igual que las páginas. Sin embargo, los fragmentos de experiencias no son páginas, sino partes de páginas que pueden reutilizarse, de modo que no residen directamente como `/content` el resto de las páginas. En su lugar, viven bajo su propia carpeta, pero como también deben localizarse, su estructura debe reflejar la estructura de localización del sitio.

```
/content
+-- experience-fragments
   +-- en
      +-- footer
   \-- fr
      +-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

Es a través de la estructura de localización reflejada que los componentes principales pueden encontrar el contenido localizado necesario para una página correspondiente.

## Pie de página de página: Fragmento de experiencias {#footer}

El componente Fragmento de experiencia es muy flexible y está bien adaptado para un encabezado o pie de página de página.

Dado que nuestro sitio web hipotético se ofrece en inglés y francés, tendremos que crear dos fragmentos de experiencia, ambos llamados `footer`[en la ubicación que hemos descrito anteriormente.](#content-structure)

![](assets/screen-shot-2019-09-09-11.08.28.png)

## Plantilla de la página {#template}

Dado que el pie de página aparecerá en todas las páginas, tendremos que agregar el fragmento de experiencias a nuestra plantilla de página estándar.

Se llama simplemente a nuestra plantilla `my-template` y se encuentra con nuestras otras plantillas:

```
/conf/my-site/settings/wcm/templates/my-template
```

A esta plantilla le agregaremos los componentes básicos en los que desee basar nuestras páginas.

* [Componente de navegación](navigation.md)
   * El componente de navegación aparecerá en la parte superior de cada página.
   * En el componente de navegación se define la raíz de navegación, que indica al componente dónde empieza la estructura de navegación del sitio.
   * En función de la raíz de navegación, el componente puede encontrar el contenido localizado correspondiente automáticamente.
* Contenedor de diseño
   * Cada página contendrá un componente contenedor de diseño editable para que los autores puedan colocar contenido adicional en la página.
* [Fragmento de experiencias](experience-fragment.md)
   * Apuntamos el componente de fragmento Experinece a la ruta de fragmento en el lenguaje de creación del fragmento que representa el pie de página.
   * En función de la ruta de ese fragmento y la estructura de los fragmentos de experiencia que reflejen la estructura de la página localizada, el componente puede buscar automáticamente el contenido localizado correspondiente.
   ![](assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Al llevar a cabo la tarea de configurar la estructura y plantilla del sitio, el autor simplemente necesita agregar el contenido necesario a las páginas. Debido a la lógica de localización de los componentes, la navegación y los pies de página se localizarán automáticamente.

Por ejemplo, el autor sólo necesitaría agregar un componente de texto a las páginas inglés y francés (representado en azul a continuación).

El componente de navegación y el componente de fragmento de experiencias permiten mostrar automáticamente el contenido correcto según la estructura de localización y la ubicación de la propia página (representada en blanco a continuación).

![](assets/screen-shot-2019-09-09-11.22.14.png)

## Encaje todos juntos {#fitting-it-all-together}

Esta es la imagen completa de cómo funcionan estos sencillos pero poderosos elementos para proporcionar páginas localizadas para los autores de contenido.

![](assets/screen-shot-2019-09-09-11.27.58.png)
