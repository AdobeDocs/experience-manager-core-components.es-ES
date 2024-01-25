---
title: Uso del tipo de archivo del proyecto de AEM
description: AEM Aprenda a utilizar el tipo de archivo del proyecto de para crear un proyecto de Adobe Experience Manager AEM mínimo basado en las prácticas recomendadas como punto de partida para sus propios proyectos de.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 33%

---


# Uso del tipo de archivo del proyecto de AEM {#using-the-archetype}

AEM En este documento se explica cómo puede utilizar el tipo de archivo del proyecto de para crear un proyecto de Adobe Experience Manager AEM mínimo basado en las prácticas recomendadas como punto de partida para sus propios proyectos de.

Se centra en los patrones de uso generales y en lo que el tipo de archivo hace por usted. Para obtener opciones de compilación detalladas e instrucciones técnicas, consulte la documentación en el repositorio de GitHub del tipo de archivo.

>[!TIP]
>
>AEM El último tipo de archivo del proyecto de y la documentación técnica asociada [se encuentra en GitHub.](https://github.com/adobe/aem-project-archetype)

## Introducción {#getting-started}

El tipo de archivo del proyecto facilita el inicio del desarrollo en AEM. Puede realizar sus primeros pasos con el tipo de archivo de varias formas.

* **Tutorial de WKND** AEM - Para obtener una buena introducción al desarrollo de la, incluido cómo aprovechar el tipo de archivo, consulte la [Introducción a AEM Sites: Tutorial de WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es) para ver un ejemplo práctico que le guíe a través del uso del tipo de archivo para implementar un proyecto simple.
* **Tutorial de eventos WKND** SPA AEM - Si usted está especialmente interesado en el desarrollo de aplicaciones de una sola página () en la, asegúrese de echar un vistazo dedicado [Tutorial de eventos WKND.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es)
* **¡Empieza por tu cuenta!** - Puede descargar fácilmente el [arquetipo de proyecto actual disponible en GitHub](https://github.com/adobe/aem-project-archetype) y cree su primer proyecto por su cuenta.

## Cómo usar el tipo de archivo {#how-to-use-the-archetype}

El primer paso con el tipo de archivo es crear un proyecto, que genere [los módulos](#what-you-get) en una estructura de archivos local. Como parte de la generación de proyectos, se pueden definir varias propiedades para el proyecto, como el nombre del proyecto, la versión, la activación de varias opciones, etc.

>[!TIP]
>
>Siempre que genere el tipo de archivo, también generará una serie de léame, lo que le proporcionará los detalles técnicos y el uso de cada módulo como [enlazado a continuación.](#what-you-get)

Al crear el proyecto con Maven, se crearán los artefactos (paquetes y paquetes OSGi) que se puedan implementar en AEM. Se pueden utilizar comandos y perfiles adicionales de Maven para implementar los artefactos del proyecto en una instancia de AEM.

## Qué obtiene utilizando el tipo de archivo {#what-you-get}

El tipo de archivo está formado por módulos, todos los cuales se crean automáticamente al utilizar el tipo de archivo.

* **[núcleo](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** es un paquete Java que contiene todas las funcionalidades principales como servicios OSGi, oyentes y programadores, así como código Java relacionado con componentes como servlets y filtros de solicitud.
* **[it.testing](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** son pruebas de integración basadas en Java.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** contiene el `/apps` y `/etc` partes del proyecto, es decir, clientlibs, componentes y plantillas de JS y CSS.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** contiene contenido de muestra mediante los componentes del módulo ui.apps.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** contiene configuraciones OSGi específicas del modo de ejecución para el proyecto.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** contiene los artefactos necesarios para utilizar el módulo de versión del front-end general basado en Webpack (opcional).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(opcional)** SPA contiene los artefactos necesarios al utilizar el tipo de archivo para crear un proyecto de tipo de archivo basado en React (opcional, depende de los parámetros de compilación).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(opcional)** SPA contiene los artefactos necesarios al utilizar el tipo de archivo para crear un proyecto de creación de proyectos basado en el Angular (opcional, depende de los parámetros de generación).
* **[ui.testing](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** contiene pruebas de IU basadas en Selenium.
* **[todo](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** es un paquete de contenido único que incrusta todos los módulos compilados (paquetes y paquetes de contenido), incluidas las dependencias del proveedor.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** contiene las configuraciones básicas de Dispatcher para proyectos AMS/locales (opcional, depende de los parámetros de compilación).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** contiene las configuraciones básicas de Dispatcher para proyectos AEMaaCS (opcional, depende de los parámetros de compilación).

![Organización del paquete de contenido](/help/assets/content-package-organization.png)

AEM Los módulos del tipo de archivo representados en Maven se implementan como paquetes de contenido que representan la aplicación, el contenido y los paquetes OSGi necesarios.

## POM principal {#parent-pom}

El `pom.xml` en la raíz del proyecto (`<src-directory>/<project>/pom.xml`) se conoce como el POM principal y controla la estructura del proyecto y administra dependencias y ciertas propiedades globales del proyecto.

### Propiedades globales de proyecto {#global-properties}

La sección `<properties>` del POM principal define varias propiedades globales que son importantes para la implementación del proyecto en una instancia de AEM, como nombre de usuario/contraseña, nombre de host/puerto, etc.

Estas propiedades están configuradas para implementarse en una instancia de AEM local, ya que esta es la versión más común que realizan los desarrolladores. Tenga en cuenta que hay propiedades para implementar en una instancia de autor, así como una instancia de publicación. También es allí donde las credenciales están configuradas para autenticarse con la instancia de AEM. El valor predeterminado `admin:admin` se utilizan credenciales de.

Estas propiedades se configuran para que se puedan sobrescribir al implementarlas en entornos de nivel superior. De este modo, los archivos POM no tienen que cambiar, pero las variables como `aem.host` y `sling.password` pueden anularse mediante argumentos de línea de comandos:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Estructura del módulo {#module-structure}

La sección `<modules>` del POM principal define los módulos que creará el proyecto. De forma predeterminada, el proyecto se genera [los módulos estándar definidos previamente.](#what-you-get) Siempre se pueden añadir más módulos a medida que evoluciona un proyecto.

### Dependencias {#dependencies}

La sección `<dependencyManagement>` del POM principal define todas las dependencias y versiones de API que se utilizan en el proyecto. Las versiones deben administrarse en el POM principal. Los submódulos no deben incluir información sobre la versión.

#### Uber-Jar {#uber-jar}

Una de las dependencias clave es la [AEM Jar de API de Java de.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=es) AEM AEM Esto incluirá todas las API de con solo una entrada de dependencia para la versión de la aplicación de.

>[!NOTE]
>
>Se recomienda actualizar la versión de uber-jar para que coincida con la versión de destino de AEM. AEM Por ejemplo, si planea implementar en la versión 6.5, debe actualizar la versión de uber-jar a la versión 6.5.X, donde `X` es el Service Pack más reciente.

#### Componentes principales {#core-components}

El arquetipo, por supuesto, aprovecha [Componentes principales.](/help/introduction.md) Por lo tanto, para aprovechar los componentes principales en todas las implementaciones, se recomienda incluirlos como parte del proyecto Maven.

core.wcm.components.samples es un conjunto de páginas de muestra que ilustran ejemplos de los componentes principales. Como práctica recomendada, al implementar un proyecto para su uso en producción debe eliminar esta dependencia y la inclusión de subpaquetes.

>[!NOTE]
>
>Los componentes principales y el tipo de archivo se mantienen como proyectos de GitHub independientes y, como tales, sus versiones difieren.
>
>Cada versión del tipo de archivo utilizará la última versión de los componentes principales disponibles en el momento de la versión. Sin embargo, es posible que desee actualizar la dependencia de los componentes principales manualmente.

## Pruebas {#testing}

Existen tres niveles de prueba en el proyecto y, como son diferentes tipos de prueba, se ejecutan de diferentes formas o en diferentes lugares.

* **[Pruebas unitarias](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Prueba de unidad clásica del código contenido en el paquete
* **[Pruebas de integración](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** AEM AEM - Pruebas de integración del lado del servidor que ejecutan pruebas unitarias en el entorno de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la, es decir, en el servidor de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad de la unidad
* **[Pruebas de IU](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Pruebas del lado del explorador basadas en Selenium que verifican el comportamiento del lado del explorador
