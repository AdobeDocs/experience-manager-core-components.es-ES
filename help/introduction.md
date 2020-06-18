---
title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas. '
translation-type: tm+mt
source-git-commit: bbbd918c7caf508866ae6dadbb8c815dca4e900b
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 29%

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas se simplifica pero mantiene su potencia para el autor; asimismo, el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales son un conjunto de componentes de Gestor de contenido web (WCM) estandarizados para AEM a fin de acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de los sitios web.

## Medios {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library)**Recopilación de ejemplos para la vista de los componentes en sus distintas configuraciones.
* **Documentación de componentes (este documento):** Para desarrolladores y autores, con detalles sobre cada componente.
* **[Repositorio de GitHub de componentes principales:](https://github.com/adobe/aem-core-wcm-components)**Para obtener detalles de desarrollador de cada componente y descarga de proyecto.
* Introducción:
   * **[Éxito con los componentes principales:](/help/developing/success.md)**Directrices para considerar mucho antes del inicio de cualquier proyecto que vaya a utilizar los componentes principales.
   * **[Tutorial de WKND:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Un tutorial de dos días para crear un nuevo sitio.
   * **[Tutorial de la Cumbre:](https://expleague.azureedge.net/labs/L767/index.html)**Un tutorial de dos horas para construir un nuevo sitio (de un laboratorio en la Cumbre de Estados Unidos 2019).
   * **[Seminario web de Gems:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)**Visita guiada de los componentes principales (grabada en diciembre de 2018).

## Características {#features}

|  |  |
|---|---|
| Listo para la producción | Los componentes principales son 28 componentes robustos que están bien probados, se utilizan ampliamente y que funcionan bien. |
| Preparado para la nube | Ya sea en [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), en [Adobes Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)o in situ, solo funcionan. |
| Versátil | Los componentes representan conceptos genéricos con los que los autores pueden ensamblar casi cualquier diseño. |
| Configurable | Las directivas [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) contenido de nivel de plantilla definen qué funciones pueden utilizar o no los autores de la página. |
| Trackable | La integración [de la capa de datos del cliente de](/help/developing/data-layer/overview.md) Adobe permite el seguimiento de todos los aspectos de la experiencia de visitante. |
| Accesible | They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+access+in%3Atítulo)). |
| Compatible con SEO | The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations. |
| Listo para WebApp | La salida [JSON](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) optimizada permite el procesamiento en el lado del cliente, con la posibilidad de editar [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)en contexto. |
| Kit de diseño | Un kit de [interfaz de usuario para Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) permite a los diseñadores crear esquemas que, a continuación, pueden [aplicar estilo según sea necesario](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| Themeable | The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/). |
| Personalizable | Varios patrones permiten una personalización [](developing/customizing.md)sencilla, desde ajustar el HTML hasta una reutilización avanzada de la funcionalidad. |
| Versiones | La directiva [de](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) versiones garantiza que los componentes principales no interrumpan el sitio al mejorar las cosas que puedan afectarle. |
| Localizable | Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md). |
| Abrir fuente | Si algo no es como debería, [contribuya con sus mejoras!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

## Los componentes {#the-components}

La versión actual de los componentes principales contiene los siguientes componentes.

### Componentes de plantilla {#template-components}

* [Página](components/page.md)
* [Navegación](components/navigation.md)
* [Navegación por idiomas](components/language-navigation.md)
* [Ruta de navegación](components/breadcrumb.md)
* [Búsqueda rápida](components/quick-search.md)

### Componentes de creación de páginas {#page-authoring-components}

* [Título](components/title.md)
* [Texto](components/text.md)
* [Imagen](components/image.md)
* [Botón](components/button.md)
* [Teaser](components/teaser.md)
* [Descargar](components/download.md)
* [Lista](components/list.md)
* [Fragmento de experiencias](components/experience-fragment.md)
* [Fragmento de contenido](components/content-fragment-component.md)
* [Lista de fragmentos de contenido](components/content-fragment-list.md)
* [Incrustar](components/embed.md)
* [Compartir en redes sociales](components/sharing.md)
* [Separador](components/separator.md)
* [Barra de progreso](components/progress-bar.md)
* [Visor de PDF](components/pdf-viewer.md)

### Componentes de Contenedor {#container-components}

* [Contenedor](components/container.md)
* [Carrusel](components/carousel.md)
* [Pestañas](components/tabs.md)
* [Acordeón](components/accordion.md)

### Componentes de formulario{#form-components}

* [Contenedor del formulario](components/forms/form-container.md)
* [Texto de formulario](components/forms/form-text.md)
* [Opciones de formulario](components/forms/form-options.md)
* [Formulario oculto](components/forms/form-hidden.md)
* [Botón de formulario](components/forms/form-button.md)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Puede que algunas versiones de los componentes principales individuales solo sean compatibles con algunas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada a la lista anterior) para obtener información sobre la compatibilidad de componentes específicos o consulte el documento [Versiones de componentes principales](versions.md) para obtener más información.

## Requisitos del sistema {#system-requirements}

| Componentes principales | AEM as a Cloud Service | AEM 6.5 | AEM 6.4   | Java SE | Maven |
---------|---------|---------|---------|---------|---------
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Continua | 6.5.0.0+ | 6.4.4.0+ | 8, 11 | 3.3.9+ |

Para conocer los requisitos de versiones anteriores de componentes principales, consulte Versiones [de componentes](versions.md)principales.

Los componentes principales requieren el uso de plantillas [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) editables y no admiten la IU clásica ni plantillas estáticas. Si es necesario, consulte las Herramientas [de modernización de](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) AEM para actualizar su proyecto con estas funciones modernas de AEM.

Para configurar el entorno de desarrollo local, consulte [esta descripción general de AEM como SDK](https://docs.adobe.com/content/help/es-ES/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) Cloud Service o este documento [para versiones anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
