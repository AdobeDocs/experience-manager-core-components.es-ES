---
title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas. '
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas se simplifica pero mantiene su potencia para el autor; asimismo, el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas; igualmente, respetan las directivas de accesibilidad, y cumplen el estándar WCAG 2.0 AA. Los componentes principales hacen que la creación de páginas sea más flexible y personalizable, y ampliarla para ofrecer funcionalidades personalizadas es más sencillo para el desarrollador.

## Pruebe los componentes principales

Si quiere empezar a probar los componentes principales directamente, vaya a la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library). La biblioteca de componentes es una presentación en línea de la versión actual de la mayoría de los componentes principales, que le permite interactuar con variaciones de esos componentes, así como ver la salida HTML y JSON de muestra.

El tutorial [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) WKND también ilustra cómo se pueden utilizar los componentes principales.

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
| [Localizado](get-started/localization.md) | La resolución de referencia inteligente permite a determinados componentes buscar y procesar automáticamente el contenido localizado correspondiente |

## Componentes disponibles {#available-components}

La versión actual de los componentes principales contiene los siguientes componentes.

* [Acordeón](components/accordion.md)
* [Ruta de navegación](components/breadcrumb.md)
* [Botón](components/button.md)
* [Contenedor](components/container.md)
* [Carrusel](components/carousel.md)
* [Fragmento de contenido](components/content-fragment-component.md)
* [Lista de fragmentos de contenido](components/content-fragment-list.md)
* [Descargar](components/download.md)
* [Incrustar](components/embed.md)
* [Fragmento de experiencias](components/experience-fragment.md)
* [Botón de formulario](components/forms/form-button.md)
* [Contenedor del formulario](components/forms/form-container.md)
* [Formulario oculto](components/forms/form-hidden.md)
* [Opciones de formulario](components/forms/form-options.md)
* [Texto de formulario](components/forms/form-text.md)
* [Imagen](components/image.md)
* [Navegación por idiomas](components/language-navigation.md)
* [Lista](components/list.md)
* [Navegación](components/navigation.md)
* [Página](components/page.md)
* [Búsqueda rápida](components/quick-search.md)
* [Separador](components/separator.md)
* [Compartir en redes sociales](components/sharing.md)
* [Pestañas](components/tabs.md)
* [Texto](components/text.md)
* [Título](components/title.md)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Puede que algunas versiones de los componentes principales individuales solo sean compatibles con algunas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada a la lista anterior) para obtener información sobre la compatibilidad de componentes específicos o consulte el documento [Versiones de componentes principales](versions.md) para obtener más información.

## Cuándo utilizar los componentes principales {#when-to-use-core-components}

Como los componentes principales son completamente nuevos y ofrecen varios beneficios, se recomienda utilizarlos en los nuevos proyectos de AEM. En los proyectos existentes, la migración debería ser parte de un esfuerzo de proyecto aún mayor; por ejemplo, para realizar un cambio en la marca o la refactorización total.

Para obtener las recomendaciones de uso específico, consulte [¿Cuándo se deben utilizar los componentes principales?](developing/overview.md#when-to-use-the-core-components) en el documento [Desarrollar componentes principales](developing/overview.md).

## Información general de la sesión de Gems {#gems-session-overview}

Para obtener información básica de los componentes principales, las funciones que ofrecen y cómo se pueden aprovechar en AEM, consulte los componentes principales de AEM en la sesión de Gems de AEM [.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de inmersiones técnicas de expertos de Adobe. Esta serie complementa la documentación del producto y todos los demás canales técnicos, permitiendo así que los desarrolladores se pongan en contacto y profundicen en un tema específico.

## Desarrollo con los componentes principales {#developing-core-components}

Los componentes principales proporcionan componentes básicos robustos y ampliables que implementan varios patrones que facilitan la personalización, desde el estilo simple hasta la reutilización avanzada de la funcionalidad. Consulte la documentación [de desarrollo de los componentes](developing/overview.md) principales para obtener más información.

Empiece a desarrollar sitios de AEM con componentes principales siguiendo [el tutorial de WKND.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

No olvide iniciar su propio proyecto de AEM aprovechando el arquetipo [del proyecto de](developing/archetype/overview.md) AEM con los últimos componentes principales incorporados.

## Compatibilidad con componentes principales {#core-components-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que sucede con otras funciones del producto, la regla general de la fecha de vencimiento es:

* Los componentes se anuncian primero como en desuso antes de eliminarse
* Se eliminarán de la versión de AEM lo antes posible tras realizar el anuncio.

Esto proporciona a los clientes al menos un ciclo de lanzamiento para poder cambiarse a la nueva versión del componente antes de que finalice el servicio de soporte.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más detalles sobre la compatibilidad de la personalización de componentes, consulte la página [Personalización de componentes principales](developing/customizing.md) de la versión del componente principal en cuestión.

## Compatibilidad con componentes de base {#foundation-component-support}

Dado que los componentes de base han servido de fundamento en el desarrollo de proyectos en muchas versiones, seguirán recibiendo ayuda técnica en el futuro.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.
