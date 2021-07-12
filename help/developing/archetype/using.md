---
title: Uso del tipo de archivo del proyecto AEM
description: Instrucciones de uso detalladas para el tipo de archivo del proyecto AEM
feature: Componentes principales, AEM tipo de archivo del proyecto
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '2147'
ht-degree: 1%

---

# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El tipo de archivo del proyecto de AEM crea un proyecto de Adobe Experience Manager mínimo basado en las prácticas recomendadas como punto de partida para sus propios proyectos de AEM. Las propiedades que se deben proporcionar al utilizar este arquetipo le permiten especificar los nombres de todas las partes de este proyecto, así como controlar determinadas funciones opcionales.

## Por qué utilizar el tipo de archivo {#why-use-the-archetype}

El uso del tipo de archivo del proyecto de AEM le permite avanzar hacia la creación de un proyecto de AEM basado en las prácticas recomendadas con solo unas pocas pulsaciones de teclas. Mediante el uso del tipo de archivo, todas las piezas ya estarán en su lugar para que, aunque el proyecto resultante sea mínimo, ya implemente todas las [características clave](#what-you-get) de AEM para que todo lo que tenga que hacer sea compilar sobre y ampliar.

Por supuesto, hay muchos elementos que entran en un proyecto AEM exitoso, pero el uso del tipo de archivo del proyecto AEM es una base sólida y se recomienda encarecidamente para cualquier proyecto AEM.

## Introducción {#getting-started}

El arquetipo del proyecto facilita el inicio del desarrollo en AEM. Puede realizar sus primeros pasos de varias formas.

* Tutorial de WKND : para obtener una buena introducción al desarrollo en AEM, incluido cómo aprovechar el tipo de archivo, consulte el [Tutorial de introducción a AEM Sites - WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) para ver un ejemplo práctico que le guía a través del uso del tipo de archivo para implementar un proyecto simple.
* Tutorial de eventos WKND : si está especialmente interesado en el desarrollo de aplicaciones de una sola página (SPA) en AEM, asegúrese de consultar el [tutorial de eventos WKND](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html) dedicado.
* Descargue e inicie por su cuenta! - Puede descargar fácilmente el tipo de archivo del proyecto actual disponible en GitHub y crear su primer proyecto [siguiendo los sencillos pasos que se indican a continuación](#how-to-use-the-archetype).

## Qué obtiene utilizando el tipo de archivo {#what-you-get}

El tipo de archivo AEM está formado por módulos:

* **[core](core.md)**: es un paquete Java que contiene todas las funcionalidades principales como servicios OSGi, oyentes y programadores, así como código Java relacionado con componentes como servlets y filtros de solicitud.
* **[it.test](ittests.md)**: son pruebas de integración basadas en Java.
* **[ui.apps](uiapps.md)**: contiene  `/apps` las  `/etc` partes y del proyecto, es decir, clientlibs, componentes y plantillas de JS y CSS.
* **[ui.content](uicontent.md)**: contiene contenido de muestra mediante los componentes del módulo ui.apps .
* **ui.config**: contiene configuraciones OSGi específicas del modo de ejecución para el proyecto.
* **[ui.frontend.general](uifrontend.md)**:  **(opcional)** contiene los artefactos necesarios para utilizar el módulo de compilación del front-end general basado en Webpack.
* **[ui.frontend.react](uifrontend-react.md)**:  **(opcional)** contiene los artefactos necesarios al utilizar el tipo de archivo para crear SPA proyectos basados en React.
* **[ui.frontend.angular](uifrontend-angular.md)**:  **(opcional)** contiene los artefactos necesarios al utilizar el tipo de archivo para crear SPA proyectos basados en el Angular.
* **[ui.testing](uitests.md)**: contiene pruebas de IU basadas en Selenium.
* **todo**: es un paquete de contenido único que incrusta todos los módulos compilados (paquetes y paquetes de contenido), incluidas las dependencias del proveedor.
* **analizar**: ejecuta el análisis en el proyecto, que proporciona una validación adicional para su implementación en AEM como Cloud Service.

![](/help/assets/archetype-structure.png)

Los módulos de AEM tipo de archivo representados en Maven se implementan para AEM como paquetes de contenido que representan la aplicación, el contenido y los paquetes OSGi necesarios.

## Cómo usar el tipo de archivo {#how-to-use-the-archetype}

Para utilizar el tipo de archivo, primero debe crear un proyecto, que genere los módulos en una estructura de archivos local como [descrita anteriormente](#what-you-get). Como parte de la generación de proyectos, se pueden definir varias propiedades para el proyecto, como el nombre del proyecto, la versión, etc.

Al crear el proyecto con Maven, se crean los artefactos (paquetes y paquetes OSGi) que se pueden implementar en AEM. Se pueden utilizar comandos y perfiles adicionales de Maven para implementar los artefactos del proyecto en una instancia de AEM.

### Creación de un proyecto    {#create-project}

Para comenzar, puede utilizar la [AEM extensión Eclipse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html) y seguir el asistente de Nuevo proyecto y elegir **AEM Proyecto de módulo múltiple de muestra** para utilizar una versión liberada del tipo de archivo.

Por supuesto, también puede invocar Maven directamente.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Establezca `XX` en el [número de versión](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) del último tipo de archivo del proyecto AEM.
* Configure `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Configure `aemVersion=6.5.0` para [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o local.
La dependencia de componentes principales solo se agrega para versiones de aem que no sean de nube, ya que los componentes principales se proporcionan como OOTB para AEM as a Cloud
Servicio.
* Ajuste `appTitle="My Site"` para definir el título del sitio web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir los nombres de Maven artifactId, los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente.
* Ajuste `groupId="com.mysite"` para definir el groupId de Maven y el Paquete de origen de Java.
* Busque la lista de propiedades disponibles para ver si hay más que desee ajustar.

>[!NOTE]
>
>Se recomienda añadir el perfil `adobe-public` al archivo Maven `settings.xml` para añadir automáticamente repo.adobe.com al proceso de compilación de maven.
>
>Un ejemplo de POM [se puede encontrar aquí](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Propiedades {#properties}

Las siguientes propiedades están disponibles al crear un proyecto con el tipo de archivo .

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

>[!NOTE]
>
> Si el tipo de archivo se ejecuta en modo interactivo la primera vez, las propiedades con valores predeterminados no se pueden cambiar (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obtener más información). El valor se puede cambiar cuando se deniega la confirmación de la propiedad al final y se repite el cuestionario, o pasando el parámetro en la línea de comandos (por ejemplo, `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Cuando se ejecuta en Windows y genera la configuración de Dispatcher, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [problema 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfiles {#profiles}

El proyecto maven generado admite distintos perfiles de implementación al ejecutar `mvn install`.

| ID de perfil | Descripción |
| --------------------------|------------------------------|
| `autoInstallBundle` | Instale el paquete principal con el complemento maven-sling a la consola felix |
| `autoInstallPackage` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin al gestor de paquetes a la instancia de autor predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallPackagePublish` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin al gestor de paquetes para publicar la instancia predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallSinglePackage` | Instale el paquete de contenido `all` con el complemento content-package-maven-plugin en el gestor de paquetes a la instancia de autor predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallSinglePackagePublish` | Instale el paquete de contenido `all` con el complemento content-package-maven-plugin en el gestor de paquetes para publicar la instancia predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `integrationTests` | Ejecuta las pruebas de integración proporcionadas en la instancia de AEM (solo para la fase `verify`) |

### Creación e instalación {#building-and-installing}

Para crear todos los módulos que se ejecutan en el directorio raíz del proyecto, utilice el siguiente comando Maven.

```shell
mvn clean install
```

Si tiene una instancia de AEM en ejecución, puede crear y empaquetar todo el proyecto e implementarlo en AEM con el siguiente comando Maven.

```shell
mvn clean install -PautoInstallPackage
```

Para implementarlo en una instancia de publicación, ejecute este comando.

```shell
mvn clean install -PautoInstallPackagePublish
```

Como alternativa, para implementar en una instancia de publicación, ejecute este comando.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

O para implementar solo el paquete en el autor, ejecute este comando.

```shell
mvn clean install -PautoInstallBundle
```

## POM principal {#parent-pom}

El `pom.xml` en la raíz del proyecto (`<src-directory>/<project>/pom.xml`) se conoce como el POM principal y controla la estructura del proyecto, así como administra dependencias y ciertas propiedades globales del proyecto.

### Propiedades de proyecto globales {#global-properties}

La sección `<properties>` del POM principal define varias propiedades globales que son importantes para la implementación del proyecto en una instancia de AEM, como nombre de usuario/contraseña, nombre de host/puerto, etc.

Estas propiedades están configuradas para implementarse en una instancia de AEM local, ya que esta es la compilación más común que los desarrolladores realizan. Tenga en cuenta que hay propiedades para implementar en una instancia de autor, así como una instancia de publicación. También es allí donde las credenciales están configuradas para autenticarse con la instancia de AEM. Se utilizan las credenciales predeterminadas admin:admin .

Estas propiedades se configuran para que se puedan sobrescribir al implementarlas en entornos de nivel superior. De este modo, los archivos POM no tienen que cambiar, pero las variables como `aem.host` y `sling.password` pueden anularse mediante argumentos de línea de comandos:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estructura del módulo {#module-structure}

La sección `<modules>` del POM principal define los módulos que el proyecto creará. De forma predeterminada, el proyecto crea [los módulos estándar definidos anteriormente](#what-you-get): core, ui.apps, ui.content, ui.test y it.launcher. Siempre se pueden añadir más módulos a medida que evoluciona un proyecto.

### Dependencias {#dependencies}

La sección `<dependencyManagement>` del POM principal define todas las dependencias y versiones de API que se utilizan en el proyecto. Las versiones deben administrarse en el POM principal. Los submódulos como core y ui.apps no deben incluir información de versión.

#### Uber-Jar {#uber-jar}

Una de las dependencias clave es [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Esto incluirá todas las API de AEM con solo una entrada de dependencia para la versión de AEM.

>[!NOTE]
>
>Se recomienda actualizar la versión de uber-jar para que coincida con la versión de destino de AEM. Por ejemplo, si planea implementar en AEM 6.4, debe actualizar la versión de uber-jar a 6.4.0.

#### Componentes principales {#core-components}

El tipo de archivo del proyecto AEM, por supuesto, aprovecha los componentes principales.

Los componentes principales se instalan en AEM automáticamente en el modo de ejecución predeterminado y se utilizan en el sitio WKND de muestra. En un [modo de ejecución de producción](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`), los componentes principales no están disponibles.

Por lo tanto, para aprovechar los componentes principales en todas las implementaciones, se recomienda incluirlos como parte del proyecto Maven.

>[!NOTE]
>
>Cada versión de los componentes principales suele ir seguida de una versión del tipo de archivo del proyecto AEM, de modo que el arquetipo más reciente utilice la versión más reciente de los componentes principales.
>
>Sin embargo, es posible que una nueva versión del tipo de archivo no siga directamente a una nueva versión de los componentes principales, por lo que puede que desee actualizar la dependencia de los componentes principales a la versión más reciente.

>[!NOTE]
>
>core.wcm.components.samples es un conjunto de páginas de muestra que ilustran ejemplos de los componentes principales. Como práctica recomendada, al implementar un proyecto para su uso en producción debe eliminar esta dependencia y la inclusión de subpaquetes.

## Pruebas {#testing}

Existen tres niveles de prueba contenidos en el proyecto y, como son diferentes tipos de prueba, se ejecutan de diferentes maneras o en diferentes lugares.

* Prueba unitaria en el núcleo: Esto muestra la prueba de unidad clásica del código contenido en el paquete. Para probar, ejecute:
   * `mvn clean test`
* Pruebas de integración del lado del servidor: Estas pruebas unitarias se ejecutan en el entorno AEM, es decir, en el servidor AEM. Para probar, ejecute:
   * `mvn clean verify -PintegrationTests`
* Pruebas Hobbes.js del lado del cliente: Estas son pruebas del lado del explorador basadas en JavaScript que verifican el comportamiento del lado del explorador. Para probar:
   1. Cargue AEM en el explorador como lo haría para crear una página.
   1. Abra la página en [Developer mode](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Abra el panel izquierdo y cambie a la pestaña **Pruebas**.
   1. Busque las **MyName Tests** generadas y ejecútelas.

## Pasos siguientes {#next-steps}

Por lo tanto, ha creado e instalado el tipo de archivo del proyecto AEM. ¿Y ahora qué? Bueno, el arquetipo es pequeño, pero consiste en muchos ejemplos de potentes funciones de AEM configuradas según las mejores prácticas recomendadas. Utilice estos indicadores para indicar cómo puede aprovechar estas funciones en su proyecto. Para cualquier proyecto, probablemente necesite:

* [Personalizar componentes ampliando los componentes principales existentes](/help/developing/customizing.md)
* [Agregar plantillas adicionales](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adaptar la estructura de localización](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Obtenga información sobre el módulo de compilación del front-end](uifrontend.md)
