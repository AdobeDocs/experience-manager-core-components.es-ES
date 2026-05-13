---
title: Crear con componentes principales
description: En AEM, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes principales ofrecen funciones flexibles y personalizables de creación.
role: Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
TQID: https://experienceleague.adobe.com/iLP4KD5kWkBaZ3b4c6Kos9ltFf1MBAZHPwN6wkcWrcY
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2: id: a6c0bfb4-91d0-4952-9c1d-c7f39e7705c4id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 792
ht-degree: 100%

---

# Crear con Componentes principales

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas.

Los componentes principales ofrecen funciones flexibles y personalizables de creación. El [sitio de referencia de WKND](https://wknd.site) ilustra cómo se pueden utilizar los componentes principales para implementar una experiencia enriquecida en el sitio web.

Para utilizar los componentes principales y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_es).

Para obtener una introducción más detallada y orientada al desarrollador para implementar los componentes principales en un proyecto AEM mediante el [Tipo de archivo del proyecto AEM](/help/developing/archetype/overview.md), consulte el [tutorial de WKND.](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](/help/get-started/using.md). Una vez integrados, pueden ponerse a disposición de los usuarios y preconfigurarse mediante el [editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

>[!CAUTION]
>
>Los componentes principales [requieren AEM 6.4 o superior](/help/versions.md) y requieren el uso de [plantillas editables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es). No funcionan con la IU clásica ni con plantillas estáticas.

## Crear con componentes principales {#authoring-with-core-components}

Como autor, notará que los componentes principales ofrecen varias ventajas, como las siguientes:

* Son fáciles de usar y se integran bien con el [editor de páginas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es)

* Funcionalidades enriquecidas con funciones para dar cabida a muchos casos de uso, como se puede ver en el [sitio de referencia de WKND](https://wknd.site) así como en la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_es)

* [Preconfigurable](#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas a través del [editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

* Han sido creados según las [directrices de accesibilidad](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=es)

* Permiten un [diseño interactivo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=es)

* Creado para conseguir una [localización fácil](localization.md)

Los componentes están disponibles en la pestaña **Componentes** del panel lateral del editor de páginas al [editar una página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es).

Los componentes se agrupan según categorías denominadas grupos de componentes para organizar y filtrar fácilmente los componentes. El nombre del grupo de componentes se muestra con el componente en el [navegador de componentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es) y también es posible filtrar por grupo para encontrar fácilmente el componente correcto.

>[!NOTE]
>
>Los componentes principales son, de forma predeterminada, parte de un grupo oculto y no son visibles en el navegador de componentes.
>
>Agregue los componentes necesarios a un grupo visible o personalícelos para que estén disponibles para los autores.

## Preconfiguración de componentes principales {#pre-configuring-core-components}

La configuración de componentes de base era tarea de un desarrollador. Sin embargo, con los componentes principales, un autor de plantillas ahora puede configurar una serie de funciones a través del editor de plantillas.

Por ejemplo, si un componente de imagen no debe permitir la carga de imágenes desde el sistema de archivos, o si un componente Texto solo debe permitir cierto formato de párrafo, estas funciones se pueden activar o desactivar con un simple clic.

Consulte [Creación de plantillas de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) para obtener más información.

### Editar y diseñar cuadros de diálogo {#edit-and-design-dialogs}

Dado que los autores de plantillas pueden preconfigurar los componentes principales para definir qué opciones se permiten como parte de una plantilla y, a continuación, el autor de la página puede configurarlas para definir el contenido real de la página, cada componente puede tener opciones en dos cuadros de diálogo diferentes.

|  | Descripción | Qué controla | Ejemplos |
|--- |--- |--- |--- |
| **Cuadro de diálogo de edición** | Opciones que un **autor de página** puede modificar durante la edición normal de la página para los componentes colocados | El contenido que muestra el componente y cómo aparecerá finalmente en la página. | Formato del texto del contenido, girar una imagen en una página |
| **Cuadro de diálogo de diseño** | Opciones que un **autor de plantillas** puede modificar al configurar una plantilla de página. | Qué opciones tiene disponible el autor de la página al editar el componente | Qué opciones de formato de texto están disponibles, qué opciones de imagen in situ están disponibles |

### Estilo de componente {#component-styling}

Los estilos de la mayoría de los componentes principales se pueden definir con el sistema de estilos de AEM.

* Un autor de plantillas puede definir qué estilos están disponibles para un componente en particular en el cuadro de diálogo de diseño de ese componente.
* El autor del contenido puede elegir qué estilos aplicar al añadir el componente y al crear contenido.

Para obtener más información, consulte la documentación de [Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=es).

## Recursos del desarrollador {#developer-resources}

Consulte la documentación para desarrolladores de [Desarrollo de Componentes principales](/help/developing/overview.md) para obtener información técnica sobre los componentes principales.
