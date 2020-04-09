---
title: Tipo de archivo del proyecto AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El arquetipo de proyecto de AEM es una plantilla Maven que crea un proyecto mínimo y basado en las prácticas recomendadas de Adobe Experience Manager (AEM) como punto de partida para su sitio web.

>[!TIP]
>
>El último arquetipo de proyecto de AEM [se encuentra en GitHub](https://github.com/adobe/aem-project-archetype).

## Medios {#resources}

* **Documentación de arquetipos (este documento):** Descripción general de la arquitectura del arquetipo y sus diferentes módulos.
   * **[Uso del arquetipo:](using.md)**más detalles sobre el uso del arquetipo y los módulos disponibles
   * **[ui.front:](uifrontend.md)**Cómo utilizar el módulo de compilación front-end
* Los siguientes tutoriales están basados en este arquetipo:
   * **[Sitio WKND:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Aprenda a inicio de un nuevo sitio web.
   * **[Aplicación de página única WKND:](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**Obtenga información sobre cómo crear una aplicación web React o Angular totalmente autorizada en AEM.

## Características {#features}

* **Práctica recomendada:** Bootstrap de su sitio con todas las prácticas recomendadas más recientes de Adobe.
* **Código bajo:** Edite sus plantillas, cree contenido, implemente su CSS y el sitio esté listo para su lanzamiento.
* **Preparado para la nube:** Si lo desea, utilice [AEM como servicio](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) de nube para empezar a utilizarlo en pocos días y facilitar la escalabilidad y el mantenimiento.
* **Dispatcher:** Un proyecto solo se completa con una configuración [](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) Dispatcher que garantiza la velocidad y la seguridad.
* **Varios sitios:** Si es necesario, el arquetipo genera la estructura de contenido para una configuración [](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html)de varios idiomas y regiones.
* **Componentes principales:** Los autores pueden crear casi cualquier diseño con nuestro versátil [conjunto de componentes](/help/introduction.md)estandarizados.
* **Plantillas editables:** Monte prácticamente cualquier [plantilla sin código](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)y defina lo que los autores pueden editar.
* **Diseño adaptable:** En plantillas o páginas individuales, [defina cómo se redistribuyen](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) los elementos para los puntos de interrupción definidos.
* **Encabezado y pie de página:** Monte y localícelos sin código, utilizando las funciones de [localización de los componentes](https://docs.adobe.com/content/help/es-ES/experience-manager-core-components/using/get-started/localization.html).
* **Sistema de estilos:** Evite crear componentes personalizados permitiendo que los autores [les apliquen estilos](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) diferentes.
* **Diseño front-end:** Los desarrolladores de front-end pueden [burlarse de las páginas](uifrontend.md#webpack-dev-server) de AEM y [crear bibliotecas](uifrontend.md) de cliente con Webpack, TypeScript y SASS.
* **Listo para WebApp:** Para los sitios que utilizan [React](uifrontend-react.md) o [Angular](uifrontend-angular.md), utilice el SDK [de](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) SPA para conservar la creación [en contexto de la aplicación](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Código de ejemplo:** Cierre el componente HelloWorld y los modelos de muestra, servelets, filtros y Planificadoras.
* **Abrir fuente:** Si algo no es como debería, ¡ [contribuya](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) con sus mejoras!

## Uso

Para generar un proyecto, ajuste la línea de comandos siguiente según sus necesidades:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Se configura `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)o in situ.
La dependencia Componentes principales solo se agrega para las versiones de Aem que no son de nube, ya que los Componentes principales se proporcionan OOTB para AEM como un servicio de nube.
* Ajuste `appTitle="My Site"` para definir el título del sitio web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir Maven artifactsId, los nombres de los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente.
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
| `aemVersion` | `6.5.0` | Versión de AEM de Destinatario (puede ser `cloud` para [AEM como un servicio](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)de nube; o `6.5.0`, `6.4.4`o `6.3.3` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ). |
| `sdkVersion` | `latest` | Cuando se puede especificar `aemVersion=cloud` una versión del [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (p. ej. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Incluye una configuración de distribuidor para cloud o para AMS/in situ, según el valor de `aemVersion` (puede ser `y` o `n`). |
| `frontendModule` | `none` | Incluye un módulo de compilación de front-end de Webpack que genera las bibliotecas de cliente (puede ser `general` o `none` para sitios normales; puede ser `angular` o `react` para una aplicación de una sola página que implemente el Editor [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)SPA). |
| `languageCountry` | `en_us` | Idioma y código de país desde los que crear la estructura de contenido (p. ej. `en_us`). |
| `singleCountry` | `y` | Incluye una estructura de contenido maestro-idioma (puede ser `y`o `n`). |
| `includeExamples` | `y` | Incluye un sitio de ejemplo de la biblioteca [de](https://www.aemcomponents.dev/) componentes (puede ser `y`o `n`). |
| `includeErrorHandler` | `n` | Incluye una página de respuesta personalizada 404 que será global para toda la instancia (puede ser `y` o `n`). |

## Requisitos del sistema

| Archetype | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | Continua | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Configure el entorno de desarrollo local para [AEM como un SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) de servicio de nube o para versiones [anteriores de AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Problemas conocidos

Cuando se ejecuta en Windows y se genera la configuración del despachante, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Cuando se ejecuta el arquetipo en modo interactivo (sin el `-B` parámetro), las propiedades con valores predeterminados no se pueden cambiar, a menos que se descarte la confirmación final, lo que después repite las preguntas incluyendo las propiedades con valores predeterminados en las preguntas (consulte[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obtener más información).

## Lectura adicional {#further-reading}

Para obtener más información sobre el uso del arquetipo, incluyendo sus beneficios, opciones y cómo funcionan sus módulos, consulte el documento [Uso del arquetipo.](using.md)