---
title: Introducción a los componentes principales
description: 'Los componentes principales proporcionan componentes básicos robustos y ampliables, basados en la tecnología y las prácticas recomendadas más recientes. '
translation-type: tm+mt
source-git-commit: 456bd449f5776355923bcd859a2afb6b00f33d5c
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 26%

---


# Introducción a los componentes principales{#core-components-introduction}

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas creadas. Los componentes siempre han sido un elemento fundamental de la experiencia de AEM, ya que la creación de páginas se simplifica pero mantiene su potencia para el autor; asimismo, el desarrollo de componentes es flexible y extensible para el desarrollador.

Los componentes principales son un conjunto de componentes de Gestor de contenido web (WCM) estandarizados para AEM a fin de acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de los sitios web.

## Medios {#resources}

* **[Biblioteca de componentes:](https://www.adobe.com/go/aem_cmp_library)** colección de ejemplos para la vista de los componentes en sus distintas configuraciones.
* **Documentación de componentes (este documento):** Para desarrolladores y autores, con detalles sobre cada componente.
* **[Repositorio de GitHub de componentes principales:](https://github.com/adobe/aem-core-wcm-components)** para obtener detalles de desarrollador de cada componente y descarga de proyecto.
* Introducción:
   * **[Éxito con los componentes principales:](/help/developing/success.md)** Directrices para tener en cuenta antes del inicio de cualquier proyecto que vaya a utilizar los componentes principales.
   * **[Tutorial de WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** un tutorial de dos días para crear un nuevo sitio.
   * **[Tutorial de la Cumbre: ](https://expleague.azureedge.net/labs/L767/index.html)** Un tutorial de dos horas para construir un nuevo sitio (de un laboratorio en la Cumbre de Estados Unidos 2019).
   * **[Seminario web de Gems: ](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** una visita guiada de los componentes principales (grabada en diciembre de 2018).

## Características {#features}

|  |  |
|---|---|
| Listo para la producción | Los componentes principales son 28 componentes robustos que están bien probados, se utilizan ampliamente y que funcionan bien. |
| Preparado para la nube | Ya sea en [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), en [Servicios administrados de Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ, simplemente funcionan. |
| Versátil | Los componentes representan conceptos genéricos con los que los autores pueden ensamblar casi cualquier diseño. |
| Configurable | Las [directivas de contenido](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) de nivel de plantilla definen qué características pueden utilizar o no los autores de la página. |
| Trackable | La [integración de capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md) permite el seguimiento de todos los aspectos de la experiencia de visitante. |
| Accesible | Cumplen [WCAG 2.1 estándar](https://www.w3.org/TR/WCAG21/), proporcionan etiquetas ARIA y admiten la navegación mediante el teclado ([problemas conocidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+access+in%3Atítulo)). |
| Compatible con SEO | El resultado HTML es semántico y proporciona [anotaciones de microdatos de esquema.org](https://schema.org). |
| Listo para WebApp | La [salida JSON optimizada](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) permite el procesamiento en el lado del cliente, aún con la posibilidad de [edición en contexto](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| Compatibilidad con AMP | Los componentes tienen [compatibilidad integrada con el estándar AMP,](/help/developing/amp.md) lo que acelera sus experiencias móviles. |
| Kit de diseño | Un [kit de interfaz de usuario para Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) permite a los diseñadores crear esquemas que luego pueden [aplicar estilo según sea necesario](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Themeable | Los componentes implementan el [sistema de estilo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html) y el marcado sigue [convenciones CSS de BEM](http://getbem.com/). |
| Personalizable | Varios patrones permiten [una fácil personalización](developing/customizing.md), desde ajustar el HTML hasta una reutilización avanzada de la funcionalidad. |
| Versiones | La [directiva de versiones](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiza que los Componentes principales no interrumpan el sitio al mejorar las cosas que puedan afectarle. |
| Localizable | La resolución de referencia inteligente permite que ciertos componentes encuentren y [procesen automáticamente el contenido localizado correspondiente](get-started/localization.md). |
| Abrir fuente | Si algo no es como debería, [contribuya con sus mejoras.](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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

### Componentes de formulario{#form-components}

* [Contenedor del formulario](components/forms/form-container.md)
* [Texto de formulario](components/forms/form-text.md)
* [Opciones de formulario](components/forms/form-options.md)
* [Formulario oculto](components/forms/form-hidden.md)
* [Botón de formulario](components/forms/form-button.md)

>[!NOTE]
>
>Los componentes principales no están disponibles para los autores de manera inmediata, ya que el [grupo de desarrollo debe integrarlos primero en su entorno](get-started/using.md). Una vez integrados, pueden estar disponibles y preconfigurados mediante el [editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Puede que algunas versiones de los componentes principales individuales solo sean compatibles con algunas versiones de AEM.
>
>Consulte la página de ayuda individual (vinculada a la lista anterior) para obtener información sobre la compatibilidad de componentes específicos o consulte el documento [Versiones de componentes principales](versions.md) para obtener más información.

## Requisitos del sistema {#system-requirements}

| Componentes principales | AEM as a Cloud Service | AEM 6.5 | AEM 6.4   | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Continua | 6.5.5.0+ * | 6.4.8.1+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) Desde la versión 2.11.0, se requiere `org.apache.sling.models.impl` versión 1.4.12 o superior (debido a [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Esto se proporcionará para AEM 6.4 y 6.5 en un futuro Service Pack. Hasta entonces, el paquete de modelos Sling se incluye en el paquete `core.wcm.components.all`.

Para conocer los requisitos de las versiones anteriores de los componentes principales, consulte [Versiones de componentes principales](versions.md).

Los componentes principales requieren el uso de [plantillas editables](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) y no admiten la IU clásica ni plantillas estáticas. Si es necesario, consulte las [Herramientas de modernización de AEM](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) para actualizar el proyecto con estas características de AEM modernas.

Para configurar el entorno de desarrollo local, consulte [esta descripción general para AEM como un SDK de Cloud Service](https://docs.adobe.com/content/help/es-ES/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) o este documento [para versiones anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
