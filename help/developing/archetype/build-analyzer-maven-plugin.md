---
title: AEM como Cloud Service SDK Build Analyzer Maven Plugin
description: Documentación para el complemento de analizador de Maven build local
translation-type: tm+mt
source-git-commit: b95515dba74486add7f50bc8984f4358090e735c
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---


# AEM como Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

El AEM como Cloud Service SDK Build Analyzer Maven Plugin analiza la estructura de los distintos proyectos de paquetes de contenido.

Consulte la documentación [del](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) complemento Maven para obtener información sobre cómo incluirlo en un proyecto AEM.

A continuación se muestra una tabla que describe los analizadores que se ejecutan como parte de este paso. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Módulo | Función, ejemplo y resolución de problemas | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Comprueba si todos los paquetes OSGI tienen sus declaraciones Import-Package satisfechas con la declaración Export-package de otros paquetes incluidos en el proyecto Maven. Un error sería el siguiente: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Para solucionar problemas, compruebe si el paquete que proporciona el paquete está incluido en la implementación o, si lo desea, consulte el manifiesto del paquete que espera exportar para determinar si se ha utilizado un nombre incorrecto o una versión incorrecta. | Sí | Sí |
| `requirements-capabilities` | Comprueba si todas las declaraciones de requisitos realizadas en los paquetes OSGI se cumplen con las declaraciones de capacidades de otros paquetes incluidos en el proyecto Maven. Un error sería el siguiente: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Para solucionar el problema, observe el manifiesto del paquete que espera que declare una capacidad para determinar por qué falta, o compruebe el manifiesto del paquete que requiere para ver que el requisito en él es correcto. | Sí | Sí |
| `bundle-content` | Proporciona una advertencia si un paquete contiene contenido inicial especificado con Sling-Initial-Content, lo que resulta problemático en el AEM como entorno agrupado de Cloud Service. La advertencia tiene este aspecto: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Para solucionar problemas al convertir el contenido inicial en sentencias de informe, consulte Documentación de informe. | Sí | Sí |
| `bundle-resources` | Proporciona una advertencia si un paquete contiene recursos especificados con el encabezado Sling-Bundle-Resources, lo que resulta problemático en el AEM como entorno agrupado de Cloud Service. La advertencia tiene este aspecto:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Para solucionar problemas al convertir los recursos en sentencias de informe, consulte [Documentación](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init)de informe. | Sí | Sí |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Estos analizadores comprueban algunos detalles relacionados con el paquete de [contenido para presentar el proceso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying) de conversión de modelos que crea artefactos que se ajustan al Modelo de características de Sling. Cualquier error debe notificarse a la asistencia al cliente de Adobe. | Sí | Sí |
| `api-regions-crossfeature-dups` | Valida que los paquetes OSGI del cliente no tengan declaraciones de paquete de exportación que anulen AEM como API pública de Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Para solucionarlo, deje de exportar un paquete que forma parte de la API pública AEM. | Sí | Sí |