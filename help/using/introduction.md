---
title: Introducción a los componentes principales
seo-title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes básicos robustos y ampliables, basados en la tecnología más reciente y las mejores prácticas. '
seo-description: 'Los componentes principales se introdujeron para proporcionar componentes básicos robustos y ampliables, basados en la tecnología más reciente y las mejores prácticas. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: Usuario
content-type: referencia
topic-tags: introducción
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: tm+mt
source-git-commit: b6fbef1cff2908533df6573cd3a92266857ba93f

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas es sencilla pero potente para el autor y el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales se introdujeron para proporcionar componentes básicos robustos y ampliables, basados en las últimas tecnologías y prácticas recomendadas, y respetando las directrices de accesibilidad, y cumpliendo la norma WCAG 2.0 AA. Los componentes principales hacen que la creación de páginas sea más flexible y personalizable, y ampliarla para ofrecer funcionalidad personalizada es sencillo para el desarrollador.

## Pruebe los componentes principales

Si desea empezar a probar los componentes principales directamente, vaya a la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library.html)componentes. La biblioteca de componentes es una muestra en línea de la versión actual de la mayoría de los componentes principales, que le permite interactuar con variaciones de los componentes, así como ver la salida HTML y JSON de muestra.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principales: funciones principales {#core-components-core-features}

Los componentes principales son:

|  |  |
|--- |--- |
| Preconfigurable | Las plantillas pueden definir cómo los autores de la página pueden utilizarlos. |
| Versátil | Los autores pueden crear la mayor parte del contenido con ellos. |
| Fácil de usar | Los autores pueden crear y administrar contenido con ellos de forma eficaz. |
| Listo para la producción | ¡Usable y listo para usar! Son robustas, están bien probadas y funcionan bien. |
| Accesible | Cumplen el estándar WCAG 2.0, proporcionan etiquetas ARIA y admiten la navegación mediante el teclado. |
| Fácil de estilo | Los componentes implementan el sistema de estilos y el marcado sigue la nominación de BEM CSS. |
| Compatible con SEO | El resultado HTML es semántico y proporciona anotaciones de microdatos de schema.org. |
| PWA/SPA/Preparado para la aplicación | Su salida JSON optimizada también se puede utilizar para el procesamiento en el lado del cliente. |
| Extensible | Para cubrir las necesidades personalizadas pero sin empezar desde cero, todo se puede ampliar. |
| Open Source | Si algo no es como debería ser, contribuya con mejoras en GitHub (Licencia Apache). |
| Con versiones | Los componentes principales no interrumpirán el sitio al mejorar las cosas que puedan afectarle. |
| [Localizado](localization.md) | La resolución de referencias inteligentes permite a determinados componentes buscar y procesar automáticamente el contenido localizado correspondiente |

## Componentes disponibles {#available-components}

La versión actual de los componentes principales incluye los siguientes componentes.

* [Acordeón](accordion.md)
* [Ruta de exploración](breadcrumb.md)
* [Botón](button.md)
* [Contenedor](container.md)
* [Carrusel](carousel.md)
* [Fragmento de contenido](content-fragment-component.md)
* [Lista de fragmentos de contenido](content-fragment-list.md)
* [Descargar](download.md)
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

>[!NOTE]
>
>Core Components are not immediately available to authors, the [development team must first integrate them to your environment](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Es posible que algunas versiones de componentes principales individuales solo sean compatibles con determinadas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada en la lista anterior) del componente específico para obtener información de compatibilidad o consulte el documento Versiones [de componentes](versions.md) principales para obtener más información.

## Cuándo utilizar los componentes principales {#when-to-use-core-components}

Dado que los componentes principales son completamente nuevos y ofrecen varias ventajas, se recomienda que los nuevos proyectos de AEM los utilicen. En el caso de los proyectos existentes, una migración debería formar parte de un esfuerzo de proyecto más amplio, por ejemplo, una renovación de la marca o una refactorización general.

Para obtener recomendaciones de uso específicas, consulte [¿Cuándo utilizar los componentes principales?](developing.md) en el documento [Desarrollar componentes](developing.md) principales.

## Información general de la sesión de Gems {#gems-session-overview}

Para obtener una introducción a los componentes principales, las funciones que ofrecen y cómo se aprovechan en AEM, consulte los componentes principales de AEM [AEM Gems Session.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de inmersiones técnicas de expertos de Adobe. Esta serie complementa la documentación del producto y todos los demás canales técnicos, permitiendo a los desarrolladores ponerse en contacto y profundizar en un tema específico.

## Tutorial para desarrolladores de WKND {#wknd-developer-tutorial}

Empiece a desarrollar sitios de AEM con componentes principales siguiendo [este tutorial paso a paso.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Compatibilidad con componentes principales {#core-components-support}

Los componentes principales son una parte integral de AEM y se admiten tal cual, en los mismos términos y condiciones que si se hubieran entregado como parte de QuickStart.

Al igual que otras características del producto, la regla general de caducidad es:

* Los componentes se anuncian primero como obsoletos antes de eliminarse
* Como muy pronto se eliminarán de la versión de AEM tras el anuncio.

Esto permite a los clientes pasar al menos un ciclo de lanzamiento a la nueva versión del componente antes de que finalice la compatibilidad.

La versión de cada componente indica claramente las versiones de AEM que admite. Cuando la compatibilidad para una versión de AEM deja de ser compatible, también lo es la compatibilidad de los componentes principales para esa versión de AEM.

Para obtener más información sobre la compatibilidad con las personalizaciones de componentes, consulte la página [Personalización de componentes](customizing.md) principales de la versión de componentes principales correspondiente.

## Compatibilidad con componentes de base {#foundation-component-support}

Dado que los componentes básicos han servido de base para tanto desarrollo de proyectos en muchas versiones, seguirán recibiendo apoyo en el futuro previsible.

Sin embargo, el énfasis de Adobe en el desarrollo ha cambiado a los componentes principales y se les añadirán nuevas funciones, mientras que [casi todos los componentes de base han quedado obsoletos con AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) y solo se corregirán los errores en los componentes de base a partir de ahora.
