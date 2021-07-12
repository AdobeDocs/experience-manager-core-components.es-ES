---
title: Desarrollo de componentes principales
description: Los componentes principales proporcionan componentes básicos sólidos y ampliables que ofrecen funciones enriquecidas, envío continuo, versiones de componentes, implementación moderna, marcado ligero y exportación de contenido JSON.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 14%

---

# Desarrollo de componentes principales {#developing-core-components}

## ¿Cuándo se deben utilizar los componentes principales? {#when-to-use-the-core-components}

Como los componentes principales son completamente nuevos y ofrecen varios beneficios, se recomienda utilizarlos en los nuevos proyectos de AEM. En los proyectos existentes, la migración debería ser parte de un esfuerzo de proyecto aún mayor; por ejemplo, para realizar un cambio en la marca o la refactorización total.

Por lo tanto, Adobe ofrece las siguientes recomendaciones:

* **Nuevos**
proyectosLos nuevos proyectos siempre deben intentar utilizar los componentes principales. Si los componentes principales no se pueden utilizar directamente o [ampliados](customizing.md) para satisfacer los requisitos del proyecto, cree un componente personalizado siguiendo la arquitectura de componentes establecida en los componentes principales. Salvo que no sea posible, evite utilizar los [componentes de base](/help/versions.md#foundation-component-support).
* **La recomendación**
Proyectos existentes se mantiene usando los componentes  [base](/help/versions.md#foundation-component-support), a menos que se planifique una refactorización de sitios o componentes.\
   Como la mayoría de los proyectos existentes los utilizan muy ampliamente, los componentes de base [seguirán siendo compatibles.](/help/versions.md#foundation-component-support)
* **Nuevos**
componentes personalizadosEvalúe si un componente  [principal existente se puede personalizar](customizing.md).\
   Si no es así, se recomienda crear un nuevo componente personalizado siguiendo las [Directrices de componentes](guidelines.md).
* **Componentes personalizados existentes**
Si los componentes funcionan según lo esperado, manténgalos tal cual.
\
   Si no es así, consulte &quot;Nuevos componentes personalizados&quot; más arriba.

## Cómo realizar correctamente con los componentes principales {#how-to-succeed}

Los componentes principales son potentes, flexibles y fáciles de usar y personalizar. [Seguir algunas ](success.md) directrices clave garantizará que el proyecto con los componentes principales sea un éxito.

## Migración a los componentes principales

Cualquier nuevo proyecto debe implementarse con los componentes principales. Sin embargo, los proyectos existentes normalmente tendrán amplias implementaciones de los componentes de base.

### Migración desde componentes de base {#from-foundation}

Un esfuerzo mayor en un proyecto existente (por ejemplo, un cambio de marca o una refactorización general) a menudo ofrece la oportunidad de migrar a los componentes principales. Para facilitar esta migración, el Adobe ha proporcionado una serie de herramientas de migración que fomentan la adopción de los componentes principales y de la tecnología de AEM más reciente.

[Las AEM ](http://opensource.adobe.com/aem-modernize-tools/) herramientas de modernización permiten la conversión sencilla de:

* Plantillas estáticas a plantillas editables.
* Diseño de las configuraciones para políticas.
* Componentes básicos a principales.
* De IU clásica a IU táctil.

Para obtener más información sobre el uso de estas herramientas, [consulte su documentación](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Las AEM Herramientas de modernización son un esfuerzo de la comunidad y no son compatibles ni están garantizadas por el Adobe.

## Migración mediante Mover a AEM como Cloud Service {#via-aemaacs}

Como AEM como Cloud Service viene con la última versión de los componentes principales automáticamente, cuando se desplaza de una instalación de AEM local, deberá eliminar cualquier dependencia de los componentes principales del archivo `pom.xml` de proyectos.

Los componentes proxy seguirán funcionando como antes porque   los proxies apuntan al supertipo necesario y la ruta de supertipo tiene la versión en él. De este modo, la simple eliminación de la dependencia permite que los componentes principales funcionen en AEMaaCS del mismo modo que lo hicieron en las instalaciones.

Al igual que cualquier otro proyecto de AEMaaCS, también deberá añadir una dependencia al jar del SDK de AEM. Esto no es específico de los componentes principales, pero es obligatorio.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Consulte el documento [AEM Estructura del proyecto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para obtener más información sobre los proyectos de AEMaaCS.

## Compatibilidad con los componentes principales {#core-component-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que otras funciones AEM producto, la regla general es: Los componentes se anuncian primero como obsoletos y los primeros se eliminan en la siguiente versión de AEM. Esto proporciona a los clientes al menos un ciclo de versiones para pasar a la nueva versión del componente antes de dejar de ofrecer asistencia.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más información sobre la compatibilidad de la personalización de componentes, consulte la página [Personalización de componentes principales](customizing.md).


## Capacidades técnicas {#technical-capabilities}

En la tabla siguiente se ofrece una descripción general de las diferencias entre los componentes principales y los componentes básicos.

Para obtener más información sobre sus capacidades de creación y las opciones para preconfigurarlas, [consulte la página de creación sobre ellas](/help/get-started/authoring.md).

| **Capacidad** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementación lógica | POJO de Java con anotaciones de [Modelos de Sling](https://sling.apache.org/documentation/bundles/models.html) | Código JSP |
| Definición de marca | [Sintaxis del lenguaje de plantilla HTML](https://docs.adobe.com/content/help/es-ES/experience-manager-htl/using/overview.html)  (HTL) | Código JSP |
| Saneamiento XSS | Automatizado por HTL | Principalmente manual |
| Asignación de nombres a clases CSS | Convenciones de nomenclatura estandarizadas basadas en la notación [Modificador de elementos de bloque](https://getbem.com/) (BEM) (a partir de la versión 2.0.0) | Esquemas personalizados |
| Definición del cuadro de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU clásica |
| Salida JSON | [Exportador de modelos Sling con serialización Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling predeterminado |
| Versiones | [Para el modelo y HTL](guidelines.md) | Ninguna |
| Pruebas | Pruebas de unidad + pruebas de integración | Pruebas de integración |
| Entrega | [A través de GitHub público](https://github.com/adobe/aem-core-wcm-components) | Mediante Quickstart |
| Licencia | [Licencia de Apache](https://www.apache.org/licenses/LICENSE-2.0) | Adobe propietario |
| Contribución | Mediante solicitud de extracción | No es posible |
| Accesibilidad | Compatible con el [WCAG 2.0 AA estándar](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) | Sólo parcialmente compatible con el [WCAG 2.0 AA estándar](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Lista de componentes {#component-list}

En la tabla siguiente se enumeran los componentes principales disponibles, enlazándolos a su API, e indican los componentes de base que reemplazan.

| Componente principal | Descripción | Componentes de base reemplazados |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2) | Página adaptable que trabaja con el editor de plantillas | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Ruta de navegación](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navegación por jerarquías de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://adobe.com/go/aem_cmp_tech_title_v2) | Título H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texto enriquecido | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagen](https://adobe.com/go/aem_cmp_tech_image_v2) | Carga inteligente y lenta de un tamaño de representación óptimo | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://adobe.com/go/aem_cmp_tech_list_v2) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartir en redes sociales](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget para compartir facebook y Pinterest | `-` |
| [Contenedor del formulario](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Sistema de párrafos de formulario adaptable | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto de formulario](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opciones de formulario](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Campo de entrada de varias opciones | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulario oculto](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botón de formulario](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Botón Enviar o personalizado | `/libs/foundation/components/form/submit` |
| [Navegación](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Componente de navegación del sitio que enumera la jerarquía de páginas anidada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegación por idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Alternador de idioma y país que enumera la estructura de idioma global | `-` |
| [Búsqueda rápida](https://adobe.com/go/aem_cmp_tech_search_v1) | Componente de búsqueda que muestra los resultados como sugerencias in situ en un menú desplegable | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o texto enriquecido y vincular con otro contenido u otras acciones | `-` |
| [Pestañas](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Permite al autor del contenido organizar el contenido de la página en varias pestañas | `-` |
| [Carrusel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Permite al autor de contenido organizar el contenido en un carrusel giratorio de diapositivas | `/libs/foundation/components/carousel` |
| [Fragmento de contenido](https://adobe.com/go/aem_cmp_tech_cf_v1) | Permite la visualización de un fragmento de contenido | `-` |
| [Lista de fragmentos de contenido](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Permite mostrar una lista de fragmentos de contenido | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1) | Separa el contenido de una página | `-` |
| [Acordeón](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organizar paneles de contenido en un acordeón contraíble | `-` |
| [Contenedor](https://adobe.com/go/aem_cmp_tech_container_v1) | Organización de componentes dentro de un contenedor | `-` |
| [Botón](https://adobe.com/go/aem_cmp_tech_button_v1) | Creación de un botón en una página | `-` |
| [Descargar](https://adobe.com/go/aem_cmp_tech_download_v1) | Agregar un recurso descargable a una página | `-` |
| [Fragmento de experiencias](https://adobe.com/go/aem_cmp_tech_xf_v1) | Añadir un fragmento de experiencia a una página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incrustar](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incrustar un recurso externo en una página | - |
| [Barra de progreso](https://adobe.com/go/aem_cmp_tech_progress_v1) | Proporcionar una representación visual del progreso hacia un objetivo | - |
| [Visualizador de PDF](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Presenta un documento PDF en una página | - |

### Próximos componentes {#upcoming-components}

Para obtener una descripción general de la próxima hoja de ruta del componente principal, consulte la [wiki del proyecto en GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Actualización de componentes principales {#upgrade-of-core-components}

Una ventaja de los componentes con versiones es que permite separar la migración a una nueva versión AEM de la migración a las nuevas versiones de los componentes. Además, si hay nuevas versiones de componentes disponibles, permite la migración individual de cada componente a la nueva versión.

Las migraciones a una nueva versión de AEM no afectarán al funcionamiento de los componentes principales, siempre que sus versiones también admitan la nueva versión de AEM a la que se va a migrar. Las personalizaciones realizadas en los componentes principales tampoco deben verse afectadas, siempre que no utilicen API que hayan sido [obsoletas o eliminadas](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Las migraciones a nuevas versiones de los componentes principales tampoco afectarán al funcionamiento del componente, pero podrían introducirse nuevas funciones a los autores de páginas, que podrían requerir cierta configuración por parte de un editor de plantillas, en caso de que no se desee el comportamiento predeterminado. Sin embargo, es posible que haya que adaptar las personalizaciones; para obtener más información, consulte la página [Personalización de componentes principales](customizing.md#upgrade-compatibility-of-customizations) .
