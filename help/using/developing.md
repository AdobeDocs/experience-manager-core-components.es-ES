---
title: Desarrollo de componentes principales
seo-title: Desarrollo de componentes principales
description: Los componentes principales proporcionan componentes base sólidos y ampliables que ofrecen capacidades ricas en funciones, entrega continua, control de versiones, implementación moderna, marcado final y exportación de contenido JSON.
seo-description: Los componentes principales proporcionan componentes base sólidos y ampliables que ofrecen capacidades ricas en funciones, entrega continua, control de versiones, implementación moderna, marcado final y exportación de contenido JSON.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: Usuario
content-type: referencia
topic-tags: desarrollar
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 157 a 2 ec 3-9 fca -4 fad -977 a-d 93013 eeb 218
translation-type: tm+mt
source-git-commit: f30a6a9f4d41c672472beb60767f3766479d9c16

---


# Developing Core Components{#developing-core-components}

## Información general {#overview}

Los componentes principales proporcionan componentes base sólidos y extensibles, y sus resaltados son:

* Funciones ricas en funciones
   * [Opciones flexibles de configuración](authoring.md) para dar cabida a muchos casos de uso
   * [Capacidades preconfigurables](authoring.md#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas
* Entrega continua
   * Mejoras frecuentes de funcionalidad incremental
   * Availability of the [source code on GitHub](https://github.com/adobe/aem-core-wcm-components) to allow the developer community to give feedback and contribute
   * Installation through a [separately released content package](https://github.com/adobe/aem-core-wcm-components/releases) for component upgrades to be done independently from AEM upgrades
* [Control de versiones de componentes](guidelines.md#component-versioning)
   * [Garantice la compatibilidad dentro de una versión](#upgrade-of-core-components), pero permita que los componentes evolucionen
   * Permitir coexistir varias versiones de un componente en el mismo entorno
* Implementación moderna
   * Markup defined in [HTML Template Language](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Content model logic implemented with [Sling Models](https://sling.apache.org/documentation/bundles/models.html)
* Marcado de marca
   * Following [Block Element Modifier](https://getbem.com/) (BEM) notation as of Release 2.0.0
      * Prior release follow [Bootstrap](https://getbootstrap.com/css/) naming conventions
   * Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capacidad para utilizarse para sitios interactivos y móviles
* Capacidad para serializar como JSON el modelo de contenido para casos de uso CMS headless
* Accesible
   * Compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Core Components require AEM 6.3 or later and Java 8 and and require the use of [editable templates](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>Los componentes principales no funcionan con la IU clásica ni con las plantillas estáticas.

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Maravillas de Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de consejos técnicos proporcionados por expertos de Adobe. Esta serie complementa la documentación del producto y de todos los demás canales técnicos, lo que permite a los desarrolladores familiarizarse con un tema específico.

## WKND Developer Tutorial {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Delivered over GitHub {#delivered-over-github}

Los componentes principales se desarrollan y se entregan a través de github.

CÓDIGO EN GITHUB

Puede encontrar el código de esta página en github

* [Abra el proyecto aem-core-wcm-components en github](https://github.com/adobe/aem-core-wcm-components)
* Download the project as [a ZIP file](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

See the [Using Core Components](using.md) documentation page to learn how to get started using them in your project.

Si tiene los componentes principales en github, podrá realizar actualizaciones frecuentes y escuchar los comentarios de la comunidad de desarrolladores de AEM. Además, esto debería ayudar a los clientes y a los socios a seguir patrones similares al crear componentes personalizados.

>[!NOTE]
>
>To keep up-to-date on the latest changes to the core components, you can watch the [Core Components repository](https://github.com/adobe/aem-core-wcm-components) on GitHub.

## Biblioteca de componentes

Check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

### Sample Content Run-Mode {#sample-content-run-mode}

The Core Components are visible in the Quickstart when the sample content is present, because the [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) uses them. However, when running in production (in `nosamplecontent` runmode, without sample content enabled), the core components won&#39;t be present anymore and must be installed on the AEM instances by the development and/or operations team.

>[!NOTE]
>
>In production environments, always run the Quickstart in `nosamplecontent` runmode. To use the Core Components in `nosamplecontent` runmode, follow the instructions of the [Using Core Components](using.md) documentation page.

## Technical Capabilities {#technical-capabilities}

La siguiente tabla proporciona una descripción general de las diferencias entre los componentes principales y los componentes de base.

For details about their authoring capabilities and options to pre-configurable them, [refer to the authoring page about them](authoring.md).

| **Capacidad** | **Componente principal** | **Componente Foundation** |
|-----|---|---|
| Implementación de lógica | Java POJOs with [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotations | Código JSP |
| Definición de marcado | [Sintaxis del lenguaje](https://helpx.adobe.com/experience-manager/htl/user-guide.html) de plantilla HTML (HTL) | Código JSP |
| sanitización XSS | Automatizado por HTL | Principalmente manual |
| Nomenclatura de clases CSS | Standardized naming convention based on [Block Element Modifier](https://getbem.com/) (BEM) notation (as of release 2.0.0) | Esquemas personalizados |
| Definición del cuadro de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU clásica |
| Salida JSON | [Sling Models Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling predeterminado |
| Versiones | [Para el modelo y HTL](guidelines.md) | Ninguna |
| Pruebas | Pruebas unitarias + Pruebas de integración | Pruebas de integración |
| Entrega | [A través de github pública](https://github.com/adobe/aem-core-wcm-components) | A través de Quickstart |
| Licencia | [Licencia de Apache](https://www.apache.org/licenses/LICENSE-2.0) | Propiedad de Adobe |
| Contribución | Mediante solicitud de extracción | No posible |
| Accesibilidad | Fully compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Only partially compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Component List {#component-list}

La siguiente tabla enumera los componentes principales disponibles, vincula a su API e indica qué componentes base sustituyen.

| Componente principal | Descripción | Se reemplazaron los componentes de base |
|---|---|---|
| [Página](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Página adaptable que funciona con el editor de plantillas | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Ruta de exploración](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navegación por jerarquía de páginas | `/libs/foundation/components/breadcrumb` |
| [Título](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | Título H 1-H 6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texto enriquecido | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagen](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Carga inteligente y diferida del tamaño de representación óptimo | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartir en redes sociales](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Utilidad para compartir Facebook y Pinterest | `-` |
| [Contenedor del formulario](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Sistema de párrafos de formulario interactivo | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto de formulario](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opciones de formulario](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Campo de entrada de varias opciones | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulario oculto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botón de formulario](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Botón de envío o personalizado | `/libs/foundation/components/form/submit` |
| [Navegación](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Un componente de navegación del sitio que enumera la jerarquía de páginas anidada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegación por idiomas](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Un cambio de idioma y país que indica la estructura de idioma global | `-` |
| [Búsqueda rápida](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Componente de búsqueda que muestra los resultados como sugerencias in-situ en un menú desplegable | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Permite al autor de contenido crear fácilmente un teaser para más contenido utilizando una imagen, un título o un texto enriquecido y vinculando a contenido u otras acciones | `-` |
| [Fichas](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Permite al autor del contenido organizar el contenido de la página en varias fichas | `-` |
| [Carrusel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Permite al autor del contenido organizar el contenido en un carrusel rotatorio de diapositivas | `/libs/foundation/components/carousel` |
| [Fragmento de contenido](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Permite la visualización de un fragmento de contenido | `-` |
| [Lista de fragmentos de contenido](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Permite mostrar una lista de fragmentos de contenido | `-` |
| [Separador](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Separa el contenido de una página | `-` |
| [Acordeón](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion) | Organización de paneles de contenido en un acordeón contraíble | `-` |
| [Contenedor](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container) | Organización de componentes dentro de un contenedor | `-` |
| [Botón](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button) | Crear un botón en una página | `-` |
| [Descargar](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download) | Agregar un recurso descargable a una página | `-` |

### Upcoming Components {#upcoming-components}

For an overview of the upcoming Core Componente roadmap see the [project wiki on GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade of Core Components {#upgrade-of-core-components}

Una ventaja de los componentes con versiones es que permite separar la migración a una nueva versión de AEM desde la migración a nuevas versiones de componentes. Además, si hay nuevas versiones de componentes disponibles, permite la migración individual de cada componente a la nueva versión.

Las migraciones a una nueva versión de AEM no afectarán el funcionamiento de los componentes principales, siempre y cuando sus versiones también admitan la nueva versión de AEM a la que se migra. Customizations made to the Core Components should not be affected either, as long as they don&#39;t use APIs that have been [deprecated or removed](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Las migraciones a nuevas versiones de los componentes principales no afectan a la forma en que funciona el componente, pero es posible que se introduzcan nuevas funciones en los autores de páginas, lo que puede requerir cierta configuración por parte de un editor de plantillas, por si no se desea el comportamiento predeterminado. Customizations however might need to be adapted, for more details see the [Customizing Core Components](customizing.md#upgrade-compatibility-of-customizations) page.

## When to Use the Core Components? {#when-to-use-the-core-components}

Dado que los componentes principales son totalmente nuevos y ofrecen múltiples beneficios, se recomienda que los nuevos proyectos de AEM puedan usarlos. Para los proyectos existentes, una migración debe formar parte de un esfuerzo de proyecto más grande, por ejemplo una remarca o una refactorización general.

Por lo tanto, Adobe proporciona recomendaciones siguientes:

* **Nuevos proyectos**
Los proyectos nuevos siempre deberían intentar utilizar componentes principales. If Core Components cannot be used directly or [extended](customizing.md) to satisfy project requirements, then create a custom component following the component architecture set forth in core components. Except where not otherwise possible, avoid using the [foundation components](developing.md).
* **La Recomendación de proyectos**
existente sigue usando los componentes [](developing.md)base, a menos que se planifique una refactorización del sitio o del componente.\
   As they are very widely used by most existing projects, the foundation components [will continue to be supported.](developing.md)
* **Nuevos componentes**
personalizados Si se puede personalizar un componente [Core existente](customizing.md).\
   If not, recommendation is to build a new custom component following the [Component Guidelines](guidelines.md).
* **Componentes
personalizados existentes** Si los componentes funcionan correctamente, manténgalos tal y como están.\
   Si no es así, consulte &quot;Nuevos componentes personalizados&quot; arriba.

## Migración a componentes principales

Cualquier proyecto nuevo debe implementarse con Componentes principales. Sin embargo, los proyectos existentes generalmente tendrán implementaciones amplias de los componentes de base.

Un esfuerzo mayor en un proyecto existente (por ejemplo, una refactorización o refactorización general) a menudo ofrece la posibilidad de migrar a los componentes principales. Para facilitar esta migración, Adobe ha proporcionado una serie de herramientas de migración para estimular la adopción de los componentes principales y la última tecnología de AEM.

[Las herramientas de modernización de AEM](http://opensource.adobe.com/aem-modernize-tools/) permiten la conversión sencilla de:

* Plantillas estáticas para plantillas editables
* Configuración de diseño a políticas
* Componentes básicos a componentes principales
* IU clásica a IU táctil

For further information about the usage of these tools, [see their documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Las herramientas de AEM Moderntools son un esfuerzo de comunidad que no son compatibles ni son garantizadas por Adobe.

## Core Component Support {#core-component-support}

Los componentes principales forman parte integral de AEM y se admiten tal y como está, bajo los mismos términos y condiciones que si se entregaran como parte de Quickstart.

Al igual que otras funciones de productos de AEM, la regla general es: Los componentes se anuncian en primer lugar en desuso y se eliminan primero para la siguiente versión de AEM. Esto proporciona a los clientes al menos un ciclo de publicación para moverse a la nueva versión del componente, antes de colocar su asistencia.

La versión de cada componente indica claramente las versiones de AEM que admite. Cuando la compatibilidad deja de aplicarse a una versión de AEM, entonces es compatible con los componentes principales para esa versión de AEM.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page.

## Foundation Component Support {#foundation-component-support}

Dado que los componentes base han servido como base para el desarrollo de tantos proyectos en muchas versiones AEM, seguirán siendo compatibles en un futuro próximo.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

**Siguiente:**

* [Uso de componentes](using.md) principales: familiarícese con los componentes principales en su propio proyecto.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
