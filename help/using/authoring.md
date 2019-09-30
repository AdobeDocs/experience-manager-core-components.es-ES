---
title: Crear con componentes principales
seo-title: Crear con componentes principales
description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas que se crean: los componentes principales ofrecen una funcionalidad de creación flexible y con muchas funciones.'
seo-description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas que se crean: los componentes principales ofrecen una funcionalidad de creación flexible y con muchas funciones.'
uuid: 4a54cd4c-3d89-4683-8301-bf1e634736e3
content-type: referencia
topic-tags: creación
discoiquuid: 8751e490-d427-44f2-b767-51935afda988
translation-type: tm+mt
source-git-commit: bf1993085c4cd95121cb6d78be8c52934802b645

---


# Autor con componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas.

Los componentes principales ofrecen una funcionalidad de creación flexible y rica en funciones. The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) illustrates how the core components can be used.

Para experimentar los componentes principales y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)componentes.

Para obtener una introducción más detallada y orientada al desarrollador para implementar los componentes principales en un proyecto de AEM, consulte [el tutorial de WKND.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html).

>[!CAUTION]
>
>Los componentes principales [requieren AEM 6.3 o superior](versions.md) y el uso de plantillas [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)editables. No funcionan con la IU clásica ni con plantillas estáticas.

## Crear con componentes principales {#authoring-with-core-components}

Como autor, notará varias ventajas de los componentes principales, entre ellas:

* Simple to use and well-integrated with the [page editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)

* Funciones ricas en funciones para acomodar muchos casos de uso, como [se ilustra en We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) y en la biblioteca de [componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)

* [Preconfigurable](#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas mediante el editor de [plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

* Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Built to support [responsive layout](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

* Creado para admitir la localización [sencilla](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Los componentes se agrupan según categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el navegador [de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) componentes y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son de forma predeterminada parte de un grupo oculto y no están visibles en el navegador de componentes.
>
>Agregue los componentes necesarios a un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

La configuración de los componentes básicos era tarea de un desarrollador. Sin embargo, con los componentes principales, un autor de plantilla ahora puede configurar una serie de funciones mediante el editor de plantillas.

Por ejemplo, si un componente de imagen no debe permitir la carga de imágenes desde el sistema de archivos o si un componente de texto solo debe permitir cierto formato de párrafo, estas funciones se pueden activar o desactivar con un solo clic.

Consulte [Creación de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) de página para obtener más información.

### Editar y diseñar cuadros de diálogo {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir qué opciones se permiten como parte de una plantilla y, a continuación, el autor de la página puede configurarlas para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controla | Ejemplos |
|--- |--- |--- |--- |
| **Editar cuadro de diálogo** | Opciones que un autor **de una** página puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá finalmente en la página. | Formato del texto del contenido, girar una imagen en una página |
| **Cuadro de diálogo Diseño** | Opciones que el autor **de una** plantilla puede modificar al configurar una plantilla de página. | Qué opciones tiene disponible el autor de la página al editar el componente | Qué opciones de formato de texto están disponibles, qué opciones de imagen in situ están disponibles |

### Estilo de componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilo AEM.

* Un autor de plantilla puede definir qué estilos están disponibles para un componente concreto en el cuadro de diálogo Diseño de dicho componente.
* A continuación, el autor del contenido puede elegir qué estilos aplicar al agregar el componente y crear contenido.

Para obtener más información, consulte la documentación [del sistema](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) de estilos.

>[!NOTE]
>
>En AEM 6.3, se requiere el Service Pack 2 (6.3.2.0) o una versión posterior para activar la función del sistema de estilo.

## Lista de componentes principales disponibles {#list-of-core-components-available}

A continuación se muestra una lista de los componentes principales disponibles vinculados a páginas que describen detalladamente sus funciones de edición y diseño del cuadro de diálogo.

La versión actual de los componentes principales incluye los siguientes componentes.

* [Acordeón](accordion.md)
* [Ruta de exploración](breadcrumb.md)
* [Botón](button.md)
* [Contenedor](container.md)
* [Carrusel](carousel.md)
* [Fragmento de contenido](content-fragment-component.md)
* [Lista de fragmentos de contenido](content-fragment-list.md)
* [Descargar](download.md)
* [Incrustar](embed.md)
* [Fragmento de experiencias](experience-fragment.md)
* [Botón de formulario](form-button.md)
* [Contenedor del formulario](form-container.md)
* [Formulario oculto](form-hidden.md)
* [Opciones de formulario](form-options.md)
* [Texto de formulario](form-text.md)
* [Imagen](image.md)
* [Navegación por idiomas](language-navigation.md)
* [Lista](list.md)
* [Navegación](navigation.md)
* [Página](page.md)
* [Búsqueda rápida](quick-search.md)
* [Separador](separator.md)
* [Compartir en redes sociales](sharing.md)
* [Fichas](tabs.md)
* [Texto](text.md)
* [Título](title.md)

>[!CAUTION]
>
>Es posible que algunas versiones de componentes principales individuales solo sean compatibles con determinadas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada en la lista anterior) del componente específico para obtener información de compatibilidad o consulte el documento Versiones [de componentes](versions.md) principales para obtener más información.

>[!NOTE]
>
>En función de su instancia, puede disponer de componentes personalizados desarrollados explícitamente para sus necesidades. Pueden tener incluso el mismo nombre que algunos de los componentes mencionados aquí.
>Los componentes principales del formulario no están relacionados con AEM Forms.

## Medios del desarrollador {#developer-resources}

Consulte la documentación para desarrolladores de [Desarrollar componentes](developing.md) principales para obtener información técnica sobre los componentes principales.
