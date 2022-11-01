---
title: Complemento Build Analyzer de Maven del SDK de AEM as a Cloud Service
description: Documentación del complemento Build Analyzer local de Maven
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: be66739084334120158eda96b830a7b6216ef5cd
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 97%

---

# Complemento Build Analyzer de Maven del SDK de AEM as a Cloud Service {#maven-analyzer-plugin}

El complemento Build Analyzer de Maven del SDK de AEM as a Cloud Service analiza la estructura de los distintos proyectos de paquetes de contenido.

Consulte la [documentación del complemento de Maven](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) para obtener información sobre cómo incluirlo en un proyecto de Maven en AEM.

>[!NOTE]
>
>Se recomienda actualizar el proyecto Maven para que haga referencia a la última versión del complemento que se encuentra en el repositorio central de Maven, en esta ubicación: https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

El complemento utiliza el SDK disponible más reciente que el configurado en el proyecto.

A continuación se muestra una tabla que describe los analizadores que se ejecutan como parte de este paso. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Módulo | Función, ejemplo y resolución de problemas | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Comprueba si todos los paquetes OSGI tienen sus declaraciones Import-Package satisfechas con la declaración Export-package de otros paquetes incluidos en el proyecto Maven. Un error tendría este aspecto: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Para solucionar el problema, consulte si el paquete que proporciona el paquete está incluido en la implementación o, alternativamente, observe el manifiesto del paquete que espera exportar para determinar si se ha utilizado un nombre o una verisón que no son correctos. | Sí | Sí |
| `requirements-capabilities` | Comprueba si todas las declaraciones de requisitos realizadas en paquetes OSGI se cumplen con las declaraciones de capacidades de otros paquetes incluidos en el proyecto Maven. Un error tendría este aspecto: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Para solucionar el problema, observe el manifiesto del paquete que esperaría declarar una capacidad para determinar por qué falta, o compruebe el manifiesto del paquete que requiere para ver que el requisito en ahí es correcto. | Sí | Sí |
| `bundle-content` | Envía una advertencia si un paquete contiene contenido inicial especificado con Sling-Initial-Content, lo que resulta problemático en el AEM como entorno agrupado de Cloud Service. La advertencia tiene este aspecto: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Para solucionar problemas al convertir el contenido inicial en instrucciones repoinit, consulte la documentación de Repoinit. | Sí | Sí |
| `bundle-resources` | Envía una advertencia si un paquete contiene recursos especificados con el encabezado Sling-Bundle-Resources, lo que resulta problemático en el entorno agrupado de AEM as a Cloud Service. La advertencia tiene este aspecto:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Para solucionar problemas al convertir los recursos a instrucciones Repoinit, consulte [Documentación de Repoinit](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#repo-init). | Sí | Sí |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Estos analizadores comprueban algunos detalles relacionados con el [paquete de contenido para el proceso de conversión del modelo de funciones](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=es) que crea artefactos que se ajustan al Modelo de funciones de Sling. Cualquier error debe notificarse al Servicio de atención al cliente de Adobe. | Sí | Sí |
| `api-regions-crossfeature-dups` | Valida que los paquetes OSGI del cliente no tengan declaraciones de paquete de exportación que anulen la API pública de AEM as a Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Para solucionarlo, deje de exportar un paquete que forme parte de la API pública de AEM. | Sí | Sí |
| `repoinit` | Comprueba la sintaxis de todas las secciones de repoinit | Sí | Sí |
| `bundle-nativecode` | Valida que los paquetes OSGI no instalen código nativo. | Sí | Sí |
| `configuration-api` | Valida configuraciones importantes de OSGi. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Sí | Sí |
| `region-deprecated-api` | Comprueba si se utiliza una [API obsoleta](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html?lang=es) <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Sí | Sí |
| `artifact-rules` | Valida dependencias como paquetes y paquetes de contenido para evitar problemas conocidos con artefactos.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Sí | Sí |
| `aem-env-var` | Comprueba el uso de eVars según la variable [guía de nomenclatura de variables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#variable-naming)<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | Sí | Sí |
| `content-package-validation` | Ejecuta los validadores de filevault. De forma predeterminada, jackrabbit-docviewparser está habilitado, así que comprueba la sintaxis de contenido bien formada del xml en los paquetes que se instalarán durante la implementación.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>Como solución, compruebe si hay problemas con xml en el archivo denominado por el analizador. | Sí | Sí |

{style=&quot;table-layout:auto&quot;}

## Problemas conocidos

A continuación, se muestra una lista de problemas conocidos al utilizar el complemento Maven de Build Analyzer.

### No se ha podido ejecutar el complemento Maven de Build Analyzer en el SDK local

Cuando se utiliza el SDK local con una versión del complemento Maven de Build Analyzer inferior a `1.1.2`, la ejecución del complemento puede provocar el siguiente error. En este caso, actualice el proyecto a la última versión del complemento.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

Si ha utilizado el tipo de archivo del proyecto de AEM para configurar el proyecto, asegúrese de ajustar la propiedad en el Maven raíz `pom.xml` como se muestra a continuación.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
