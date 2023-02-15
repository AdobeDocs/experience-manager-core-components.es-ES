---
title: Tipo de archivo del proyecto AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 0d004c90e789f23ff9e121fbd8ae11df9c9748b2
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 100%

---

# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El tipo de archivo del proyecto de AEM es una plantilla de Maven que crea un proyecto mínimo de Adobe Experience Manager (AEM) basado en las prácticas recomendadas como punto de partida para su sitio web.

>[!TIP]
>
>El último tipo de archivo del proyecto de AEM [se encuentra en GitHub.](https://github.com/adobe/aem-project-archetype)

## Medios {#resources}

* **Documentación de tipo de archivo (este documento):** Información general sobre la arquitectura de tipo de archivo y sus distintos módulos.
   * **[Uso del tipo de archivo:](using.md)** Más información sobre el uso del tipo de archivo y los módulos disponibles
   * **[ui.frontend:](uifrontend.md)** Cómo usar el módulo de versión del front-end
* **Los siguientes tutoriales están basados en este tipo de archivo:**
   * **[Sitio WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es)** Aprenda a iniciar un nuevo sitio web.
   * **[Aplicación de una sola página WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es)** Aprenda a crear una aplicación web de React o Angular totalmente legible en AEM.

## Características {#features}

* **Práctica recomendada:** inicie su sitio con todas las prácticas recomendadas más recientes de Adobe.
* **Código bajo:** edite sus plantillas, cree contenido, implemente su CSS y el sitio estará listo para su publicación.
* **Preparado para la nube:** si lo desea, utilice [AEM Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es) para publicarlo en pocos días y facilitar la escalabilidad y el mantenimiento.
* **Dispatcher:** un proyecto se completa solamente con una [configuración de Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=es)que garantice la velocidad y la seguridad.
* **Varios sitios:** si es necesario, el tipo de archivo genera la estructura de contenido para una [configuración de varios idiomas y regiones](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=es).
* **Componentes principales:** los autores pueden crear casi cualquier diseño con nuestro versátil [conjunto de componentes estandarizados](/help/introduction.md).
* **Plantillas editables:** combine prácticamente cualquier [plantilla sin código](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=es) y defina lo que los autores pueden editar.
* **Diseño interactivo:** en plantillas o páginas individuales, [defina el reflujo de los elementos](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=es) para los puntos de interrupción definidos.
* **Encabezado y pie de página:** reúna y localícelos sin código, utilizando las [funciones de localización de los componentes](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=es).
* **Sistema de estilos:** evite crear componentes personalizados al permitir que los autores [les apliquen estilos diferentes](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=es).
* **Compilación front-end:** los desarrolladores de front-end pueden [burlar las páginas de AEM](uifrontend.md#webpack-dev-server) y [crear bibliotecas de cliente](uifrontend.md) con Webpack, TypeScript y SASS.
* **Preparado para aplicaciones web:** para sitios que utilizan el [React](uifrontend-react.md) o [Angular](uifrontend-angular.md), utilice el [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=es) para mantener [la autoría en el contexto de la aplicación](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es).
* **Comercio habilitado:** para proyectos que desean integrar [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=es) con soluciones de comercio como [Magento](https://magento.com/es) utilizando [componentes principales de comercio](https://github.com/adobe/aem-core-cif-components).
* **Código de ejemplo:** cierre la compra del componente HelloWorld y de los modelos, servlets, filtros y programadores de ejemplo.
* **Abrir fuente:** si algo no funciona como debería, [contribuya con sus mejoras](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md).

## Uso {#usage}

Para generar un proyecto, ajuste la siguiente línea de comandos según sus necesidades:

```shell
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Sustituya `XX` por el último número de versión del [tipo de archivo.](#requirements)
* Configure `aemVersion=cloud` para [AEM Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es);\
   Configure `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o en línea.
La dependencia de componentes principales solo se agrega para versiones de AEM que no sean en la nube, ya que los componentes principales se proporcionan como OOTB para AEM Cloud Service.
* Ajuste `appTitle="My Site"` para definir el título del sitio web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir los nombres de Maven artifactId, los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente.
* Ajuste `groupId="com.mysite"` para definir el groupId de Maven y el paquete de origen de Java.
* Busque la lista de propiedades disponibles para ver si hay más que desee ajustar.

## Propiedades disponibles {#available-properties}

| Nombre | Predeterminado | Descripción |
|---------------------------|----------------|--------------------|
| `appTitle` |  | El título de la aplicación se utilizará para el título del sitio web y los grupos de componentes (p. ej. `"My Site"`). |
| `appId` |  | El nombre técnico se utilizará para nombres de componentes, configuración y carpetas de contenido, así como nombres de bibliotecas de cliente (p. ej. `"mysite"`). |
| `artifactId` | *`${appId}`* | ID del artefacto base de Maven (p. ej. `"mysite"`). |
| `groupId` |  | ID del grupo base de Maven (p. ej. `"com.mysite"`). Este valor debe ser un [nombre de paquete Java válido](https://docs.oracle.com/javase/specs/jls/se6/html/packages.html#7.7). |
| `package` | *`${groupId}`* | Paquete de origen de Java (p. ej. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versión del proyecto (p. ej. `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Versión de AEM de destino (puede ser `cloud` para [AEM Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es); o `6.5.0` o `6.4.4` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o en línea). |
| `sdkVersion` | `latest` | Cuando `aemVersion=cloud` se puede especificar una versión de [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=es) (p. ej. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Incluye una configuración de Dispatcher para la nube o para AMS/en línea, según el valor de `aemVersion` (puede ser `y` o `n`). |
| `frontendModule` | `general` | Incluye un módulo de versión de front-end de Webpack que genera las bibliotecas de cliente (puede ser `general` o `none` para sitios normales; puede ser `angular` o `react` para una aplicación de una sola página que implementa el [Editor SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/editor-overview.html?lang=es)). |
| `language` | `en` | Código de idioma (ISO 639-1) desde el que se crea la estructura de contenido (p. ej. `en`, `deu`). |
| `country` | `us` | Código de país (ISO 3166-1) desde el que crear la estructura de contenido (p. ej. `US`). |
| `singleCountry` | `y` | Incluye una estructura de contenido maestra de idioma (puede ser `y` o `n`). |
| `includeExamples` | `n` | Incluye un sitio de ejemplo de la [Biblioteca de componentes](https://www.aemcomponents.dev/) (puede ser `y` o `n`). |
| `includeErrorHandler` | `n` | Incluye una página de respuesta 404 personalizada que será global para toda la instancia (puede ser `y` o `n`). |
| `includeCommerce` | `n` | Incluye las dependencias [Componentes principales del CIF](https://github.com/adobe/aem-core-cif-components) y genera los artefactos correspondientes. |
| `commerceEndpoint` |  | Necesario solo para CIF. Punto final opcional del servicio GraphQL del sistema de comercio que se va a utilizar (p. ej. `https://hostname.com/grapql`). |
| `includeFormscommunications` | `n` | Incluye dependencias, plantillas, modelos de datos de formulario y temas de [Componentes principales de Forms](https://github.com/adobe/aem-core-forms-components) y genera los elementos correspondientes para los programas de comunicaciones de Forms. |
| `includeFormsenrollment` | `n` | Incluye dependencias, plantillas, modelos de datos de formulario y temas de [Componentes principales de Forms](https://github.com/adobe/aem-core-forms-components) y genera los elementos correspondientes para los programas de inscripción de Forms. |
| `sdkFormsVersion` | `latest` | Cuando `aemVersion=cloud` y uno de `includeFormsenrollment=y` o `includeFormscommunications=y`, se puede especificar una versión del SDK de Forms (por ejemplo `2020.12.17.02`). |
| `datalayer` | `y` | Activar la integración con la [Capa de datos del cliente de Adobe](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Habilite la compatibilidad con [AMP](/help/developing/amp.md) para plantillas de proyecto generadas. |
| `enableDynamicMedia` | `n` | Habilita los componentes básicos de Dynamic Media en la configuración de directivas de proyecto y activa las funciones de Dynamic Media en la directiva del componente de imagen principal. |
| `enableSSR` | `n` | Opción para habilitar SSR para el proyecto front-end |
| `precompiledScripts` | `n` | Opción para [precompilar](/help/developing/archetype/precompiled-bundled-scripts.md) los scripts del lado del servidor de `ui.apps` y adjuntarlos a la versión como un artefacto de paquete secundario en el proyecto `ui.apps`. `aemVersion` debe establecerse en `cloud`. |
| `includeFormsheadless` | `n` | Incluye las dependencias de los [Componentes principales de Forms](https://github.com/adobe/aem-core-forms-components), `ui.frontend.react.forms.af`, y artefactos sin encabezado. |

## Requisitos del sistema {#requirements}

| Tipo de archivo | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [40](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-40) | Continua | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Configure su entorno de desarrollo local para [AEM Cloud Service SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=es) o para [versiones anteriores de AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=es).

### Problemas conocidos {#known-issues}

Cuando se ejecuta en Windows y genera la configuración de Dispatcher, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Al ejecutar el tipo de archivo en modo interactivo (sin el parámetro `-B`), las propiedades con valores predeterminados no se pueden cambiar, a menos que se descarte la confirmación final, que después repite las preguntas incluyendo las propiedades con valores predeterminados en las preguntas (consulte
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para más detalles).

No se puede usar este tipo de archivo en Eclipse al iniciar un nuevo proyecto con `File -> New -> Maven Project`, ya que el script de generación posterior `archetype-post-generate.groovy` no se ejecutará debido a un problema con [Eclipse.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) La solución es usar la línea de comandos anterior y luego usar Eclipse `File -> Import -> Existing Maven Project`.

## Lectura adicional {#further-reading}

Para obtener más información sobre el uso del tipo de archivo, incluidas sus ventajas, opciones y cómo funcionan sus módulos, consulte el documento [Utilizar el tipo de archivo.](using.md)
