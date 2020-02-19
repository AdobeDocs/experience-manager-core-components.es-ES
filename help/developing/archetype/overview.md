---
title: Tipo de archivo del proyecto AEM
description: Una plantilla de proyecto para aplicaciones basadas en AEM
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El arquetipo de proyecto de AEM crea un proyecto de Adobe Experience Manager mínimo basado en las prácticas recomendadas como punto de partida para sus propios proyectos de AEM. Las propiedades que se deben proporcionar al utilizar este arquetipo le permiten especificar los nombres de todas las partes de este proyecto, así como controlar determinadas funciones opcionales.

>[!TIP]
>
>El último arquetipo de proyecto de AEM [se encuentra en GitHub](https://github.com/adobe/aem-project-archetype).

## Características {#features}

El arquetipo tiene varias funciones que están pensadas para ofrecer un punto de partida conveniente para nuevos proyectos de AEM:

* Páginas en inglés y francés con contenido de ejemplo
* Plantilla de contenido basada en la función de plantilla editable con política de contenido de ejemplo
* Componente de página basado en el componente principal de página de [AEM](/help/components/page.md)
* Ejemplos de componentes de contenido implementados con el patrón de proxy recomendado y un componente personalizado de ejemplo de ayuda basado en componentes [principales de](/help/introduction.md)AEM.
* Ejemplos de componentes de [formulario](/help/components/forms/form-container.md)
* Configuraciones para emuladores de dispositivos, configuración de arrastrar y soltar e internacionalización
* Bibliotecas de clientes que siguen las convenciones de nomenclatura de BEM, así como estilos específicos de componentes
* Ejemplos de paquetes, incluidos modelos de muestra, servelets, filtros y programadores
* Pruebas de unidad, integración y lado del cliente
* Implementaciones de SPA de muestra en React o Angular (opcional)

## ¿Por qué usar el arquetipo? {#why-use-the-archetype}

El uso del arquetipo de proyecto de AEM le permite avanzar hacia la creación de un proyecto de AEM basado en las prácticas recomendadas con solo unas pocas pulsaciones de tecla. Mediante el uso del arquetipo, todas las piezas ya estarán en su lugar, de modo que mientras el proyecto resultante sea mínimo, ya implementará todas las funciones [](#features) clave de AEM para que todo lo que tenga que hacer sea construir en la parte superior y extender.

Por supuesto, hay muchos elementos que entran en un proyecto AEM exitoso, pero el uso del arquetipo de proyecto AEM es una base sólida y se recomienda encarecidamente para cualquier proyecto AEM.

## Introducción {#getting-started}

El arquetipo del proyecto facilita el inicio del desarrollo en AEM. Puede dar sus primeros pasos de varias maneras.

* Tutorial de WKND: para obtener una excelente introducción al desarrollo de AEM, incluida la forma de aprovechar el arquetipo, consulte el tutorial [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) de WKND Getting Started with AEM Sites (Introducción a los sitios de AEM), donde encontrará un ejemplo práctico de cómo utilizar el arquetipo para implementar un proyecto sencillo.
* Tutorial de eventos WKND: si está especialmente interesado en el desarrollo de aplicaciones de una sola página (SPA) en AEM, asegúrese de consultar el tutorial [dedicado de eventos](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)WKND.
* Descárguelo y comience por su cuenta. - Puede descargar fácilmente el arquetipo de proyecto actual disponible en GitHub y crear su primer proyecto [siguiendo los sencillos pasos a continuación](#how-to-use-the-archetype).

## Qué se obtiene usando el arquetipo {#what-you-get}

El arquetipo de AEM está compuesto de módulos:

* **[núcleo](core.md)**: es un paquete Java que contiene toda la funcionalidad básica, como servicios OSGi, oyentes y programadores, así como código Java relacionado con componentes, como servlets y filtros de solicitud.
* **[ui.apps](uiapps.md)**: contiene las partes`/apps`y`/etc`partes del proyecto, es decir, clientes de JS y CSS, componentes, plantillas, configuraciones específicas de runmode, así como pruebas de Hobbes.
* **[ui.content](uicontent.md)**: contiene contenido de muestra utilizando los componentes del módulo ui.apps.
* **[ui.testing](uitests.md)**: es un paquete Java que contiene pruebas JUnit que se ejecutan en el servidor. Este paquete no debe implementarse en producción.
* **ui.launcher**: contiene código de pegado que implementa el paquete ui.testing (y paquetes dependientes) en el servidor y activa la ejecución remota de JUnit.
* **[ui.front.general](uifrontend.md)**:**(opcional)**contiene los artefactos necesarios para utilizar el módulo de compilación general basado en Webpack.
* **[ui.front.response](uifrontend-react.md)**:**(opcional)**contiene los artefactos necesarios al utilizar el arquetipo para crear proyectos de SPA basados en React.
* **[ui.front.angle](uifrontend-angular.md)**:**(opcional)**contiene los artefactos necesarios al utilizar el arquetipo para crear proyectos de SPA basados en Angular.

![](/help/assets/archetype-structure.png)

Los módulos de AEM Archetype representados en Maven se implementan en AEM como paquetes de contenido que representan la aplicación, el contenido y los paquetes OSGi necesarios.

## Requisitos {#requirements}

La versión actual del arquetipo tiene los siguientes requisitos:

* Adobe Experience Manager 6.3.3.0 o superior (6.4.2 o superior al generar un proyecto con las opciones de compilación Angular o React) o [AEM como servicio de nube](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)
* Apache Maven (3.3.9 o posterior)
* Repositorio público de Adobe Maven en la configuración de Maven. Consulte este artículo [de la Base de conocimiento para obtener más detalles](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

Para obtener una lista de las versiones compatibles de AEM de versiones anteriores de arquetipos, consulte las versiones [](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md)históricas de AEM admitidas.

## Cómo usar el arquetipo {#how-to-use-the-archetype}

Para utilizar el arquetipo, primero debe crear un proyecto, que genere los módulos en una estructura de archivos local como se [describió](#what-you-get)anteriormente. Como parte de la generación de proyectos, se pueden definir varias propiedades para el proyecto, como el nombre del proyecto, la versión, etc.

Al crear el proyecto con Maven se crean los artefactos (paquetes y paquetes OSGi) que se pueden implementar en AEM. Se pueden utilizar comandos y perfiles Maven adicionales para implementar los artefactos del proyecto en una instancia de AEM.

### Creación de un proyecto {#create-project}

Para empezar, puede simplemente utilizar la extensión [Eclipse de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) AEM y seguir el Asistente para nuevo proyecto y elegir Proyecto **multimódulo de muestra de** AEM para utilizar una versión publicada del arquetipo.

Por supuesto también puede invocar Maven directamente.

```
mvn archetype:generate \
 -DarchetypeGroupId=com.adobe.granite.archetypes \
 -DarchetypeArtifactId=aem-project-archetype \
 -DarchetypeVersion=XX
```

Dónde `XX` es el número [de](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) versión del último arquetipo de proyecto de AEM.

>[!NOTE]
>
>Se recomienda agregar el `adobe-public` perfil al archivo Maven `settings.xml` para agregar automáticamente repo.adobe.com al proceso de generación de lotes.
>
>Aquí [se](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html)puede encontrar un ejemplo de POM.

### Propiedades {#properties}

Las siguientes propiedades están disponibles al crear un proyecto con el arquetipo.

| Nombre | Predeterminado | Descripción |
----------------------------|---------|--------------------
| `groupId` |  | Maven base `groupId` |
| `artifactId` |  | Id. de artefacto de la curva base |
| `version` |  | Versión |
| `package` |  | Paquete de código fuente Java |
| `appID` |  | ID de aplicación utilizado para carpetas de componentes, configuración y contenido e ID de css |
| `appTitle` |  | Título de aplicación utilizado para los grupos de componentes y título del sitio web |
| `aemVersion` | 6.5.0 | Versión de AEM de Target |
| `sdkVersion` |  |
| `languageCountry` | en_us | Idioma y código de país para crear la estructura de contenido localizado (p. ej. `en_us`) |
| `includeExamples` | y | Incluir un sitio de ejemplo de la biblioteca de componentes |
| `includeErrorHandler` | n | Incluir una página de respuesta personalizada 404 |
| `frontendModule` | ninguno | Incluir un módulo de front-end dedicado (uno de `none`, [`general`](uifrontend.md), [`angular`](uifrontend-angular.md), [`react`](uifrontend-react.md)) |
| `singleCountry` | y | Crear una estructura de idioma-maestro en contenido de ejemplo |
| `includeDispatcherConfig` | n | Define si se genera una configuración de despachante para el proyecto <br> Definir en [`cloud`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.cloud) al crear un proyecto para [AEM como un servicio](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) de nube <br> Definir en [`ams`](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) al crear un proyecto para los servicios gestionados de Adobe |

>[!NOTE]
> Si el arquetipo se ejecuta en modo interactivo la primera vez, no se pueden cambiar las propiedades con valores predeterminados (consulte [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) para obtener más información). El valor se puede cambiar cuando se deniega la confirmación de la propiedad al final y se repite el cuestionario, o pasando el parámetro en la línea de comandos (p. ej. `-DoptionIncludeExamples=n`).

>[!NOTE]
>Cuando se ejecuta en Windows y se genera la configuración del despachante, debe estar ejecutando un símbolo del sistema elevado o el Subsistema de Windows para Linux (consulte el [problema 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Perfiles {#profiles}

El proyecto principal generado admite distintos perfiles de implementación al ejecutarse `mvn install`.

| ID de perfil | Descripción |
--------------------------|------------------------------
| `autoInstallBundle` | Monte el paquete principal con el complemento maven-sling en la consola felix |
| `autoInstallPackage` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin en el administrador de paquetes para la instancia de creación predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y el `aem.port` usuario. |
| `autoInstallPackagePublish` | Instale el paquete de contenido ui.content y ui.apps con el complemento content-package-maven-plugin en el administrador de paquetes para publicar la instancia predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y el `aem.port` usuario. |
| `autoInstallSinglePackage` | Instale el paquete de `all` contenido con el content-package-maven-plugin en el administrador de paquetes para la instancia de creación predeterminada en localhost, puerto 4502. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y el `aem.port` usuario. |
| `autoInstallSinglePackagePublish` | Instale el paquete de `all` contenido con el complemento content-package-maven-plugin en el administrador de paquetes para publicar la instancia predeterminada en localhost, puerto 4503. El nombre de host y el puerto se pueden cambiar con las propiedades definidas por el usuario `aem.host` y el `aem.port` usuario. |
| `integrationTests` | Ejecuta las pruebas de integración proporcionadas en la instancia de AEM (solo para la `verify` fase) |

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

El `pom.xml` en la raíz del proyecto (`<src-directory>/<project>/pom.xml`) se conoce como POM principal y dirige la estructura del proyecto, además de administrar dependencias y ciertas propiedades globales del proyecto.

### Propiedades del proyecto global {#global-properties}

La `<properties>` sección del POM principal define varias propiedades globales que son importantes para la implementación del proyecto en una instancia de AEM, como nombre de usuario/contraseña, nombre de host/puerto, etc.

Estas propiedades están configuradas para implementarse en una instancia de AEM local, ya que esta es la compilación más común que los desarrolladores van a realizar. Tenga en cuenta que hay propiedades que implementar en una instancia de autor, así como en una instancia de publicación. Aquí también se establecen las credenciales para la autenticación con la instancia de AEM. Se utilizan las credenciales predeterminadas admin:admin.

Estas propiedades se configuran para que se puedan anular al implementarlas en entornos de nivel superior. De este modo, los archivos POM no tienen que cambiar, pero las variables como `aem.host` y se pueden anular `sling.password` mediante argumentos de la línea de comandos:

````
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
````

### Estructura del módulo {#module-structure}

La `<modules>` sección del POM principal define los módulos que el proyecto creará. De forma predeterminada, el proyecto crea [los módulos estándar definidos](#what-you-get)anteriormente: core, ui.apps, ui.content, ui.testing y it.launcher. Siempre se pueden añadir más módulos a medida que evoluciona un proyecto.

### Dependencias {#dependencies}

La `<dependencyManagement>` sección del POM principal define todas las dependencias y versiones de las API que se utilizan en el proyecto. Las versiones se deben administrar en el POM principal. Los submódulos como core y ui.apps no deben incluir información de la versión.

#### Uber-Jar {#uber-jar}

Una de las dependencias clave es el subjar [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies)AEM. Esto incluirá todas las API de AEM con una sola entrada de dependencia para la versión de AEM.

>[!NOTE]
>
>La práctica recomendada es actualizar la versión de subar-jar para que coincida con la versión de destino de AEM. Por ejemplo, si planea implementar en AEM 6.4, debe actualizar la versión de uber-jar a 6.4.0.

#### Componentes principales {#core-components}

Por supuesto, el arquetipo del proyecto de AEM aprovecha los componentes principales.

Los componentes principales se instalan automáticamente en AEM en el modo de ejecución predeterminado y se utilizan en el sitio de muestra de We.Retail. En un modo [de ejecución](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) de producción (`nosamplecontent`), los componentes principales no están disponibles.

Por lo tanto, para aprovechar los componentes principales en todas las implementaciones, es recomendable incluirlos como parte del proyecto Maven.

>[!NOTE]
>
>Cada versión de los componentes principales suele ir seguida de una versión del arquetipo de proyecto de AEM, de modo que el arquetipo más reciente utiliza la versión más reciente de los componentes principales.
>
>Sin embargo, es posible que una nueva versión del arquetipo no siga directamente a una nueva versión de los componentes principales, por lo que puede que desee actualizar la dependencia de los componentes principales a la última versión.

>[!NOTE]
>
>core.wcm.components.samples es un conjunto de páginas de muestra que ilustran ejemplos de los componentes principales. Se recomienda eliminar esta dependencia y la inclusión de subpaquetes al implementar un proyecto para producción.

## Pruebas {#testing}

Hay tres niveles de prueba contenidos en el proyecto y, como son diferentes tipos de pruebas, se ejecutan de diferentes maneras o en diferentes lugares.

* Prueba unitaria en el núcleo: Esto muestra las pruebas de unidades clásicas del código incluido en el paquete. Para realizar la prueba, ejecute:
   * `mvn clean test`
* Pruebas de integración del lado del servidor: Estas pruebas unitarias se ejecutan en el entorno AEM, es decir, en el servidor AEM. Para realizar la prueba, ejecute:
   * `mvn clean verify -PintegrationTests`
* Pruebas de Hobbes.js del lado del cliente: Son pruebas basadas en JavaScript en el navegador que verifican el comportamiento en el navegador. Para probar:
   1. Cargue AEM en el navegador como lo haría para crear una página.
   1. Open the page in [Developer mode](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Abra el panel izquierdo y cambie a la ficha **Pruebas** .
   1. Busque las pruebas **** MyName generadas y ejecútelas.

## Próximos pasos {#next-steps}

Así que ha creado e instalado el Arquetipo de proyecto de AEM. ¿Y ahora qué? Bueno, el arquetipo es pequeño, pero consta de muchos ejemplos de potentes funciones de AEM configuradas según las optimizaciones recomendadas. Estas funciones indican cómo puede aprovechar estas funciones en el proyecto. Para cualquier proyecto que necesite:

* [Personalice los componentes ampliando los componentes principales existentes](/help/developing/customizing.md)
* [Agregar plantillas adicionales](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [Adaptar la estructura de localización](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Obtenga información sobre el módulo de compilación front-end](uifrontend.md)
