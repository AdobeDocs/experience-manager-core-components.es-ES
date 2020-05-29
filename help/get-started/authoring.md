---
title: Crear con componentes principales
description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas que se crean: oferta de componentes principales, funcionalidad de creación flexible y con muchas funciones.'
translation-type: tm+mt
source-git-commit: 4281f6421482682f603f6a7f5e18df61f9a6d98c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 7%

---


# Autor con componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas.

La oferta de componentes principales ofrece una funcionalidad de creación flexible y rica en funciones. El sitio [de referencia](https://wknd.site) WKND y su informe ilustran cómo se pueden utilizar los componentes principales para implementar una experiencia de sitio web enriquecida.

Para experimentar los componentes principales y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library)componentes.

Para obtener una introducción más detallada y orientada al desarrollador sobre la implementación de los componentes principales en un proyecto de AEM mediante el arquetipo del proyecto de [AEM](/help/developing/archetype/overview.md) , consulte [el tutorial de WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](/help/get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Los componentes principales [requieren AEM 6.3 o superior](/help/versions.md) y el uso de plantillas [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)editables. No funcionan con la IU clásica ni con plantillas estáticas.

## Crear con componentes principales {#authoring-with-core-components}

Como autor, notará varias ventajas de los componentes principales, entre las que se incluyen:

* Simple to use and well-integrated with the [page editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Funciones ricas en funciones para dar cabida a muchos casos de uso, como se ilustra en el sitio [de referencia de](https://wknd.site) WKND y en la biblioteca de [componentes](https://adobe.com/go/aem_cmp_library)

* [Preconfigurable](#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas mediante el editor de [plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Built around [accessibility guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Built to support [responsive layout](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Diseñado para soportar una localización [sencilla](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Los componentes se agrupan según categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) componentes y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son, de forma predeterminada, parte de un grupo oculto y no están visibles en el navegador de componentes.
>
>Añada los componentes necesarios en un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

La configuración de los componentes básicos era tarea de un desarrollador. Sin embargo, con los componentes principales, un autor de plantilla ahora puede configurar una serie de funciones mediante el editor de plantillas.

Por ejemplo, si un componente de imagen no debe permitir la carga de imágenes desde el sistema de archivos o si un componente de texto solo debe permitir cierto formato de párrafo, estas funciones se pueden activar o desactivar con un solo clic.

Consulte [Creación de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) de página para obtener más información.

### Diálogos de edición y diseño {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir qué opciones se permiten como parte de una plantilla y, a continuación, el autor de la página puede configurarlas para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controla | Ejemplos |
|--- |--- |--- |--- |
| **Editar cuadro de diálogo** | Opciones que un autor **de una** página puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá en última instancia en la página. | Formato del texto del contenido, girar una imagen en una página |
| **Cuadro de diálogo Diseño** | Opciones que el autor **de una** plantilla puede modificar al configurar una plantilla de página. | Qué opciones tiene disponible el autor de la página al editar el componente | Qué opciones de formato de texto están disponibles, qué opciones de imagen in situ están disponibles |

### Estilo de componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilo AEM.

* Un autor de plantilla puede definir qué estilos están disponibles para un componente concreto en el cuadro de diálogo Diseño de dicho componente.
* A continuación, el autor del contenido puede elegir qué estilos aplicar al agregar el componente y crear contenido.

Para obtener más información, consulte la documentación [del sistema](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) de estilos.

>[!NOTE]
>
>En AEM 6.3, se requiere el Service Pack 2 (6.3.2.0) o una versión posterior para activar la función del sistema de estilo.

## Medios del desarrollador {#developer-resources}

Consulte la documentación para desarrolladores de [Desarrollar componentes](/help/developing/overview.md) principales para obtener información técnica sobre los componentes principales.
