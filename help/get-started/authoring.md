---
title: Crear con componentes principales
description: 'En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas que se crean: la oferta de componentes principales ofrece una funcionalidad de creación flexible y con muchas funciones.'
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 7%

---


# Autor con componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas.

La oferta de componentes principales ofrece una funcionalidad de creación flexible y rica en funciones. El [sitio de referencia de WKND](https://wknd.site) e ilustra cómo se pueden utilizar los componentes principales para implementar una experiencia de sitio Web enriquecida.

Para experimentar los componentes principales y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library).

Para obtener una introducción más detallada y orientada al desarrollador para implementar los Componentes principales en un proyecto AEM mediante el [AEM Arquetipo de proyecto](/help/developing/archetype/overview.md) consulte el tutorial de WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)[

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](/help/get-started/using.md). Una vez integrados, pueden estar disponibles y preconfigurados mediante el [editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Los componentes principales [requieren AEM 6.4 o superior](/help/versions.md) y requieren el uso de [plantillas editables](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). No funcionan con la IU clásica ni con plantillas estáticas.

## Crear con componentes principales {#authoring-with-core-components}

Como autor, notará varias ventajas de los componentes principales, entre las que se incluyen:

* Fácil de usar y bien integrado con el [editor de páginas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Capacidades ricas en funciones para dar cabida a muchos casos de uso, como se ilustra en el [sitio de referencia de WKND](https://wknd.site) así como en la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library)

* [Preconfigurable ](#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas mediante el editor de  [plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Creado en torno a [pautas de accesibilidad](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Creado para admitir [diseño interactivo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Creado para admitir [localización fácil](localization.md)

Los componentes están disponibles en la ficha **Componentes** del panel lateral del editor de páginas al [editar una página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Los componentes se agrupan según categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el [navegador de componentes](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son, de forma predeterminada, parte de un grupo oculto y no están visibles en el navegador de componentes.
>
>Añada los componentes necesarios en un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

La configuración de los componentes básicos era tarea de un desarrollador. Sin embargo, con los componentes principales, un autor de plantilla ahora puede configurar una serie de funciones mediante el editor de plantillas.

Por ejemplo, si un componente de imagen no debe permitir la carga de imágenes desde el sistema de archivos o si un componente de texto solo debe permitir cierto formato de párrafo, estas funciones se pueden activar o desactivar con un solo clic.

Consulte [Creación de plantillas de página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) para obtener más información.

### Editar y diseñar diálogos {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir qué opciones se permiten como parte de una plantilla y, a continuación, el autor de la página puede configurarlas para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controla | Ejemplos |
|--- |--- |--- |--- |
| **Editar cuadro de diálogo** | Opciones que un **autor de página** puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá en última instancia en la página. | Formato del texto del contenido, girar una imagen en una página |
| **Cuadro de diálogo Diseño** | Opciones que un **autor de plantilla** puede modificar al configurar una plantilla de página. | Qué opciones tiene disponible el autor de la página al editar el componente | Qué opciones de formato de texto están disponibles, qué opciones de imagen in situ están disponibles |

### Estilo del componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilo AEM.

* Un autor de plantilla puede definir qué estilos están disponibles para un componente concreto en el cuadro de diálogo Diseño de dicho componente.
* A continuación, el autor del contenido puede elegir qué estilos aplicar al agregar el componente y crear contenido.

Para obtener más información, consulte la documentación de [Style System](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html).

## Medios del desarrollador {#developer-resources}

Consulte la [documentación para desarrolladores de Componentes principales](/help/developing/overview.md) para obtener información técnica sobre los componentes principales.
