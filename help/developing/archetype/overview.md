---
title: Tipo de archivo del proyecto AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Architect, Developer, Administrator
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: b5ad1c874d5f6d6781c2d0b0cc992b278c91211b
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 9%

---

# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El tipo de archivo del proyecto de AEM es una plantilla de Maven que crea un proyecto mínimo de Adobe Experience Manager (AEM) basado en las prácticas recomendadas como punto de partida para su sitio web.

>[!TIP]
>
>El último tipo de archivo del proyecto AEM [se encuentra en GitHub.](https://github.com/adobe/aem-project-archetype)

## Medios {#resources}

* **Documentación de tipo de archivo (este documento):** Información general sobre la arquitectura de tipo de archivo y sus distintos módulos.
   * **[Uso del tipo de archivo:](using.md)** más información sobre el uso del tipo de archivo y los módulos disponibles
   * **[ui.frontend:](uifrontend.md)** Uso del módulo de compilación del front-end
* Los siguientes tutoriales están basados en este tipo de archivo:
   * **[Sitio WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Aprenda a iniciar un nuevo sitio web.
   * **[Aplicación de una sola página WKND: ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Aprenda a crear una aplicación web de React o Angular totalmente legible en AEM.

## Características {#features}

* **Práctica recomendada:** Bootstrap su sitio con todas las prácticas recomendadas más recientes de Adobe.
* **Código bajo:** edite sus plantillas, cree contenido, implemente su CSS y el sitio esté listo para su lanzamiento.
* **Preparado para la nube:** si lo desea, utilice  [AEM as a Cloud ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Service para empezar a utilizarlo en pocos días y facilitar la escalabilidad y el mantenimiento.
* **Dispatcher:** un proyecto se completa solamente con una  [configuración de ](https://docs.adobe.com/content/help/es-ES/experience-manager-dispatcher/using/dispatcher.html) Dispatcher que garantice la velocidad y la seguridad.
* **Varios sitios:** si es necesario, el tipo de archivo genera la estructura de contenido para una configuración [ ](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html) de varios idiomas y regiones.
* **Componentes principales:** los autores pueden crear casi cualquier diseño con nuestro versátil  [conjunto de componentes](/help/introduction.md) estandarizados.
* **Plantillas editables:** combine prácticamente cualquier  [plantilla sin código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) y defina lo que los autores pueden editar.
* **Diseño interactivo:** en plantillas o páginas individuales,  [defina cómo se ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) reflejan los elementos para los puntos de interrupción definidos.
* **Encabezado y pie de página:** reúna y localícelos sin código, utilizando las funciones de  [localización de los componentes](https://docs.adobe.com/content/help/es-ES/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilos:** evite crear componentes personalizados al permitir que los autores  [les apliquen ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) estilos diferentes.
* **Compilación front-end:** los desarrolladores de front-end pueden  [burlarse de AEM ](uifrontend.md#webpack-dev-server) páginas y  [crear ](uifrontend.md) bibliotecas de cliente con Webpack, TypeScript y SASS.
* **Preparado para la aplicación web:** para sitios que utilizan el  [](uifrontend-react.md)  [Angular](uifrontend-angular.md) de Reactor, utilice el  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDK para mantener la creación  [en contexto de la aplicación](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Comercio habilitado:** para proyectos que desean integrar  [AEM ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) comercio con soluciones de comercio como  [](https://magento.com/) Magentousing the  [Commerce Core Components](https://github.com/adobe/aem-core-cif-components).
* **Código de ejemplo:** cierre la compra del componente HelloWorld y de los modelos, servlets, filtros y programadores de ejemplo.
* **Abrir fuente:** si algo no funciona como debería, ¡ [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) contribuya con las mejoras!

## Uso {#usage}

Para generar un proyecto, ajuste la siguiente línea de comandos según sus necesidades:

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Sustituya `XX` por el último número de versión del [tipo de archivo.](#requirements)
* Configure `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Configure `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o local.
La dependencia de componentes principales solo se agrega para versiones de aem que no sean de nube, ya que los componentes principales se proporcionan como OOTB para AEM como Cloud Service.
* Ajuste `appTitle="My Site"` para definir el título del sitio web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir los nombres de Maven artifactId, los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente.
* Ajuste `groupId="com.mysite"` para definir el groupId de Maven y el Paquete de origen de Java.
* Busque la lista de propiedades disponibles para ver si hay más que desee ajustar.

## Propiedades disponibles {#available-properties}

| Nombre | Predeterminado | Descripción |
|---------------------------|----------------|--------------------|
| `appTitle` |  | El título de la aplicación se utilizará para el título del sitio web y los grupos de componentes (p. ej. `"My Site"`). |
| `appId` |  | Nombre técnico, se utilizará para nombres de componentes, configuración y carpetas de contenido, así como nombres de bibliotecas de cliente (p. ej. `"mysite"`). |
| `artifactId` | *`${appId}`* | ID del artefacto de Maven base (p. ej. `"mysite"`). |
| `groupId` |  | ID del grupo Maven base (p. ej. `"com.mysite"`). |
| `package` | *`${groupId}`* | Paquete de fuentes Java (p. ej. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versión del proyecto (p. ej. `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Versión de AEM de destino (puede ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); o `6.5.0` o `6.4.4` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o local). |
| `sdkVersion` | `latest` | Cuando `aemVersion=cloud` se puede especificar una versión de [SDK](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (p. ej. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Incluye una configuración de Dispatcher para cloud o para AMS/on-premise, según el valor de `aemVersion` (puede ser `y` o `n`). |
| `frontendModule` | `general` | Incluye un módulo de compilación de front-end de Webpack que genera las bibliotecas de cliente (puede ser `general` o `none` para sitios normales; puede ser `angular` o `react` para una aplicación de una sola página que implementa el [SPA Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Código de idioma (ISO 639-1) desde el que se crea la estructura de contenido (p. ej. `en`, `deu`). |
| `country` | `us` | Código de país (ISO 3166-1) desde el que crear la estructura de contenido (p. ej. `US`). |
| `singleCountry` | `y` | Incluye una estructura de contenido maestra de idioma (puede ser `y` o `n`). |
| `includeExamples` | `n` | Incluye un sitio de ejemplo de [Biblioteca de componentes](https://www.aemcomponents.dev/) (puede ser `y` o `n`). |
| `includeErrorHandler` | `n` | Incluye una página de respuesta 404 personalizada que será global para toda la instancia (puede ser `y` o `n`). |
| `includeCommerce` | `n` | Incluye dependencias [Componentes principales del CIF](https://github.com/adobe/aem-core-cif-components) y genera los artefactos correspondientes. |
| `commerceEndpoint` |  | Necesario solo para CIF. Punto final opcional del servicio GraphQL del sistema de comercio que se va a utilizar (p. ej. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Active la integración con [Adobe Client Data Layer](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilite la compatibilidad con [AMP](/help/developing/amp.md) para plantillas de proyecto generadas. |
| `enableDynamicMedia` | `n` | Habilita los componentes básicos de Dynamic Media en la configuración de directivas de proyecto y activa las funciones de Dynamic Media en la política del componente de imagen principal. |
| `enableSSR` | `n` | Opción para habilitar SSR para el proyecto front-end |

## Requisitos del sistema {#requirements}

| Tipo de archivo | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [28](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-28) | Continua | Más de 6.5.7.0 | 8, 11 | 3.3.9+ |

Configure su entorno de desarrollo local para [AEM como SDK de Cloud Service](https://docs.adobe.com/content/help/es-ES/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) o para [versiones anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conocidos {#known-issues}

Cuando se ejecuta en Windows y genera la configuración de Dispatcher, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Al ejecutar el tipo de archivo en modo interactivo (sin el parámetro `-B`), las propiedades con valores predeterminados no se pueden cambiar, a menos que se descarte la confirmación final, que después repite las preguntas incluyendo las propiedades con valores predeterminados en las preguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para más detalles).

No se puede usar este tipo de archivo en Eclipse al iniciar un nuevo proyecto con `File -> New -> Maven Project`, ya que el script de generación posterior `archetype-post-generate.groovy` no se ejecutará debido a un problema con [Eclipse.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) La solución es usar la línea de comandos anterior y luego usar Eclipse  `File -> Import -> Existing Maven Project`.

## Lectura adicional {#further-reading}

Para obtener más información sobre el uso del tipo de archivo, incluidas sus ventajas, opciones y cómo funcionan sus módulos, consulte el documento [Uso del tipo de archivo.](using.md)
