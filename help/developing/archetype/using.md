---
title: Uso del arquetipo del proyecto AEM
description: Instrucciones de uso detalladas para el arquetipo del proyecto AEM
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '2057'
ht-degree: 1%

---


# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El Arquetipo de proyecto AEM crea un proyecto de Adobe Experience Manager mínimo basado en optimizaciones como punto de partida para sus propios proyectos AEM. Las propiedades que se deben proporcionar al utilizar este arquetipo le permiten especificar los nombres de todas las partes de este proyecto, así como controlar determinadas funciones opcionales.

## Por qué usar el arquetipo {#why-use-the-archetype}

El uso del Arquetipo de proyecto AEM lo coloca en el camino hacia la construcción de un proyecto de AEM basado en optimizaciones con sólo unas pocas pulsaciones de tecla. Al usar el arquetipo, todas las piezas ya estarán en su lugar, de modo que mientras el proyecto resultante sea mínimo, ya implementará todas las [características clave](#what-you-get) de AEM para que todo lo que tenga que hacer sea construir en la parte superior y extender.

Por supuesto, hay muchos elementos que entran en un proyecto de AEM exitoso, pero el uso del arquetipo del proyecto AEM es una base sólida y se recomienda encarecidamente para cualquier proyecto AEM.

## Introducción {#getting-started}

El arquetipo del proyecto hace que sea fácil empezar a desarrollar en AEM. Puede dar sus primeros pasos de varias maneras.

* Tutorial de WKND: para obtener una buena introducción al desarrollo de AEM, incluida la forma de aprovechar el arquetipo, consulte el [Tutorial de introducción a AEM Sites - WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) para ver un ejemplo práctico que lo acompañará utilizando el arquetipo para implementar un proyecto sencillo.
* Tutorial de Eventos WKND: si le interesa especialmente el desarrollo de aplicaciones de una sola página (SPA) en AEM, asegúrese de consultar el tutorial [Eventos WKND](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html) dedicado.
* Descarga y inicio por su cuenta! - Puede descargar fácilmente el arquetipo de proyecto actual disponible en GitHub y crear su primer proyecto [siguiendo los sencillos pasos a continuación](#how-to-use-the-archetype).

## Qué se obtiene al usar el arquetipo {#what-you-get}

El arquetipo AEM está compuesto por módulos:

* **[núcleo](core.md)**: es un paquete Java que contiene toda la funcionalidad básica, como servicios OSGi, oyentes y Planificadoras, así como código Java relacionado con componentes, como servlets y filtros de solicitud.
* **[ui.apps](uiapps.md)**: contiene las  `/apps` y  `/etc` partes del proyecto, es decir, clientes de JS y CSS, componentes, plantillas, configuraciones específicas de runmode, así como pruebas de Hobbes.
* **[ui.content](uicontent.md)**: contiene contenido de muestra utilizando los componentes del módulo ui.apps.
* **[ui.testing](uitests.md)**: es un paquete Java que contiene pruebas JUnit que se ejecutan en el servidor. Este paquete no debe implementarse en producción.
* **ui.launcher**: contiene código de pegado que implementa el paquete ui.testing (y paquetes dependientes) en el servidor y activa la ejecución remota de JUnit.
* **[ui.front.general](uifrontend.md)**:  **(opcional)** contiene los artefactos necesarios para utilizar el módulo de compilación general basado en Webpack.
* **[ui.front.response](uifrontend-react.md)**:  **(opcional)** contiene los artefactos requeridos al utilizar el arquetipo para crear proyectos SPA basados en React.
* **[ui.front.angle](uifrontend-angular.md)**:  **(opcional)** contiene los artefactos necesarios al utilizar el arquetipo para crear proyectos SPA basados en Angular.

![](/help/assets/archetype-structure.png)

Los módulos de AEM Archetype representados en Maven se implementan en AEM como paquetes de contenido que representan la aplicación, el contenido y los paquetes OSGi necesarios.

## Cómo usar el arquetipo {#how-to-use-the-archetype}

Para utilizar el arquetipo, primero debe crear un proyecto que genere los módulos en una estructura de archivos local como [descrita anteriormente](#what-you-get). Como parte de la generación de proyectos, se pueden definir varias propiedades para el proyecto, como el nombre del proyecto, la versión, etc.

Al crear el proyecto con Maven se crean los artefactos (paquetes y paquetes OSGi) que se pueden implementar en AEM. Se pueden utilizar comandos y perfiles Maven adicionales para implementar los artefactos del proyecto en una instancia de AEM.

### Creación de un proyecto    {#create-project}

Para empezar, puede utilizar la [extensión Eclipse](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) de &lt;a0/>AEM y seguir el Asistente para nuevo proyecto y elegir **AEM Proyecto de Módulo múltiple de muestra** para utilizar una versión liberada del arquetipo.

Por supuesto también puede invocar Maven directamente.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Establezca `XX` en el [número de versión](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) del último arquetipo de proyecto de AEM.
* Configure `aemVersion=cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Configure `aemVersion=6.5.0` para [Servicios administrados de Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ.
La dependencia Componentes principales solo se agrega para las versiones que no son de nube, ya que los Componentes principales se proporcionan OOTB para AEM como nube
Servicio.
* Ajuste `appTitle="My Site"` para definir el título del sitio Web y los grupos de componentes.
* Ajuste `appId="mysite"` para definir Maven artifactsId, los nombres de los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de clientes.
* Ajuste `groupId="com.mysite"` para definir el groupId de Maven y el paquete de origen de Java.
* Busque la lista de propiedades disponibles para ver si hay más que desea ajustar.

>[!NOTE]
>
>Se recomienda agregar el perfil `adobe-public` a su archivo Maven `settings.xml` para agregar automáticamente repo.adobe.com al proceso de compilación.
>
>Aquí](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html) se puede encontrar un ejemplo de POM [.

### Propiedades {#properties}

Las siguientes propiedades están disponibles al crear un proyecto con el arquetipo.

| Nombre | Predeterminado | Descripción |
--------------------------|----------------|--------------------
| `appTitle` |  | El título de la aplicación se utilizará para el título del sitio web y los grupos de componentes (p. ej. `"My Site"`). |
| `appId` |  | El nombre técnico se utilizará para los nombres de los componentes, la configuración y las carpetas de contenido, así como los nombres de las bibliotecas de cliente (p. ej. `"mysite"`). |
| `artifactId` | *`${appId}`* | ID de artefacto de la mueble base (p. ej. `"mysite"`). |
| `groupId` |  | ID de grupo de Maven base (p. ej. `"com.mysite"`). |
| `package` | *`${groupId}`* | Paquete de fuentes Java (p. ej. `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Versión del proyecto (p. ej. `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Destinatario AEM versión (puede ser `cloud` para [AEM como Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html); o `6.5.0`, o `6.4.4` para [Servicios administrados de Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) o in situ). |
| `sdkVersion` | `latest` | Cuando `aemVersion=cloud` se puede especificar una versión [SDK](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) (p. ej. `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Incluye una configuración de distribuidor para cloud o para AMS/in situ, según el valor de `aemVersion` (puede ser `y` o `n`). |
| `frontendModule` | `none` | Incluye un módulo de compilación de front-end de Webpack que genera bibliotecas de cliente (puede ser `general` o `none` para sitios regulares; puede ser `angular` o `react` para una aplicación de una sola página que implemente el [Editor de SPA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/introduction.html)). |
| `languageCountry` | `en_us` | Idioma y código de país desde los que crear la estructura de contenido (p. ej. `en_us`). |
| `singleCountry` | `y` | Incluye una estructura de contenido maestro-idioma (puede ser `y` o `n`). |
| `includeExamples` | `y` | Incluye un sitio de ejemplo de [Biblioteca de componentes](https://www.aemcomponents.dev/) (puede ser `y` o `n`). |
| `includeErrorHandler` | `n` | Incluye una página de respuesta personalizada 404 que será global para toda la instancia (puede ser `y` o `n`). |

>[!NOTE]
>
> Si el arquetipo se ejecuta en modo interactivo la primera vez, no se pueden cambiar las propiedades con valores predeterminados (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obtener más información). El valor se puede cambiar cuando se deniega la confirmación de la propiedad al final y se repite el cuestionario, o pasando el parámetro en la línea de comandos (p. ej. `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Cuando se ejecuta en Windows y se genera la configuración del despachante, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte [número 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfiles {#profiles}

El proyecto principal generado admite diferentes perfiles de implementación al ejecutar `mvn install`.

| ID de perfil | Descripción |
--------------------------|------------------------------
| `autoInstallBundle` | Monte el paquete principal con el complemento maven-sling en la consola felix |
| `autoInstallPackage` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin en el administrador de paquetes para la instancia de creación predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallPackagePublish` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin en el administrador de paquetes para publicar la instancia predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallSinglePackage` | Instale el paquete de contenido `all` con el complemento content-package-maven-plugin en el administrador de paquetes para la instancia de creación predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `autoInstallSinglePackagePublish` | Instale el paquete de contenido `all` con el complemento content-package-maven-plugin en el administrador de paquetes para la instancia de publicación predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y `aem.port`. |
| `integrationTests` | Ejecuta las pruebas de integración proporcionadas en la instancia de AEM (solo para la fase `verify`) |

### Generación e instalación {#building-and-installing}

Para generar todos los módulos ejecutados en el directorio raíz del proyecto, utilice el siguiente comando Maven.

```
mvn clean install
```

Si tiene una instancia de AEM en ejecución, puede compilar y empaquetar todo el proyecto e implementarlo en AEM con el siguiente comando Maven.

```
mvn clean install -PautoInstallPackage
```

Para implementarlo en una instancia de publicación, ejecute este comando.

```
mvn clean install -PautoInstallPackagePublish
```

Como alternativa, para implementar en una instancia de publicación, ejecute este comando.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

O bien, para implementar únicamente el paquete para el autor, ejecute este comando.

```
mvn clean install -PautoInstallBundle
```

## POM principal {#parent-pom}

El `pom.xml` en la raíz del proyecto (`<src-directory>/<project>/pom.xml`) se conoce como POM principal y dirige la estructura del proyecto, así como administra dependencias y ciertas propiedades globales del proyecto.

### Propiedades del proyecto global {#global-properties}

La sección `<properties>` del POM principal define varias propiedades globales que son importantes para la implementación del proyecto en una instancia de AEM, como nombre de usuario/contraseña, nombre de host/puerto, etc.

Estas propiedades están configuradas para implementarse en una instancia de AEM local, ya que ésta es la compilación más común que los desarrolladores van a realizar. Tenga en cuenta que hay propiedades que implementar en una instancia de autor, así como en una instancia de publicación. Aquí también se establecen las credenciales para autenticarse con la instancia de AEM. Se utilizan las credenciales predeterminadas admin:admin.

Estas propiedades se configuran para que se puedan anular al implementar en entornos de nivel superior. De este modo, los archivos POM no tienen que cambiar, pero las variables como `aem.host` y `sling.password` pueden reemplazarse mediante argumentos de línea de comandos:

```
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estructura del módulo {#module-structure}

La sección `<modules>` del POM principal define los módulos que el proyecto generará. De forma predeterminada, el proyecto genera [los módulos estándar definidos anteriormente](#what-you-get): core, ui.apps, ui.content, ui.testing y it.launcher. Siempre se pueden añadir más módulos a medida que evoluciona un proyecto.

### Dependencias {#dependencies}

La sección `<dependencyManagement>` del POM principal define todas las dependencias y versiones de las API que se utilizan en el proyecto. Las versiones se deben administrar en el POM principal. Los submódulos como core y ui.apps no deben incluir información de la versión.

#### Uber-Jar {#uber-jar}

Una de las dependencias clave es el [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Esto incluirá todas las API AEM con una sola entrada de dependencia para la versión de AEM.

>[!NOTE]
>
>Se recomienda actualizar la versión de suber-jar para que coincida con la versión de destinatario de AEM. Por ejemplo, si planea implementar en AEM 6.4, debe actualizar la versión de uber-jar a 6.4.0.

#### Componentes principales {#core-components}

Por supuesto, el arquetipo del proyecto AEM aprovecha los componentes principales.

Los componentes principales se instalan en AEM automáticamente en el modo de ejecución predeterminado y se utilizan en el sitio WKND de muestra. En un [modo de ejecución de producción](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) los componentes principales no están disponibles.

Por lo tanto, para aprovechar los componentes principales en todas las implementaciones, es recomendable incluirlos como parte del proyecto Maven.

>[!NOTE]
>
>Cada versión de los componentes principales suele ir seguida de una versión del arquetipo del proyecto AEM, de modo que el arquetipo más reciente utiliza la versión más reciente de los componentes principales.
>
>Sin embargo, es posible que una nueva versión del arquetipo no siga directamente a una nueva versión de los componentes principales, por lo que puede que desee actualizar la dependencia de los componentes principales a la última versión.

>[!NOTE]
>
>core.wcm.components.samples es un conjunto de páginas de muestra que ilustran ejemplos de los componentes principales. Se recomienda eliminar esta dependencia y la inclusión de subpaquetes al implementar un proyecto para producción.

## Pruebas {#testing}

Hay tres niveles de prueba contenidos en el proyecto y, como son diferentes tipos de pruebas, se ejecutan de diferentes maneras o en diferentes lugares.

* Prueba unitaria en el núcleo: Esto muestra las pruebas de unidades clásicas del código incluido en el paquete. Para realizar la prueba, ejecute:
   * `mvn clean test`
* Pruebas de integración del lado del servidor: Estas pruebas unitarias se ejecutan en el entorno de AEM, es decir, en el servidor AEM. Para realizar la prueba, ejecute:
   * `mvn clean verify -PintegrationTests`
* Pruebas de Hobbes.js del lado del cliente: Son pruebas basadas en JavaScript en el navegador que verifican el comportamiento en el navegador. Para probar:
   1. Cargue AEM en el explorador como lo haría para crear una página.
   1. Abra la página en [modo de desarrollador](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Abra el panel izquierdo y cambie a la ficha **Pruebas**.
   1. Busque las **pruebas MyName** generadas y ejecútelas.

## Próximos pasos {#next-steps}

Así que han construido e instalado el Arquetipo del Proyecto AEM. ¿Y ahora qué? Bueno, el arquetipo es pequeño, pero consiste en muchos ejemplos de poderosas características de AEM configuradas según las mejores prácticas recomendadas. Estas funciones indican cómo puede aprovechar estas funciones en el proyecto. Para cualquier proyecto que necesite:

* [Personalice los componentes ampliando los componentes principales existentes](/help/developing/customizing.md)
* [Añadir plantillas adicionales](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adaptar la estructura de localización](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Obtenga información sobre el módulo de compilación front-end](uifrontend.md)
