---
title: Introducción a los componentes principales
seo-title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas. '
seo-description: 'Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas. '
uuid: b815c7d1-fbb0-4480-bd23-42606ff8b1eb
contentOwner: User
content-type: reference
topic-tags: introduction
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: c44bb0d7-5d91-4659-878e-a0658fe29aa2
translation-type: tm+mt
source-git-commit: cbfc96bd215260e902f96c035a7889c968814e39

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas se simplifica pero mantiene su potencia para el autor; asimismo, el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas; igualmente, respetan las directivas de accesibilidad, y cumplen el estándar WCAG 2.0 AA. Los componentes principales hacen que la creación de páginas sea más flexible y personalizable, y ampliarla para ofrecer funcionalidades personalizadas es más sencillo para el desarrollador.

## Pruebe los componentes principales

Si quiere empezar a probar los componentes principales directamente, vaya a la [biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html). La biblioteca de componentes es una presentación en línea de la versión actual de la mayoría de los componentes principales, que le permite interactuar con variaciones de esos componentes, así como ver la salida HTML y JSON de muestra.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principales: funciones principales {#core-components-core-features}

Estos son los componentes principales:

|  |  |
|--- |--- |
| Preconfigurable | Las plantillas pueden definir el uso que pueden darles los autores de la página. |
| Versátil | Los autores pueden crear la mayoría de tipos de contenido con ellos. |
| Fácil de usar | Los autores pueden crear y administrar el contenido de manera eficiente con ellos. |
| Listo para la producción | Listo para usar. Son robustas, han sido ampliamente probadas y funcionan bien. |
| Accesible | Cumplen el estándar WCAG 2.0, proporcionan etiquetas de tipo ARIA y admiten la navegación mediante el teclado. |
| Fácil de diseñar | Los componentes implementan el sistema de estilos y el marcado sigue la nomenclatura de BEM CSS. |
| Compatible con SEO | La salida de HTML de salida es semántica y proporciona anotaciones de microdatos de tipo schema.org. |
| PWA/SPA/Preparado para la aplicación | Su elemento de salida JSON optimizado también se puede utilizar para el procesamiento en el lado del cliente. |
| Extensible | Todo se puede ampliar para cubrir las necesidades personalizadas y sin tener que empezar desde cero. |
| Código abierto | Si algo no funciona como es debido, envíe sus comentarios en GitHub (Licencia Apache) y ayúdenos a mejorar. |
| Con versiones | Los componentes principales interferirán en el funcionamiento del sitio al mejorar los elementos que esté usando. |
| [Localizado](localization.md) | La resolución de referencia inteligente permite a ciertos componentes buscar y reproducir automáticamente el contenido localizado correspondiente |

## Componentes disponibles {#available-components}

La versión actual de los componentes principales contiene los siguientes componentes.

* [Acordeón](accordion.md)
* [Ruta de navegación](breadcrumb.md)
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
* [Pestañas](tabs.md)
* [Texto](text.md)
* [Título](title.md)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) or in [design mode](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-designmode.html).

>[!CAUTION]
>
>Puede que algunas versiones de los componentes principales individuales solo sean compatibles con algunas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada a la lista anterior) para obtener información sobre la compatibilidad de componentes específicos o consulte el documento [Versiones de componentes principales](versions.md) para obtener más información.

## Cuándo utilizar los componentes principales {#when-to-use-core-components}

Como los componentes principales son completamente nuevos y ofrecen varios beneficios, se recomienda utilizarlos en los nuevos proyectos de AEM. En los proyectos existentes, la migración debería ser parte de un esfuerzo de proyecto aún mayor; por ejemplo, para realizar un cambio en la marca o la refactorización total.

Para obtener las recomendaciones de uso específico, consulte [¿Cuándo se deben utilizar los componentes principales?](developing.md) en el documento [Desarrollar componentes principales](developing.md).

## Información general de la sesión de Gems {#gems-session-overview}

Para obtener información básica de los componentes principales, las funciones que ofrecen y cómo se pueden aprovechar en AEM, consulte los componentes principales de AEM en la sesión de Gems de AEM [.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de inmersiones técnicas de expertos de Adobe. Esta serie complementa la documentación del producto y todos los demás canales técnicos, permitiendo así que los desarrolladores se pongan en contacto y profundicen en un tema específico.

## Desarrollo con los componentes principales {#developing-core-components}

Los componentes principales proporcionan componentes básicos robustos y ampliables que implementan varios patrones que facilitan la personalización, desde el estilo simple hasta la reutilización avanzada de la funcionalidad. Consulte la documentación [de desarrollo de componentes](developing.md) principales para obtener más información.

Empiece a desarrollar elementos en AEM Sites con componentes principales siguiendo [este tutorial paso a paso.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

No olvide iniciar su propio proyecto de AEM aprovechando el arquetipo [del proyecto de](archetype.md) AEM con los últimos componentes principales incorporados.

## Compatibilidad con componentes principales {#core-components-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que sucede con otras funciones del producto, la regla general de la fecha de vencimiento es:

* Los componentes se anuncian primero como en desuso antes de eliminarse
* Se eliminarán de la versión de AEM lo antes posible tras realizar el anuncio.

Esto proporciona a los clientes al menos un ciclo de lanzamiento para poder cambiarse a la nueva versión del componente antes de que finalice el servicio de soporte.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más detalles sobre la compatibilidad de la personalización de componentes, consulte la página [Personalización de componentes principales](customizing.md) de la versión del componente principal en cuestión.

## Compatibilidad con componentes de base {#foundation-component-support}

Dado que los componentes de base han servido de fundamento en el desarrollo de proyectos en muchas versiones, seguirán recibiendo ayuda técnica en el futuro.

However, Adobe's development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.
