---
title: Crear con componentes principales
seo-title: Crear con componentes principales
description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas: los componentes principales ofrecen una funcionalidad de creación flexible y enriquecida.'
seo-description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas: los componentes principales ofrecen una funcionalidad de creación flexible y enriquecida.'
uuid: 4 a 54 cd 4 c -3 d 89-4683-8301-bf 1 e 634736 e 3
content-type: referencia
topic-tags: creación
discoiquuid: 8751 e 490-d 427-44 f 2-b 767-51935 afda 988
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Autor con componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Esta sección trata los componentes principales, que proporcionan tipos de contenido esenciales para crear páginas.

Los componentes principales ofrecen funciones de creación flexibles y enriquecidas. El sitio de referencia [We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) ilustra cómo se pueden utilizar los componentes principales.

>[!NOTE]
>
>Los componentes principales no están disponibles inmediatamente para los autores, el [equipo de desarrollo debe integrarlos primero en su entorno](using.md). Una vez integrados, pueden estar disponibles y preconfigurados a través del [editor de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) o en [modo de diseño](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Los componentes [principales requieren AEM 6.3 o superior](versions.md) y no funcionan con la IU clásica.

## Crear con componentes principales {#authoring-with-core-components}

Para comprender los componentes principales, consulte la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html), que muestra los componentes principales y proporciona ejemplos de su uso.

Como autor, notará varias ventajas de los componentes principales, como:

* Uso sencillo y bien integrado con el editor [de páginas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)
* Capacidades ricas en funciones para dar cabida a muchos casos de uso como [se ilustra en We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)
* [Preconfigurable](#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas
   * A través del [editor de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) para [plantillas editables](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html)
   * A través [del modo](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html) de diseño para [plantillas estáticas](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-static.html)

* Se basa en [las directrices de accesibilidad](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* Creación de diseños [adaptables](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

Los componentes están disponibles en la ficha **Componentes** del panel lateral del editor de páginas al [editar una página](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html).

Los componentes se agrupan según las categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el navegador [de componentes](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son por defecto de un grupo oculto y no son visibles en el navegador de componentes.
>
>Agregue los componentes necesarios a un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

Configurar componentes de base era el trabajo de un desarrollador. Sin embargo, con los componentes principales, un autor de plantillas ahora puede configurar varias capacidades a través del editor de plantillas o en modo de diseño.

Por ejemplo, si un componente de imagen no debería permitir la carga de imágenes del sistema de archivos, o si un componente de texto debería permitir únicamente cierto formato de párrafo, estas funciones se pueden activar o desactivar con un simple clic.

Consulte [Creación de plantillas de página](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) para obtener más información.

### Editar y diseñar diálogos {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir las opciones permitidas como parte de una plantilla y, a continuación, configurarlas por el autor de la página para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controles controla | Ejemplos |
|--- |--- |--- |--- |
| **Editar cuadro de diálogo** | Opciones que un autor **de página** puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá en última instancia en la página. | Formato del texto del contenido, rotar una imagen en una página |
| **Cuadro de diálogo de diseño** | Opciones que un **autor** de plantilla puede modificar al configurar una plantilla de página. | Las opciones que el autor de la página tiene al editar el componente | Qué opciones de formato de texto están disponibles, qué imágenes en contexto están disponibles |

### Estilo del componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilos AEM.

* Un autor de plantilla puede definir los estilos disponibles para un componente concreto en el cuadro de diálogo Diseño de ese componente.
* El autor de contenido puede elegir qué estilos se aplicarán al agregar el componente y a crear contenido.

Para obtener más información, consulte [la documentación del Sistema](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) de estilos.

>[!NOTE]
>
>En AEM 6.3, se requiere service pack 2 (6.3.2.0) o posterior para activar la función del sistema de estilos.

## Lista de los componentes principales disponibles {#list-of-core-components-available}

La siguiente es una lista de los componentes principales disponibles vinculados a páginas que describen sus capacidades de diálogo de edición y diseño en detalle.

La versión actual de los componentes principales incluye los componentes siguientes.

* [Ruta de exploración](breadcrumb.md)
* [Botón de formulario](form-button.md)
* [Carrusel](carousel.md)
* [Contenedor del formulario](form-container.md)
* [Fragmento de contenido](content-fragment-component.md)
* [Lista de fragmentos de contenido](content-fragment-list.md)
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
* [Teaser](teaser.md)
* [Texto](text.md)
* [Título](title.md)

>[!CAUTION]
>
>Algunas versiones de componentes principales individuales pueden ser compatibles únicamente con ciertas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada en la lista anterior) para el componente específico de información de compatibilidad o haga referencia al [documento Versiones](versions.md) de componentes principales para obtener más información.

>[!NOTE]
>
>En función de su instancia, puede disponer de componentes personalizados desarrollados explícitamente para sus necesidades. Pueden tener incluso el mismo nombre que algunos de los componentes mencionados aquí.
>Los componentes principales del formulario no están relacionados con AEM Forms.

## Medios del desarrollador {#developer-resources}

Consulte la documentación del desarrollador [Desarrollar componentes](developing.md) principales para obtener información técnica sobre los componentes principales.
