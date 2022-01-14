---
title: Introducción a los componentes principales
description: 'Los componentes principales se introdujeron para proporcionar componentes básicos sólidos y ampliables, basados en las últimas tecnologías y prácticas recomendadas. '
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: ef18f65be72295f7886a132a26bdd4f8bc2fbd50
workflow-type: ht
source-wordcount: '917'
ht-degree: 100%

---

# Introducción a los componentes principales {#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas se simplifica pero mantiene su potencia para el autor; asimismo, el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales son un conjunto de componentes estandarizados de Administración de contenido web (WCM) para AEM a fin de acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de los sitios web.

## Medios {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library_es)** una colección de ejemplos para ver los componentes en sus distintas configuraciones.
* **Documentación de componentes (este documento):** para desarrolladores y autores, con detalles sobre cada componente.
* **[Repositorio de componentes principales de GitHub: ](https://github.com/adobe/aem-core-wcm-components)** para obtener detalles del desarrollador de cada componente y descarga de proyecto.
* Introducción:
   * **[Éxito con los componentes principales:](/help/developing/success.md)** instrucciones que se deben tener en cuenta mucho antes del inicio de cualquier proyecto que vaya a utilizar los componentes principales.
   * **[Tutorial de WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es)** tutorial de dos días para crear un nuevo sitio.
   * **[Tutorial Summit:](https://expleague.azureedge.net/labs/L767/index.html)** un tutorial de dos horas para construir un nuevo sitio (de un laboratorio en la US Summit 2019).
   * **[Seminario web de Gems:](https://helpx.adobe.com/es/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** visita guiada por los componentes principales (grabada en diciembre de 2018).

## Características {#features}

|  |  |
|---|---|
| Listo para la producción | Los componentes principales son 28 componentes sólidos que se han probado, utilizado ampliamente y que funcionan bien. |
| Preparado para la nube | Ya sea en [AEM como Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es), en [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o en línea, simplemente funcionan. |
| Versátil | Los componentes representan conceptos genéricos con los que los autores pueden ensamblar casi cualquier diseño. |
| Configurable | Las [directivas de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) a nivel de plantilla definen qué características pueden utilizar o no los autores de la página. |
| Rastreable | La [integración de capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md) permite el seguimiento de todos los aspectos de la experiencia del visitante. |
| Accesible | Cumplen el estándar [WCAG 2.1](https://www.w3.org/TR/WCAG21/), proporcionan etiquetas de tipo ARIA y admiten la navegación con teclado ([problemas conocidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| Compatible con SEO | La salida de HTML es semántica y proporciona anotaciones de microdatos de tipo [schema.org](https://schema.org). |
| Preparado para la aplicación web | La [salida JSON optimizada](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html?lang=es) permite el procesamiento en el lado del cliente, con la posibilidad de [editar en contexto](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es). |
| Compatibilidad con AMP | Los componentes tienen [compatibilidad integrada con el estándar AMP,](/help/developing/amp.md) lo que acelera las experiencias móviles. |
| Kit de diseño | Un [kit de interfaz de usuario para Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) permite a los diseñadores crear mallas metálicas que luego pueden [dar forma según sea necesario](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Configurable | Los componentes implementan el [Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/components-templates/style-system.html) y el marcado sigue la [nomenclatura de BEM CSS](http://getbem.com/). |
| Personalizable | Varios patrones permiten [una fácil personalización](developing/customizing.md), desde ajustar el HTML a una reutilización avanzada de la funcionalidad. |
| Versiones | La [directiva de versiones](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiza que los componentes principales no romperán el sitio al mejorar las cosas que puedan afectarle. |
| Localizable | La resolución de referencia inteligente permite a ciertos componentes buscar y [procesar automáticamente el contenido localizado correspondiente](get-started/localization.md). |
| Abrir origen | Si algo no funciona como debería, [contribuya con sus mejoras](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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
* [Visualizador de PDF](components/pdf-viewer.md)

### Componentes de contenedor {#container-components}

* [Contenedor](components/container.md)
* [Carrusel](components/carousel.md)
* [Pestañas](components/tabs.md)
* [Acordeón](components/accordion.md)

### Componentes de formulario {#form-components}

* [Contenedor del formulario](components/forms/form-container.md)
* [Texto de formulario](components/forms/form-text.md)
* [Opciones de formulario](components/forms/form-options.md)
* [Formulario oculto](components/forms/form-hidden.md)
* [Botón de formulario](components/forms/form-button.md)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](get-started/using.md). Una vez integrados, pueden ponerse a disposición de los usuarios y preconfigurarse mediante el [editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

>[!NOTE]
>
>Puede que algunas versiones de los componentes principales individuales solo sean compatibles con algunas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada a la lista anterior) para obtener información sobre la compatibilidad de componentes específicos o consulte el documento [Versiones de componentes principales](versions.md) para obtener más información.

## Requisitos del sistema {#system-requirements}

| Componentes principales | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.14) | Continua | 6.5.6.0+ * | 6.4.8.4+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) Desde la versión 2.11.0, se requiere la versión 1.4.12 o superior de `org.apache.sling.models.impl` (debido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Esto se proporcionará para AEM 6.4 y 6.5 en un futuro Service Pack. Hasta entonces, el paquete de modelos Sling se incluye en el paquete `core.wcm.components.all`.

Para conocer los requisitos de las versiones anteriores de los componentes principales, consulte [Versiones de los componentes principales](versions.md).

Los componentes principales requieren el uso de [plantillas editables](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=es) y no admiten la interfaz de usuario clásica ni plantillas estáticas. Si es necesario, consulte las [Herramientas de modernización de AEM](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) para actualizar el proyecto con estas funciones modernas de AEM.

Para configurar su entorno de desarrollo local, consulte [esta descripción general de AEM Cloud Service SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=es) o este documento [para versiones anteriores de AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=es).

>[!TIP]
>
>Los componentes principales forman parte automáticamente de AEM Cloud Service y siempre tendrá la última versión de los componentes principales.
>
>Consulte el documento [Uso de componentes principales](/help/get-started/using.md) para obtener más información sobre cómo empezar a utilizar los componentes principales tanto en AEMaaCS como en línea.
