---
title: Desarrollo de componentes principales
description: Los componentes principales proporcionan componentes básicos sólidos y ampliables que ofrecen funciones enriquecidas, envío continuo, versiones de componentes, implementación moderna, marcado ligero y exportación de contenido JSON.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '1583'
ht-degree: 100%

---

# Desarrollo de componentes principales {#developing-core-components}

## ¿Cuándo utilizar los componentes principales? {#when-to-use-the-core-components}

Como los componentes principales son completamente nuevos y ofrecen varios beneficios, se recomienda utilizarlos en los nuevos proyectos de AEM. En los proyectos existentes, la migración debería ser parte de un esfuerzo de proyecto aún mayor; por ejemplo, para realizar un cambio en la marca o la refactorización total.

Por lo tanto, Adobe ofrece las siguientes recomendaciones:

* **Proyectos nuevos**
Los proyectos nuevos siempre deben intentar utilizar los componentes principales. Si los componentes principales no se pueden utilizar directamente o [ampliados](customizing.md) para satisfacer los requisitos del proyecto, cree un componente personalizado siguiendo la arquitectura de componentes establecida en los componentes principales. Salvo que no sea posible, evite utilizar los [componentes de base](/help/versions.md#foundation-component-support).
* **Proyectos existentes**
Se recomienda que los proyectos existentes sigan usando los [componentes base](/help/versions.md#foundation-component-support), a menos que se planifique una refactorización de sitios o componentes.\
   Como la mayoría de los proyectos existentes los utilizan muy ampliamente, los componentes de base [seguirán siendo compatibles.](/help/versions.md#foundation-component-support)
* **Nuevos componentes personalizados**
Evaluar si un [componente principal existente se puede personalizar](customizing.md).\
   Si no es así, se recomienda crear un componente personalizado nuevo siguiendo las [Directrices de componentes](guidelines.md).
* **Componentes personalizados existentes**
Si los componentes funcionan según lo esperado, manténgalos tal cual.
\
   Si no es así, consulte &quot;Nuevos componentes personalizados&quot; más arriba.

## Cómo utilizar correctamente los componentes principales {#how-to-succeed}

Los componentes principales son completos, flexibles y fáciles de usar y personalizar. [Seguir algunas directrices clave](success.md) garantizará que el proyecto con los componentes principales sea un éxito.

## Migración hacia los componentes principales

Cualquier nuevo proyecto debe implementarse con los componentes principales. Sin embargo, los proyectos existentes normalmente tendrán amplias implementaciones de los componentes de base.

### Migración desde componentes de base {#from-foundation}

Un esfuerzo mayor en un proyecto existente (por ejemplo, un cambio de marca o una refactorización general) a menudo ofrece la oportunidad de migrar a los componentes principales. Para facilitar esta migración, Adobe ofrece una serie de herramientas de migración que fomentan la adopción de los componentes principales y de la tecnología de AEM más reciente.

[Las herramientas de modernización de AEM](http://opensource.adobe.com/aem-modernize-tools/) facilitan la conversión de lo siguiente:

* Plantillas estáticas a plantillas editables.
* Diseño de las configuraciones para directivas.
* Componentes básicos a principales.
* De IU clásica a IU táctil.

Para obtener más información sobre el uso de estas herramientas, [consulte su documentación](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>Las herramientas de modernización de AEM son un esfuerzo de la comunidad y Adobe no las admite ni las garantiza.

## Migración mediante Cambiar a AEM Cloud Service {#via-aemaacs}

Como AEM Cloud Service viene con la última versión de los componentes principales automáticamente, cuando se desplaza de una instalación de AEM en línea, deberá eliminar cualquier dependencia de los componentes principales del archivo de proyectos `pom.xml`.

Los componentes proxy seguirán funcionando como antes porque los proxies apuntan al supertipo necesario y la ruta del supertipo tiene la versión en él. De este modo, la simple eliminación de la dependencia permite que los componentes principales funcionen en AEMaaCS del mismo modo que lo hicieron en línea.

Al igual que cualquier otro proyecto de AEMaaCS, también deberá añadir una dependencia al jar del SDK de AEM. Esto no es específico de los componentes principales, pero es obligatorio.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Consulte el documento [Estructura del proyecto de AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es) para obtener más información sobre los proyectos de AEMaaCS.

## Compatibilidad con los componentes principales {#core-component-support}

Los componentes principales son parte integral de AEM y se admiten tal cual bajo los mismos términos y condiciones en los que se admitirían si fueran parte del inicio rápido.

Al igual que otras características de los productos de AEM, la regla general es que los componentes se anuncien primero como obsoletos y los primeros se eliminen en la siguiente versión de AEM. Esto proporciona a los clientes al menos un ciclo de lanzamiento para poder cambiarse a la nueva versión del componente antes de que finalice el servicio de soporte.

La versión de cada componente señala claramente las versiones de AEM que admite. Cuando una versión de AEM deja de ser compatible, también lo deja de ser el componente principal de esa versión de AEM.

Para obtener más detalles sobre la compatibilidad de la personalización de componentes, consulte la página [Personalizar componentes principales](customizing.md).


## Capacidades técnicas {#technical-capabilities}

En la siguiente tabla se ofrece una descripción general de las diferencias entre los componentes principales y los de base.

Para obtener más información sobre sus capacidades de creación y las opciones para preconfigurarlas, [consulte la página de creación sobre ellas](/help/get-started/authoring.md).

| **Capacidad** | **Componente principal** | **Componente Base** |
|-----|---|---|
| Implementación lógica | POJO de Java con anotaciones de [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) | Código JSP |
| Definición de marca | [Lenguaje de la plantilla HTML](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=es) sintaxis (HTL) | Código JSP |
| Saneamiento XSS | Automatizado por HTL | Principalmente manual |
| Asignación de nombres a clases CSS | Convenciones de nomenclatura estandarizadas basadas en la notación [Modificador de elementos de bloque](https://getbem.com/) (BEM) (a partir de la versión 2.0.0) | Esquemas personalizados |
| Cuadro de diálogo de definición | [Coral 3](https://helpx.adobe.com/es/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU clásica |
| Salida JSON | [Exportador de modelos Sling con serialización Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling predeterminado |
| Versiones | [Para el modelo y el HTL](guidelines.md) | Ninguna |
| Pruebas | Pruebas de unidad + pruebas de integración | Pruebas de integración |
| Entrega | [A través de GitHub público](https://github.com/adobe/aem-core-wcm-components) | Mediante Quickstart |
| Licencia | [Licencia de Apache](https://www.apache.org/licenses/LICENSE-2.0) | Propietario de Adobe |
| Contribución | Mediante solicitud de extracción | No es posible |
| Accesibilidad | Totalmente compatible con el [WCAG 2.0 AA estándar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=es) | Sólo parcialmente compatible con el [WCAG 2.0 AA estándar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=es) |

## Lista de componentes {#component-list}

En la siguiente tabla se enumeran los componentes principales disponibles, enlazándolos a su API, e indican los componentes de base a los que reemplazan.

| Componente principal | Descripción | Componentes de base reemplazados |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2_es) | Página adaptable que trabaja con el editor de plantillas | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Ruta de navegación](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_es) | Navegación por las jerarquías de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://adobe.com/go/aem_cmp_tech_title_v2_es) | Título H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texto enriquecido | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagen](https://adobe.com/go/aem_cmp_tech_image_v2_es) | Carga inteligente y lenta de un tamaño de representación óptimo | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://adobe.com/go/aem_cmp_tech_list_v2_es) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartir en redes sociales](https://adobe.com/go/aem_cmp_tech_sharing_v1_es) | Widget para compartir en Facebook y Pinterest | `-` |
| [Contenedor del formulario](https://adobe.com/go/aem_cmp_tech_form_container_v2_es) | Sistema de párrafos de formulario adaptable | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto de formulario](https://adobe.com/go/aem_cmp_tech_form_text_v2_es) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opciones de formulario](https://adobe.com/go/aem_cmp_tech_form_options_v2_es) | Campo de entrada de varias opciones | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulario oculto](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_es) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botón de formulario](https://adobe.com/go/aem_cmp_tech_form_button_v2_es) | Botón Enviar o personalizado | `/libs/foundation/components/form/submit` |
| [Navegación](https://adobe.com/go/aem_cmp_tech_navigation_v1_es) | Componente de navegación del sitio que enumera la jerarquía de páginas anidada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegación por idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1_es) | Alternador de idioma y país que enumera la estructura de idioma global | `-` |
| [Búsqueda rápida](https://adobe.com/go/aem_cmp_tech_search_v1_es) | Componente de búsqueda que muestra los resultados como sugerencias in situ en un menú desplegable | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1_es) | Permite al autor del contenido crear fácilmente un teaser para añadir contenido mediante una imagen, un título o un texto enriquecido y vincular con otro contenido u otras acciones | `-` |
| [Pestañas](https://adobe.com/go/aem_cmp_tech_tabs_v1_es) | Permite al autor del contenido organizar el contenido de la página en varias pestañas | `-` |
| [Carrusel](https://adobe.com/go/aem_cmp_tech_carousel_v1_es) | Permite al autor de contenido organizar el contenido en un carrusel giratorio de diapositivas | `/libs/foundation/components/carousel` |
| [Fragmento de contenido](https://adobe.com/go/aem_cmp_tech_cf_v1_es) | Permite la visualización de un fragmento del contenido | `-` |
| [Lista de fragmentos de contenido](https://adobe.com/go/aem_cmp_tech_cflist_v1_es) | Permite mostrar una lista de fragmentos de contenido | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1_es) | Separa el contenido de una página | `-` |
| [Acordeón](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organiza paneles de contenido en un acordeón plegable | `-` |
| [Contenedor](https://adobe.com/go/aem_cmp_tech_container_v1_es) | Organización de componentes dentro de un contenedor | `-` |
| [Botón](https://adobe.com/go/aem_cmp_tech_button_v1) | Creación de un botón en una página | `-` |
| [Descargar](https://adobe.com/go/aem_cmp_tech_download_v1) | Agregar un recurso descargable a una página | `-` |
| [Fragmento de experiencias](https://adobe.com/go/aem_cmp_tech_xf_v1) | Añadir un fragmento de experiencia a una página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incrustar](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incrustar un recurso externo en una página | - |
| [Barra de progreso](https://adobe.com/go/aem_cmp_tech_progress_v1) | Proporcionar una representación visual del progreso hacia un objetivo | - |
| [Visualizador de PDF](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_es) | Presenta un documento PDF en una página | - |

### Próximos componentes {#upcoming-components}

Para obtener una descripción general de la próxima hoja de ruta del componente principal, consulte la [wiki del proyecto en GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Actualización de los componentes principales {#upgrade-of-core-components}

Una ventaja de los componentes con versiones es que permite separar la migración a una nueva versión de AEM de la migración a las nuevas versiones de los componentes. Además, si hay versiones de componentes nuevas disponibles, permite la migración individual de cada componente a la nueva versión.

Las migraciones a una nueva versión de AEM no afectarán al funcionamiento de los componentes principales, siempre que sus versiones también admitan la nueva versión de AEM a la que se va a migrar. Las personalizaciones realizadas en los componentes principales tampoco deben verse afectadas, siempre que no utilicen API [obsoletas o eliminadas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=es).

Las migraciones a nuevas versiones de los componentes principales tampoco afectarán al funcionamiento del componente, pero podrían introducirse nuevas funciones a los autores de páginas, que podrían requerir cierta configuración por parte de un editor de plantillas, en caso de que no se desee el comportamiento predeterminado. Sin embargo, es posible que haya que adaptar las personalizaciones; para obtener más información, consulte la página [Personalización de componentes principales](customizing.md#upgrade-compatibility-of-customizations).
