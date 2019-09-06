---
title: Introducción a los componentes principales
seo-title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes base sólidos y ampliables, basados en la tecnología más reciente y en las prácticas recomendadas. '
seo-description: 'Los componentes principales se introdujeron para proporcionar componentes base sólidos y ampliables, basados en la tecnología más reciente y en las prácticas recomendadas. '
uuid: b 815 c 7 d 1-fbb 0-4480-bd 23-42606 ff 8 b 1 eb
contentOwner: Usuario
content-type: referencia
topic-tags: introducción
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: c 44 bb 0 d 7-5 d 91-4659-878 e-a 0658 fe 29 aa 2
translation-type: tm+mt
source-git-commit: 63e75079e41d3091ca57bfc3129e700675bf4939

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, lo que hace que la creación de páginas sea sencilla pero potente para el autor y que el desarrollo de componentes sea flexible y extensible para el desarrollador.

Los componentes principales se introdujeron para proporcionar componentes base sólidos y ampliables, basados en la tecnología y las prácticas recomendadas más recientes, y cumplir las directrices de accesibilidad y cumplir con el estándar WCAG 2.0 AA. Los componentes principales hacen que la creación de páginas sea más flexible y personalizable, y ampliarlos para ofrecer funcionalidad personalizada es simple para el desarrollador.

## Probar los componentes principales

Si desea comenzar a probar directamente los componentes principales, coloque el puntero sobre la biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html). La biblioteca de componentes es una vidriera en línea de la versión actual de la mayoría de los componentes principales, lo que permite interactuar con variaciones de los componentes, así como ver la salida HTML y JSON de muestra.

The [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html) also illustrates how the core components can be used.

## Componentes principales: funciones principales {#core-components-core-features}

Los componentes principales son:

|  |  |
|--- |--- |
| Preconfigurable | Las plantillas pueden definir cómo pueden usarlos los autores de páginas. |
| Versátil | Los autores pueden crear más contenido con ellos. |
| Fácil de utilizar | Los autores pueden crear y administrar con eficacia contenido con ellos. |
| Producción listo | Se puede utilizar directamente. Son robustas, bien probados y funcionan bien. |
| Accesible | Cumplen el estándar WCAG 2.0, proporcionan etiquetas ARIA y admiten la navegación por teclado. |
| Fácil de estilo | Los componentes implementan el sistema de estilos y el marcado sigue la nomenclatura BEM CSS. |
| SEO sencillo | El resultado HTML es semántica y proporciona schema.org microdata annotations. |
| PWA/SPA/App Ready | Su salida JSON racionalizada también se puede utilizar para procesar el lado del cliente. |
| Extensible | Para cubrir necesidades personalizadas, pero sin empezar desde cero, todo se puede ampliar. |
| Código abierto | Si algo no es así, contribuye con mejoras en github (Apache License). |
| Versiones | Los componentes principales no romperán el sitio al mejorar las cosas que puedan afectarle. |

## Componentes disponibles {#available-components}

La versión actual de los componentes principales incluye los componentes siguientes.

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
>Algunas versiones de componentes principales individuales pueden ser compatibles únicamente con ciertas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada en la lista anterior) para el componente específico de información de compatibilidad o haga referencia al [documento Versiones](versions.md) de componentes principales para obtener más información.

## Cuándo utilizar los componentes principales {#when-to-use-core-components}

Dado que los componentes principales son totalmente nuevos y ofrecen múltiples beneficios, se recomienda que los nuevos proyectos de AEM puedan usarlos. Para los proyectos existentes, una migración debe formar parte de un esfuerzo de proyecto más grande, por ejemplo una remarca o una refactorización general.

Para utilizar recomendaciones específicas, consulte [Cuándo utilizar los componentes principales?](developing.md) en [el documento Desarrollo de componentes](developing.md) principales.

## Información general de sesión de Gems {#gems-session-overview}

Para obtener una introducción a los componentes principales, las características que ofrecen y cómo se aprovechan en AEM, consulte los componentes de AEM Session [AEM Session de AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Maravillas de Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de consejos técnicos proporcionados por expertos de Adobe. Esta serie complementa la documentación del producto y de todos los demás canales técnicos, lo que permite a los desarrolladores familiarizarse con un tema específico.

## Tutorial para desarrolladores WKND {#wknd-developer-tutorial}

Aprenda a desarrollar sitios AEM con componentes principales siguiendo [este paso paso a paso.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Compatibilidad con componentes principales {#core-components-support}

Los componentes principales forman parte integral de AEM y se admiten tal y como está, bajo los mismos términos y condiciones que si se entregaran como parte de Quickstart.

Al igual que otras funciones del producto, la regla general del final de la vida útil es:

* Primero se anunciará que los componentes estén obsoletos antes de eliminarse
* Al principio, se eliminan de la versión AEM después del anuncio.

Esto proporciona a los clientes al menos un ciclo de publicación para moverse a la nueva versión del componente, antes de que finalice la asistencia.

La versión de cada componente indica claramente las versiones de AEM que admite. Cuando la compatibilidad deja de aplicarse a una versión de AEM, entonces es compatible con los componentes principales para esa versión de AEM.

Para obtener más información sobre la compatibilidad de las personalizaciones de componentes, consulte [la página Personalización de componentes](customizing.md) principales de la versión relevante de componentes principales.

## Compatibilidad con componentes base {#foundation-component-support}

Dado que los componentes Foundation han servido como base para el desarrollo de tantos proyectos en muchas versiones, seguirán siendo compatibles en un futuro próximo.

Sin embargo, el énfasis de desarrollo de Adobe se ha trasladado a los componentes principales y se agregarán nuevas funciones, mientras [que casi todos los componentes Foundation se han quedado obsoletos con AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) y solo se realizarán correcciones de errores en los componentes de base.
