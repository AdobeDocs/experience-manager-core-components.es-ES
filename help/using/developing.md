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
source-git-commit: 600aefa49d6247c290b8fb9f6acf5548126b3f61

---


# Desarrollo de componentes principales{#developing-core-components}

## Información general {#overview}

Los componentes principales proporcionan componentes base sólidos y extensibles, y sus resaltados son:

* Funciones ricas en funciones
   * [Opciones flexibles de configuración](authoring.md) para dar cabida a muchos casos de uso
   * [Capacidades preconfigurables](authoring.md#pre-configuring-core-components) para definir qué funciones están disponibles para los autores de páginas
* Entrega continua
   * Mejoras frecuentes de funcionalidad incremental
   * Disponibilidad del código [fuente en github](https://github.com/adobe/aem-core-wcm-components) para permitir que la comunidad de desarrolladores proporcione comentarios y contribuya
   * Instalación a través de [un paquete de contenido publicado por separado](https://github.com/adobe/aem-core-wcm-components/releases) para actualizaciones de componentes que se realizará de forma independiente con las actualizaciones de AEM
* [Control de versiones de componentes](guidelines.md#component-versioning)
   * [Garantice la compatibilidad dentro de una versión](#upgrade-of-core-components), pero permita que los componentes evolucionen
   * Permitir coexistir varias versiones de un componente en el mismo entorno
* Implementación moderna
   * Marcado definido en [el lenguaje de plantilla HTML](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Lógica del modelo de contenido implementada con [Sling Models](https://sling.apache.org/documentation/bundles/models.html)
* Marcado de marca
   * Notación del [modificador](https://getbem.com/) de elemento bloque (BEM) desde la versión 2.0.0
      * La versión anterior sigue [las convenciones](https://getbootstrap.com/css/) de nomenclatura de Bootstrap
   * Se basa en [las directrices de accesibilidad](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capacidad para utilizarse para sitios interactivos y móviles
* Capacidad para serializar como JSON el modelo de contenido para casos de uso CMS headless
* Accesible
   * Compatible con el estándar [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Los componentes principales requieren AEM 6.3 o posterior y Java 8.
>
>Los componentes principales no funcionan con la IU clásica.

## Información general de sesión de Gems {#gems-session-overview}

Para obtener una introducción a los componentes principales, las características que ofrecen y cómo se aprovechan en AEM, consulte los componentes de AEM Session [AEM Session de AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Maravillas de Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) es una serie de consejos técnicos proporcionados por expertos de Adobe. Esta serie complementa la documentación del producto y de todos los demás canales técnicos, lo que permite a los desarrolladores familiarizarse con un tema específico.

## Tutorial para desarrolladores WKND {#wknd-developer-tutorial}

[Aprenda a desarrollar sitios AEM con componentes principales siguiendo este paso paso a paso.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Enviado por github {#delivered-over-github}

Los componentes principales se desarrollan y se entregan a través de github.

CÓDIGO EN GITHUB

Puede encontrar el código de esta página en github

* [Abra el proyecto aem-core-wcm-components en github](https://github.com/adobe/aem-core-wcm-components)
* Descargar el proyecto como [archivo ZIP](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Consulte la página [de](using.md) documentación Uso de componentes principales para aprender a empezar a utilizarlos en su proyecto.

Si tiene los componentes principales en github, podrá realizar actualizaciones frecuentes y escuchar los comentarios de la comunidad de desarrolladores de AEM. Además, esto debería ayudar a los clientes y a los socios a seguir patrones similares al crear componentes personalizados.

>[!NOTE]
>
>Para mantenerse informado sobre los cambios más recientes en los componentes principales, puede ver el repositorio de componentes [principales](https://github.com/adobe/aem-core-wcm-components) en github.

## Biblioteca de componentes

Consulte la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html), que exhibe la versión actual de los componentes principales y proporciona ejemplos de su uso.

### Modo de ejecución de contenido de muestra {#sample-content-run-mode}

Los componentes principales son visibles en Quickstart cuando el contenido de muestra está presente, porque el sitio de referencia [de We. Retail los](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) utiliza. Sin embargo, cuando se ejecute en producción (en `nosamplecontent` modo de ejecución, sin contenido de muestra habilitado), los componentes principales ya no estarán presentes y deben instalarse en las instancias de AEM por el equipo de desarrollo o de operaciones.

>[!NOTE]
>
>En entornos de producción, ejecute siempre Quickstart en `nosamplecontent` modo de ejecución. Para utilizar los componentes principales en `nosamplecontent` el modo de ejecución, siga las instrucciones de la página [de documentación Uso de componentes](using.md) principales.

## Capacidades técnicas {#technical-capabilities}

La siguiente tabla proporciona una descripción general de las diferencias entre los componentes principales y los componentes de base.

Para obtener más información sobre las capacidades de creación y las opciones para preconfigurarlas, [consulte la página de creación sobre ellas](authoring.md).

| **Capacidad** | **Componente principal** | **Componente Foundation** |
|-----|---|---|
| Implementación de lógica | Java POJOs with [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotations | Código JSP |
| Definición de marcado | [Sintaxis del lenguaje](https://helpx.adobe.com/experience-manager/htl/user-guide.html) de plantilla HTML (HTL) | Código JSP |
| sanitización XSS | Automatizado por HTL | Principalmente manual |
| Nomenclatura de clases CSS | Convención de nombre estandarizada basada en [notación del Modificador](https://getbem.com/) de elemento bloque (BEM) (desde la versión 2.0.0) | Esquemas personalizados |
| Definición del cuadro de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU clásica |
| Salida JSON | [Sling Models Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling predeterminado |
| Versiones | [Para el modelo y HTL](guidelines.md) | Ninguna |
| Pruebas | Pruebas unitarias + Pruebas de integración | Pruebas de integración |
| Entrega | [A través de github pública](https://github.com/adobe/aem-core-wcm-components) | A través de Quickstart |
| Licencia | [Licencia de Apache](https://www.apache.org/licenses/LICENSE-2.0) | Propiedad de Adobe |
| Contribución | Mediante solicitud de extracción | No posible |
| Accesibilidad | Totalmente compatible con el estándar [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Solo se ajusta parcialmente a la norma [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Lista de componentes {#component-list}

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

### Próximos componentes {#upcoming-components}

Se están trabajando activamente los siguientes componentes principales. Aún no se han publicado, pero se pueden previsualizar en la rama [de desarrollo](https://github.com/adobe/aem-core-wcm-components/tree/development):

* Vídeo
* Descargar

## Actualización de componentes principales {#upgrade-of-core-components}

Una ventaja de los componentes con versiones es que permite separar la migración a una nueva versión de AEM desde la migración a nuevas versiones de componentes. Además, si hay nuevas versiones de componentes disponibles, permite la migración individual de cada componente a la nueva versión.

Las migraciones a una nueva versión de AEM no afectarán el funcionamiento de los componentes principales, siempre y cuando sus versiones también admitan la nueva versión de AEM a la que se migra. Las personalizaciones hechas a los componentes principales no deberían verse afectadas, siempre y cuando no utilicen API que estén [obsoletas o eliminadas](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Las migraciones a nuevas versiones de los componentes principales no afectan a la forma en que funciona el componente, pero es posible que se introduzcan nuevas funciones en los autores de páginas, lo que puede requerir cierta configuración por parte de un editor de plantillas, por si no se desea el comportamiento predeterminado. Es posible que deba adaptar las personalizaciones para obtener más detalles en la página [Personalizar componentes](customizing.md#upgrade-compatibility-of-customizations) principales.

## ¿Cuándo se deben utilizar los componentes principales? {#when-to-use-the-core-components}

Dado que los componentes principales son totalmente nuevos y ofrecen múltiples beneficios, se recomienda que los nuevos proyectos de AEM puedan usarlos. Para los proyectos existentes, una migración debe formar parte de un esfuerzo de proyecto más grande, por ejemplo una remarca o una refactorización general.

Por lo tanto, Adobe proporciona recomendaciones siguientes:

* **Nuevos proyectos**
Los proyectos nuevos siempre deberían intentar utilizar componentes principales. Si los componentes principales no se pueden utilizar directamente ni [se prolongan](customizing.md) para satisfacer los requisitos del proyecto, cree un componente personalizado después de la arquitectura de componentes establecida en los componentes principales. Excepto donde no sea posible, evite utilizar los componentes [base](developing.md).
* **La Recomendación de proyectos**
existente sigue usando los componentes [](developing.md)base, a menos que se planifique una refactorización del sitio o del componente.\
   Dado que la mayoría de los proyectos existentes utilizan muy ampliamente, los componentes [base seguirán siendo compatibles.](developing.md)
* **Nuevos componentes**
personalizados Si se puede personalizar un componente [Core existente](customizing.md).\
   Si no es así, la recomendación es generar un nuevo componente personalizado siguiendo las Pautas [de componentes](guidelines.md).
* **Componentes
personalizados existentes** Si los componentes funcionan correctamente, manténgalos tal y como están.\
   Si no es así, consulte &quot;Nuevos componentes personalizados&quot; arriba.

### Compatibilidad con componentes principales {#core-component-support}

Los componentes principales forman parte integral de AEM y se admiten tal y como está, bajo los mismos términos y condiciones que si se entregaran como parte de Quickstart.

Al igual que otras funciones de productos de AEM, la regla general es: Los componentes se anuncian en primer lugar en desuso y se eliminan primero para la siguiente versión de AEM. Esto proporciona a los clientes al menos un ciclo de publicación para moverse a la nueva versión del componente, antes de colocar su asistencia.

La versión de cada componente indica claramente las versiones de AEM que admite. Cuando la compatibilidad deja de aplicarse a una versión de AEM, entonces es compatible con los componentes principales para esa versión de AEM.

Para obtener más información sobre la compatibilidad de las personalizaciones de componentes, consulte la página [Personalización de componentes](customizing.md) principales.

### Compatibilidad con componentes base {#foundation-component-support}

Dado que los componentes base han servido como base para el desarrollo de tantos proyectos en muchas versiones, se seguirán admitiendo en un futuro próximo.

Sin embargo, el énfasis de desarrollo de Adobe se ha trasladado a los componentes principales y se agregarán nuevas funciones, mientras que solo se realizarán correcciones de errores en los componentes base.

**Siguiente:**

* [Uso de componentes](using.md) principales: familiarícese con los componentes principales en su propio proyecto.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
