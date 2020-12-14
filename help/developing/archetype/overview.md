---
title: Tipo de archivo del proyecto AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
translation-type: tm+mt
source-git-commit: 794408e8b643de2234664e69e59e1108cf286cd7
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 10%

---


# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El Arquetipo de proyecto AEM es una plantilla Maven que crea un proyecto de Adobe Experience Manager (AEM) mínimo y basado en optimizaciones como punto de partida para su sitio web.

>[!TIP]
>
>El último arquetipo del proyecto de AEM [se puede encontrar en GitHub](https://github.com/adobe/aem-project-archetype).

## Medios {#resources}

* **Documentación de arquetipos (este documento):** Visión general de la arquitectura de arquetipos y sus diferentes módulos.
   * **[Uso del arquetipo:](using.md)** más detalles sobre el uso del arquetipo y los módulos disponibles
   * **[ui.frontender:](uifrontend.md)** Cómo usar el módulo de compilación front-end
* Los siguientes tutoriales están basados en este arquetipo:
   * **[Sitio WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Conozca cómo crear un nuevo sitio web de inicio.
   * **[Aplicación de una sola página WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** aprenda a crear una aplicación web React o Angular totalmente autorizada en AEM.

## Características {#features}

* **Práctica recomendada:** Bootstrap del sitio con todas las prácticas recomendadas más recientes de Adobe.
* **Código bajo:** edite las plantillas, cree contenido, implemente su CSS y el sitio esté listo para su lanzamiento.
* **Preparado para la nube:** si lo desea, utilice  [AEM como ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) servicio de nube para activarse en pocos días y facilitar la escalabilidad y el mantenimiento.
* **Dispatcher:** Un proyecto se completa únicamente con una  [configuración ](https://docs.adobe.com/content/help/es-ES/experience-manager-dispatcher/using/dispatcher.html) de Dispatcher que garantiza velocidad y seguridad.
* **Múltiples sitios:** Si es necesario, el arquetipo genera la estructura de contenido para una configuración [ ](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html) de varios idiomas y regiones.
* **Componentes principales:** Los autores pueden crear casi cualquier diseño con nuestro versátil  [conjunto de componentes](/help/introduction.md) estandarizados.
* **Plantillas editables:** Monte prácticamente cualquier  [plantilla sin código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) y defina lo que los autores pueden editar.
* **Diseño adaptable:** en plantillas o páginas individuales,  [defina el modo en que los elementos se ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) redimensionan para los puntos de interrupción definidos.
* **Encabezado y pie de página:** Monte y localícelos sin código, utilizando las funciones de  [localización de los componentes](https://docs.adobe.com/content/help/es-ES/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilos:** evite crear componentes personalizados permitiendo a los autores  [aplicarles diferentes ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) estilos.
* **Compilación front-end: los desarrolladores** front-end pueden  [burlarse de ](uifrontend.md#webpack-dev-server) las páginas y  [crear ](uifrontend.md) bibliotecas de cliente con Webpack, TypeScript y SASS.
* **Listo para WebApp:** para sitios que utilizan  [](uifrontend-react.md) Reactor  [Angular](uifrontend-angular.md), utilice el  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDKpara conservar la creación  [en contexto de la aplicación](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Comercio habilitado:** Para proyectos que deseen integrar  [AEM ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) comercio con soluciones comerciales como  [](https://magento.com/) Magentousing the  [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Código de ejemplo:** Cierre la compra del componente HelloWorld y de los modelos de muestra, servlets, filtros y Planificadoras.
* **Open Sourced:** Si algo no es como debería,  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) contribuya a sus mejoras.

## Uso

Para generar un proyecto, ajuste la línea de comandos siguiente según sus necesidades:

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=24 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Configure `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Configure `aemVersion=6.5.0` para [Servicios administrados de Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ.
La dependencia de Componentes principales solo se agrega para las versiones de Aem que no son de nube, ya que los Componentes principales se proporcionan OOTB para AEM como Cloud Service.
* Ajuste `appTitle="My Site"` para definir el título del sitio Web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir Maven artifactsId, los nombres de los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de clientes.
* Ajuste `groupId="com.mysite"` para definir el groupId de Maven y el paquete de origen de Java.
* Busque la lista de propiedades disponibles para ver si hay más que desea ajustar.

## Propiedades disponibles

| Nombre | Predeterminado | Descripción |
--------------------------|----------------|--------------------
| `appTitle` |  | El título de la aplicación se utilizará para el título del sitio web y los grupos de componentes (p. ej. `"My Site"`). |
| `appId` |  | El nombre técnico se utilizará para los nombres de los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente (p. ej. `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefacto de la mueble base (p. ej. `"mysite"`). |
| `groupId` |  | ID de grupo de Maven base (p. ej. `"com.mysite"`). |
| `package` | *`${groupId}`* | Paquete de fuentes Java (p. ej. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versión del proyecto (p. ej. `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Destinatario AEM versión (puede ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); o `6.5.0`, o `6.4.4` para [Servicios administrados de Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ). |
| `sdkVersion` | `latest` | Cuando `aemVersion=cloud` se puede especificar una versión [SDK](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (p. ej. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Incluye una configuración de distribuidor para cloud o para AMS/in situ, según el valor de `aemVersion` (puede ser `y` o `n`). |
| `frontendModule` | `general` | Incluye un módulo de compilación de front-end de Webpack que genera bibliotecas de cliente (puede ser `general` o `none` para sitios regulares; puede ser `angular` o `react` para una aplicación de una sola página que implemente el [Editor de SPA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Código de idioma (ISO 639-1) desde el que se crea la estructura de contenido (p. ej. `en`, `deu`). |
| `country` | `us` | Código de país (ISO 3166-1) desde el que crear la estructura de contenido (p. ej. `US`). |
| `singleCountry` | `y` | Incluye una estructura de contenido maestro-idioma (puede ser `y` o `n`). |
| `includeExamples` | `n` | Incluye un sitio de ejemplo de [Biblioteca de componentes](https://www.aemcomponents.dev/) (puede ser `y` o `n`). |
| `includeErrorHandler` | `n` | Incluye una página de respuesta personalizada 404 que será global para toda la instancia (puede ser `y` o `n`). |
| `includeCommerce` | `n` | Incluye dependencias [Componentes principales de CIF](https://github.com/adobe/aem-core-cif-components) y genera artefactos correspondientes. |
| `commerceEndpoint` |  | Necesario solo para CIF. Extremo opcional del servicio GraphQL del sistema de comercio que se va a utilizar (p. ej. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Active la integración con [capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilite la compatibilidad con [AMP](/help/developing/amp.md) para plantillas de proyecto generadas. |

## Requisitos del sistema

| Archetype | AEM as a Cloud Service | AEM 6.5 | AEM 6.4   | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | Continua | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Configure el entorno de desarrollo local para [AEM como un SDK de Cloud Service](https://docs.adobe.com/content/help/es-ES/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) o para [versiones anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conocidos

Cuando se ejecuta en Windows y se genera la configuración del despachante, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Cuando se ejecuta el arquetipo en modo interactivo (sin el parámetro `-B`), las propiedades con valores predeterminados no se pueden cambiar, a menos que se descarte la confirmación final, lo que después repite las preguntas incluyendo las propiedades con valores predeterminados en las preguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obtener más información).

## Lectura adicional {#further-reading}

Para obtener más información sobre el uso del arquetipo, incluidos sus beneficios, opciones y cómo funcionan sus módulos, consulte el [Uso del documento Archetype.](using.md)
