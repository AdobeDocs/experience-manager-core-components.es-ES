---
title: Desarrollo de componentes principales
description: Los componentes principales proporcionan componentes básicos robustos y ampliables que ofrecen funciones enriquecidas, entrega continua, versiones de componentes, implementación moderna, marcado ligero y exportación de contenido JSON.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Desarrollo de componentes principales {#developing-core-components}

## Información general {#overview}

Los componentes principales proporcionan componentes básicos robustos y ampliables, y sus aspectos destacados son:

* Funciones ricas en funciones
   * [Opciones](/help/get-started/authoring.md) de configuración flexibles para admitir muchos casos de uso
   * [Capacidades](/help/get-started/authoring.md#pre-configuring-core-components) preconfigurables para definir qué funciones están disponibles para los creadores de páginas
* Entrega continua
   * Mejoras frecuentes en la funcionalidad incremental
   * Disponibilidad del código [fuente en GitHub](https://github.com/adobe/aem-core-wcm-components) para permitir a la comunidad de desarrolladores dar sus comentarios y contribuir
   * Instalación mediante un paquete [de contenido liberado](https://github.com/adobe/aem-core-wcm-components/releases) por separado para las actualizaciones de componentes que se realizan de forma independiente de las actualizaciones de AEM
* [Versiones de componentes](guidelines.md#component-versioning)
   * [Garantizar la compatibilidad dentro de una versión](#upgrade-of-core-components), pero permitir que los componentes evolucionen
   * Permitir que varias versiones de un componente coexistan en el mismo entorno
* Implementación moderna
   * Marca definida en lenguaje [de plantilla](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) HTML (HTL)
   * Lógica del modelo de contenido implementada con modelos [Sling](https://sling.apache.org/documentation/bundles/models.html)
* Marcado de pérdida
   * Notación del modificador [de elementos de](https://getbem.com/) bloque (BEM) siguiente a partir de la versión 2.0.0
      * La versión anterior sigue las convenciones de nomenclatura de [Bootstrap](https://getbootstrap.com/css/) .
   * Built around [accessibility guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)
   * Capacidad para utilizarse en sitios adaptables y móviles
* Capacidad de serializar como JSON el modelo de contenido para casos de uso CMS sin encabezado
* Accesible
   * Compatible con el estándar [WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

>[!CAUTION]
>
>Los componentes principales requieren AEM 6.3 o posterior y Java 8 y requieren el uso de plantillas [editables](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
>
>Los componentes principales no funcionan con la IU clásica ni con plantillas estáticas.

## Información general de la sesión de Gems {#gems-session-overview}

Para obtener información básica de los componentes principales, las funciones que ofrecen y cómo se pueden aprovechar en AEM, consulte los componentes principales de AEM en la sesión de Gems de AEM [.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de inmersiones técnicas de expertos de Adobe. Esta serie complementa la documentación del producto y todos los demás canales técnicos, permitiendo así que los desarrolladores se pongan en contacto y profundicen en un tema específico.

## Tutorial para desarrolladores de WKND {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Tipo de archivo del proyecto AEM {#aem-project-archetype}

[El arquetipo](/help/developing/archetype/overview.md) de proyecto de AEM crea un proyecto mínimo de Adobe Experience Manager como punto de partida para sus propios proyectos, incluido un ejemplo de componentes HTML personalizados con SlingModels para la lógica y la correcta implementación de los componentes principales con el patrón proxy recomendado.

## Entregado a través de GitHub {#delivered-over-github}

Los componentes principales se desarrollan en GitHub y se entregan a través de él.

CÓDIGO DE GITHUB

Puede encontrar el código de esta página en GitHub

* [Abrir un proyecto de aem-core-wcm-components en GitHub](https://github.com/adobe/aem-core-wcm-components)
* Descargar el proyecto como [archivo ZIP](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Consulte la página de documentación [Uso de componentes](/help/get-started/using.md) principales para obtener información sobre cómo empezar a utilizarlos en el proyecto.

Tener los componentes principales en GitHub permitirá realizar actualizaciones frecuentes y escuchar los comentarios de la comunidad de desarrolladores de AEM. Además, esto debería ayudar a los clientes y socios a seguir patrones similares al crear componentes personalizados.

>[!NOTE]
>
>Para mantenerse al día sobre los últimos cambios en los componentes principales, puede ver el repositorio [de componentes](https://github.com/adobe/aem-core-wcm-components) principales en GitHub.

## Biblioteca de componentes

Consulte la biblioteca [de](https://adobe.com/go/aem_cmp_library)componentes, que muestra la versión actual de los componentes principales y ofrece ejemplos de su uso.

### Componentes principales listos para usar {#out-of-the-box}

Los componentes principales pueden instalarse o no automáticamente en función de cómo se ejecute AEM.

#### AEM como Cloud Service {#aem-cloud-service}

Aunque los componentes principales son totalmente compatibles con [AEM como servicio](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)de nube, los componentes principales deben instalarse manualmente y no están disponibles de forma predeterminada.

#### AEM In situ {#on-premise}

En las instalaciones locales, los componentes principales son visibles en el inicio rápido cuando el contenido de muestra está presente, ya que el sitio [de referencia](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) We.Retail los utiliza. Sin embargo, al ejecutarse en producción (en `nosamplecontent` modo de ejecución, sin contenido de muestra activado), los componentes principales ya no estarán presentes y deben instalarse en la instancia de AEM.

>[!NOTE]
>
>En los entornos de producción locales, ejecute siempre Quickstart en `nosamplecontent` modo de ejecución. Para utilizar los componentes principales en `nosamplecontent` modo de ejecución, siga las instrucciones de la página de documentación [Uso de componentes](/help/get-started/using.md) principales.

## Capacidades técnicas {#technical-capabilities}

La siguiente tabla ofrece una visión general de las diferencias entre los componentes principales y los componentes básicos.

Para obtener más información sobre sus capacidades de creación y las opciones para preconfigurarlas, [consulte la página de creación sobre ellas](/help/get-started/authoring.md).

| **Capacidad** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementación lógica | JPOs de Java con anotaciones [de modelos](https://sling.apache.org/documentation/bundles/models.html) Sling | Código JSP |
| Definición de marca | [Sintaxis del lenguaje](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) de plantilla HTML (HTL) | Código JSP |
| Saneamiento XSS | Automatizado por HTL | Principalmente manual |
| Nombres de clases CSS | Convenciones de nombres estandarizadas basadas en la notación del modificador [de elementos de](https://getbem.com/) bloque (BEM) (a partir de la versión 2.0.0) | Esquemas personalizados |
| Definición de cuadro de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU clásica |
| Salida JSON | [Modelos Sling Exporter con serialización Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling predeterminado |
| Versiones | [Para el modelo y el HTL](guidelines.md) | Ninguna |
| Pruebas | Pruebas de unidad + Pruebas de integración | Pruebas de integración |
| Entrega | [Vía GitHub público](https://github.com/adobe/aem-core-wcm-components) | Vía Quickstart |
| Licencia | [Licencia de Apache](https://www.apache.org/licenses/LICENSE-2.0) | Adobe, propiedad privada |
| Contribución | Mediante solicitud de extracción | No es posible |
| Accesibilidad | Compatible con el estándar []WCAG 2.0 AA(https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) | Compatible solo parcialmente con el estándar [WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Lista de componentes {#component-list}

La siguiente tabla enumera los componentes principales disponibles, vinculándolos a su API, e indica qué componentes de base reemplazan.

| Componente principal | Descripción | Componente(s) base(s) sustituido(s) |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2) | Página adaptable que trabaja con el editor de plantillas | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Ruta de navegación](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navegación por la jerarquía de páginas | `/libs/foundation/components/breadcrumb` |
| [Título](https://adobe.com/go/aem_cmp_tech_title_v2) | Título H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texto enriquecido | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagen](https://adobe.com/go/aem_cmp_tech_image_v2) | Carga inteligente y diferida del tamaño de representación óptimo | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://adobe.com/go/aem_cmp_tech_list_v2) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartir en redes sociales](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget de uso compartido de Facebook y Pinterest | `-` |
| [Contenedor del formulario](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Sistema de párrafos de formularios interactivos | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto de formulario](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opciones de formulario](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Campo de entrada de varias opciones | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulario oculto](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botón de formulario](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Botón Enviar o personalizado | `/libs/foundation/components/form/submit` |
| [Navegación](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Un componente de navegación del sitio que enumera la jerarquía de páginas anidada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegación por idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Cambiador de idioma y país que enumera la estructura de idioma global | `-` |
| [Búsqueda rápida](https://adobe.com/go/aem_cmp_tech_search_v1) | Componente de búsqueda que muestra los resultados como sugerencias in situ en un menú desplegable | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincularlo a contenido u otras acciones | `-` |
| [Pestañas](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Permite al autor del contenido organizar el contenido de la página en varias fichas | `-` |
| [Carrusel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Permite al autor del contenido organizar el contenido en un carrusel de diapositivas rotatorio | `/libs/foundation/components/carousel` |
| [Fragmento de contenido](https://adobe.com/go/aem_cmp_tech_cf_v1) | Permite la visualización de un fragmento de contenido | `-` |
| [Lista de fragmentos de contenido](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Permite mostrar una lista de fragmentos de contenido | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1) | Separa el contenido de una página | `-` |
| [Acordeón](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organizar paneles de contenido en un acordeón contraíble | `-` |
| [Contenedor](https://adobe.com/go/aem_cmp_tech_container_v1) | Organización de componentes dentro de un contenedor | `-` |
| [Botón](https://adobe.com/go/aem_cmp_tech_button_v1) | Creación de un botón en una página | `-` |
| [Descargar](https://adobe.com/go/aem_cmp_tech_download_v1) | Agregar un recurso descargable a una página | `-` |
| [Fragmento de experiencias](https://adobe.com/go/aem_cmp_tech_xf_v1) | Adición de un fragmento de experiencia a una página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incrustar](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incrustar un recurso externo dentro de una página | - |

### Próximos componentes {#upcoming-components}

Para obtener una visión general de la próxima hoja de ruta del componente principal, consulte la wiki del [proyecto en GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Actualización de los componentes principales {#upgrade-of-core-components}

Una ventaja de los componentes con versiones es que permite separar la migración a una nueva versión de AEM de la migración a las nuevas versiones de componentes. Además, si hay nuevas versiones de componentes disponibles, permite la migración individual de cada componente a la nueva versión.

Las migraciones a una nueva versión de AEM no afectarán al funcionamiento de los componentes principales, siempre que sus versiones también admitan la nueva versión de AEM a la que se está migrando. Las personalizaciones realizadas en los componentes principales tampoco deben verse afectadas, siempre que no utilicen API que hayan sido [obsoletas o eliminadas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Las migraciones a nuevas versiones de los componentes principales tampoco afectarán al funcionamiento del componente, pero es posible que se introduzcan nuevas funciones a los autores de páginas, lo que puede requerir cierta configuración por parte de un editor de plantillas, en caso de que no se desee el comportamiento predeterminado. Sin embargo, es posible que sea necesario adaptar las personalizaciones para obtener más información, consulte la página [Personalización de componentes](customizing.md#upgrade-compatibility-of-customizations) principales.

## When to Use the Core Components? {#when-to-use-the-core-components}

Como los componentes principales son completamente nuevos y ofrecen varios beneficios, se recomienda utilizarlos en los nuevos proyectos de AEM. En los proyectos existentes, la migración debería ser parte de un esfuerzo de proyecto aún mayor; por ejemplo, para realizar un cambio en la marca o la refactorización total.

Por lo tanto, Adobe proporciona las siguientes recomendaciones:

* **Nuevos proyectos** Los nuevos proyectos siempre deben intentar utilizar los componentes principales. Si los componentes principales no se pueden utilizar directamente o [ampliar](customizing.md) para satisfacer los requisitos del proyecto, cree un componente personalizado siguiendo la arquitectura de componentes establecida en los componentes principales. Salvo en los casos en que no sea posible, evite utilizar los componentes [de](#foundation-component-support)base.
* **La recomendación de proyectos** existentes se mantiene usando los componentes [de](#foundation-component-support)base, a menos que se planifique una refactorización de sitios o componentes.\
   Dado que la mayoría de los proyectos existentes los utilizan muy ampliamente, [seguirán contando con el apoyo de los componentes básicos.](#foundation-component-support)
* **Nuevos componentes** personalizadosSe evalúa si un componente [principal existente puede personalizarse](customizing.md).\
   Si no es así, se recomienda crear un nuevo componente personalizado siguiendo las directrices [de](guidelines.md)componentes.
* **Componentes** personalizados existentes Si los componentes funcionan correctamente, manténgalos tal como están.\
   Si no es así, consulte &quot;Nuevos componentes personalizados&quot; más arriba.

## Migración a los componentes principales

Cualquier nuevo proyecto debe implementarse con los componentes principales. Sin embargo, los proyectos existentes normalmente tendrán una amplia implementación de los componentes de base.

Un esfuerzo mayor en un proyecto existente (por ejemplo, un rediseño de marca o una refactorización general) a menudo ofrece la posibilidad de migrar a los componentes principales. Para facilitar esta migración, Adobe ha proporcionado una serie de herramientas de migración para fomentar la adopción de los componentes principales y la tecnología AEM más reciente.

[Las herramientas](http://opensource.adobe.com/aem-modernize-tools/) de modernización de AEM facilitan la conversión de:

* Plantillas estáticas a plantillas editables
* Diseñar configuraciones para políticas
* Componentes básicos a componentes principales
* IU clásica a IU táctil

Para obtener más información sobre el uso de estas herramientas, [consulte su documentación](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Las herramientas de moderación de AEM son un esfuerzo de la comunidad y Adobe no las admite ni garantiza.

## Compatibilidad con componentes principales {#core-component-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que otras funciones de productos de AEM, la regla general es: Los componentes se anuncian primero como obsoletos y los primeros se eliminan en la siguiente versión de AEM. Esto proporciona a los clientes al menos un ciclo de lanzamiento para pasar a la nueva versión del componente, antes de dejar de ofrecer soporte.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más información sobre la compatibilidad con las personalizaciones de componentes, consulte la página [Personalización de componentes](customizing.md) principales.

## Compatibilidad con componentes de base {#foundation-component-support}

Dado que los componentes de base han servido de base para tanto desarrollo de proyectos en muchas versiones de AEM, seguirán recibiendo apoyo en el futuro previsible.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

**Consulte lo siguiente:**

* [Uso de componentes](/help/get-started/using.md) principales: obtenga y ejecute los componentes principales en su propio proyecto.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.