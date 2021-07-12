---
title: Crear con componentes principales
description: En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes principales ofrecen funciones flexibles y personalizables de creación.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 8%

---

# Crear con componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas.

Los componentes principales ofrecen funciones flexibles y personalizables de creación. El [sitio de referencia de WKND](https://wknd.site) y su ilustra cómo se pueden utilizar los componentes principales para implementar una experiencia enriquecida en el sitio web.

Para experimentar los componentes principales y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library).

Para obtener una introducción más detallada y orientada al desarrollador para implementar los componentes principales en un proyecto AEM mediante el [AEM tipo de archivo del proyecto](/help/developing/archetype/overview.md), consulte el [tutorial de WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](/help/get-started/using.md). Una vez integrados, pueden estar disponibles y preconfigurados mediante el [editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Los componentes principales [requieren AEM 6.4 o superior](/help/versions.md) y requieren el uso de [plantillas editables](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). No funcionan con la IU clásica ni con plantillas estáticas.

## Crear con componentes principales {#authoring-with-core-components}

Como autor, verá varias ventajas de los componentes principales, entre ellas:

* Fácil de usar y bien integrado con el [editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Funcionalidades enriquecidas con funciones para dar cabida a muchos casos de uso, como lo ilustra el [sitio de referencia de WKND](https://wknd.site) así como en la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library)

* [Pre-](#pre-configuring-core-components) configurable para definir qué funciones están disponibles para los autores de páginas a través del editor de  [plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Creado alrededor de [directrices de accesibilidad](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Creado para admitir [diseño interactivo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Creado para admitir [localización fácil](localization.md)

Los componentes están disponibles en la pestaña **Components** del panel lateral del editor de páginas al [editar una página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Los componentes se agrupan según categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el [navegador de componentes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son, de forma predeterminada, parte de un grupo oculto y no son visibles en el navegador de componentes.
>
>Agregue los componentes necesarios a un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

La configuración de componentes de base era tarea de un desarrollador. Sin embargo, con los componentes principales, un autor de plantillas ahora puede configurar una serie de funciones a través del editor de plantillas.

Por ejemplo, si un componente de imagen no debe permitir la carga de imágenes desde el sistema de archivos, o si un componente de texto solo debe permitir cierto formato de párrafo, estas funciones se pueden activar o desactivar con un simple clic.

Consulte [Creación de plantillas de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) para obtener más información.

### Editar y diseñar cuadros de diálogo {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir qué opciones se permiten como parte de una plantilla y, a continuación, el autor de la página puede configurarlas para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controla | Ejemplos |
|--- |--- |--- |--- |
| **Cuadro de diálogo Editar** | Opciones que un **autor de página** puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá finalmente en la página. | Formato del texto del contenido, girar una imagen en una página |
| **Cuadro de diálogo Diseño** | Opciones que un **autor de plantillas** puede modificar al configurar una plantilla de página. | Qué opciones tiene disponible el autor de la página al editar el componente | Qué opciones de formato de texto están disponibles, qué opciones de imagen in situ están disponibles |

### Estilo de componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilos de AEM.

* Un autor de plantillas puede definir qué estilos están disponibles para un componente en particular en el cuadro de diálogo Diseño de ese componente.
* El autor del contenido puede elegir qué estilos aplicar al añadir el componente y al crear contenido.

Para obtener más información, consulte la documentación de [Style System](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

## Medios del desarrollador {#developer-resources}

Consulte la documentación para desarrolladores de [Developing Core Components](/help/developing/overview.md) para obtener información técnica sobre los componentes principales.
