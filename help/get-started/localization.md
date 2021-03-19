---
title: Funciones de localización de los componentes principales
description: Funciones de localización de los componentes principales
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---


# Características de localización de los componentes principales {#localization-features-of-the-core-components}

Muchos sitios web requieren que el contenido se entregue en un formato localizado en varios idiomas y regiones geográficas. Los componentes principales seleccionados presentan una resolución de referencia inteligente para que sea sencillo crear una plantilla unificada para todo el contenido localizado que se adapte automáticamente en función de la estructura del sitio localizado.

## Ejemplo: Página localizada con Navegación y Pies de página {#example}

La mayoría de los sitios requieren que un pie de página esté presente en todas las páginas. Por lo general, estos pies de página son coherentes en todo el contenido de la página. Sin embargo, para una página de contenido localizada, es necesario mostrar una versión localizada de ese encabezado o pie de página.

Del mismo modo, un componente de navegación suele mostrarse en todas las páginas. Sin embargo, también deberá reflejar el contenido de las páginas localizadas.

Al utilizar las funciones de localización del [Componente principal de navegación](/help/components/navigation.md) y del [Componente principal del fragmento de experiencia](/help/components/experience-fragment.md) junto con las [plantillas editables de AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html), esto se convierte en una tarea sencilla. El ejemplo se podría ampliar para que también utilice el [Componente de navegación de idioma](/help/components/language-navigation.md).

## La estructura de contenido {#content-structure}

Todas las funciones de localización de AEM y sus componentes principales dependen de una estructura de contenido clara y lógica para el contenido localizado.

Digamos que su sitio simplemente se llama `my-site` y se encuentra aquí:

```
/content/my-site
```

Digamos también que usted crea su sitio en inglés y lo ofrece también en francés. Por lo tanto, si tiene una página simple llamada `my-page`, se encontrará en dos ramas de localización del árbol de contenido del sitio:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

Es en estas ramas de localización donde creará páginas de sitios adicionales.

Los pies de página generalmente se crean mediante fragmentos de experiencias, por lo que necesitará una versión en inglés y francés igual que sus páginas. Sin embargo, los fragmentos de experiencia no son páginas, sino partes de páginas que se pueden reutilizar en todas las páginas, por lo que no residen directamente en `/content` como el resto de las páginas. En su lugar, viven bajo su propia carpeta, pero como también deben localizarse, su estructura debe reflejar la estructura de localización del sitio.

```
/content
+-- experience-fragments
   +-- en
      \-- footer
   \-- fr
      \-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

A través de la estructura de localización reflejada, los componentes principales pueden encontrar el contenido localizado necesario para una página correspondiente.

## Pie de página: fragmento de experiencia {#xf-footer}

El componente Fragmento de experiencia es muy flexible y es adecuado para un encabezado o pie de página de página.

Dado que nuestro sitio web hipotético se ofrece en inglés y francés, necesitaremos crear dos fragmentos de experiencias, ambos denominados `footer` [en las ubicaciones que describimos anteriormente.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Plantilla de la página {#template}

Como el pie de página aparecerá en todas las páginas, tendremos que agregar el fragmento de experiencia a nuestra plantilla de página estándar.

Nuestra plantilla se denomina simplemente `my-template` y se encuentra con nuestras otras plantillas:

```
/conf/my-site/settings/wcm/templates/my-template
```

A esta plantilla añadiremos los componentes básicos en los que queremos basar nuestras páginas.

* [Componente de navegación](/help/components/navigation.md)
   * El componente de navegación aparecerá en la parte superior de cada página.
   * En el componente de navegación, definimos la raíz de navegación, indicando al componente dónde comienza la estructura de navegación del sitio.
   * En función de la raíz de navegación, el componente puede encontrar automáticamente el contenido localizado correspondiente.
* [Componente contenedor](/help/components/container.md)
   * Cada página contendrá un componente contenedor editable para que los autores puedan colocar contenido adicional en la página.
* [Fragmento de experiencias](/help/components/experience-fragment.md)
   * El componente Fragmento de experiencia se dirige a la ruta de fragmento en el idioma de creación del fragmento que representa el pie de página.
   * En función de la ruta de ese fragmento y de la estructura de los fragmentos de experiencia que reflejan la estructura de página localizada, el componente puede encontrar automáticamente el contenido localizado correspondiente.

   ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Al hacer el trabajo duro en la configuración de la estructura y plantilla del sitio, el autor del contenido simplemente necesita añadir el contenido necesario a las páginas. Gracias a las plantillas y a la lógica de localización de los componentes, la navegación y los pies de página se añaden automáticamente a la página y se localizan.

Por ejemplo, el autor solo tendría que añadir contenido, como un componente de texto, a las páginas en inglés y francés (representadas en azul a continuación).

El componente de navegación y el componente de fragmento de experiencia provienen de la plantilla de página y saben mostrar automáticamente el contenido correcto en función de la estructura de localización y la ubicación de la propia página (representada en blanco a continuación).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Agrupación de todo {#fitting-it-all-together}

A continuación se muestra una imagen completa de cómo estos elementos simples pero potentes trabajan juntos para ofrecer páginas localizadas para los autores de contenido.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
