---
title: Funciones de localización de los componentes principales
description: Funciones de localización de los componentes principales
role: Architect, Developer, Admin, User
exl-id: 9140b65a-6dd7-4ec9-9095-6e8243ec8424
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 100%

---

# Funciones de localización de los componentes principales {#localization-features-of-the-core-components}

Muchos sitios web requieren que el contenido se entregue en un formato localizado en varios idiomas y regiones geográficas. Los componentes principales seleccionados presentan una resolución de referencia inteligente para que sea sencillo crear una plantilla unificada para todo el contenido localizado que se adapte automáticamente en función de la estructura del sitio localizado.

## Ejemplo: Página localizada con navegación y pies de página {#example}

La mayoría de los sitios requieren que un pie de página esté presente en todas las páginas. Por lo general, estos pies de página son coherentes en todo el contenido de la página. Sin embargo, para una página de contenido localizada, es necesario mostrar una versión localizada de ese encabezado o pie de página.

Del mismo modo, un componente de navegación suele mostrarse en todas las páginas. Sin embargo, también deberá reflejar el contenido de las páginas localizadas.

Al utilizar las funciones de localización del [Componente principal Navegación](/help/components/navigation.md) y del [Componente principal Fragmento de experiencia](/help/components/experience-fragment.md) junto con las [plantillas editables de AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es), esto se convierte en una tarea sencilla. El ejemplo se podría ampliar para que también utilice el [Componente Navegación de idioma](/help/components/language-navigation.md).

## La estructura de contenido {#content-structure}

Todas las funciones de localización de AEM y sus componentes principales dependen de una estructura de contenido clara y lógica para el contenido localizado.

Digamos que su sitio se llama `my-site` y se encuentra aquí:

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

Los pies de página generalmente se crean mediante fragmentos de experiencias, por lo que necesitará una versión en inglés y francés igual que sus páginas. Sin embargo, los fragmentos de experiencia no son páginas, sino partes de páginas que se pueden reutilizar en todas las páginas, por lo que no residen directamente en `/content` como el resto de las páginas. En su lugar, se encuentran bajo su propia carpeta, pero como también deben localizarse, su estructura debe reflejar la estructura de localización del sitio.

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

El componente Fragmento de experiencia es muy flexible y es adecuado para un encabezado o pie de página.

Dado que nuestro sitio web hipotético se ofrece en inglés y francés, necesitaremos crear dos fragmentos de experiencias, ambos denominados `footer` [en las ubicaciones que describimos anteriormente.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Plantilla de la página {#template}

Como el pie de página aparecerá en todas las páginas, tendremos que agregar el fragmento de experiencia a nuestra plantilla de página estándar.

Nuestra plantilla se denomina simplemente `my-template` y se encuentra con nuestras otras plantillas:

```
/conf/my-site/settings/wcm/templates/my-template
```

A esta plantilla añadiremos los componentes básicos en los que queremos basar nuestras páginas.

* [Componente Navegación](/help/components/navigation.md)
   * El componente Navegación aparecerá en la parte superior de cada página.
   * En el componente Navegación, definimos la raíz de navegación, indicando al componente dónde comienza la estructura de navegación del sitio.
   * En función de la raíz de navegación, el componente puede encontrar automáticamente el contenido localizado correspondiente.
* [Componente Contenedor](/help/components/container.md)
   * Cada página contendrá un componente contenedor editable para que los autores puedan colocar contenido adicional en la página.
* [Fragmento de experiencias](/help/components/experience-fragment.md)
   * El componente Fragmento de experiencia se dirige a la ruta de fragmento en el idioma de creación del fragmento que representa el pie de página.
   * En función de la ruta de ese fragmento y de la estructura de los fragmentos de experiencia que reflejan la estructura de página localizada, el componente puede encontrar automáticamente el contenido localizado correspondiente.

   ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Al hacer el trabajo duro en la configuración de la estructura y plantilla del sitio, el autor del contenido simplemente necesita añadir el contenido necesario a las páginas. Gracias a las plantillas y a la lógica de localización de los componentes, la navegación y los pies de página se añaden automáticamente a la página y se localizan.

Por ejemplo, el autor solo tendría que añadir contenido, como un componente Texto, a las páginas en inglés y francés (representadas en azul a continuación).

El componente Navegación y el componente Fragmento de experiencia provienen de la plantilla de página y saben mostrar automáticamente el contenido correcto en función de la estructura de localización y la ubicación de la propia página (representada en blanco a continuación).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Resultado {#fitting-it-all-together}

A continuación se muestra una imagen completa de cómo estos elementos simples pero útiles trabajan juntos para ofrecer páginas localizadas para los autores de contenido.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
