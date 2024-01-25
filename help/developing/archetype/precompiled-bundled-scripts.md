---
title: Scripts agrupados precompilados
description: Obtenga información sobre cómo implementar scripts de componentes con paquetes OSGi en Adobe Experience Manager Cloud Service.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 53%

---


# Scripts agrupados precompilados {#precompiled-bundled-scripts}

AEM as a Cloud Service admite la implementación de los scripts de componentes [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#code-packages-%2F-osgi-bundles) como scripts agrupados precompilados. Esto permite a los desarrolladores precompilar sus scripts en el momento de la compilación y empaquetarlos como paquetes OSGi.

## Ventajas de implementar scripts precompilados mediante paquetes OSGi {#advantages}

La implementación de los scripts como scripts empaquetados precompilados tiene las siguientes ventajas:

+ La compilación de scripts en tiempo de compilación permite a los desarrolladores descubrir errores al principio del proceso de desarrollo.
+ Las dependencias de script de la API de Java se definen explícitamente mediante la variable `Import-Package` y `Export-Package` encabezados de paquete.
+ Herencia (mediante `sling:resourceSuperType`) y delegación a otros tipos de recursos (a través de HTL `data-sly-resource` elemento de bloque o a través de `sling:include` JSP (por ejemplo) se puede asignar a través de los metadatos del paquete.
+ Las versiones de tipo de recurso se pueden aplicar de forma similar a las API de Java.

## Precompilaciones e importaciones de paquetes {#precompilation}

El [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) puede validar la sintaxis de los scripts HTL, pero también se puede utilizar para transformar los scripts HTL en clases de Java. A continuación, se añaden a la carpeta `generated-sources` del proyecto Maven y `maven-compiler-plugin` los recoge.

Se puede agregar [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) para generar los metadatos del paquete OSGi para las importaciones de la API de Java.

## Herencia y delegación {#inheritance-delegation}

El marco OSGi proporciona una forma eficaz de definir [requisitos y capacidades](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) para expresar contratos entre varios componentes. Se describen mediante metadatos y se aplican durante la ejecución. Los scripts agrupados utilizan este mecanismo para expresar tanto sus relaciones de herencia (`sling:resourceSuperType`) como su delegación (incluidos otros tipos de recursos en el proceso de renderización).

El `bnd` complemento de [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) proyecto se puede utilizar para extraer los requisitos y las capacidades correspondientes a los scripts proporcionados por el [`ui.apps`.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#code-packages-%2F-osgi-bundles) paquete de contenido

## AEM Compatibilidad con tipo de archivo del proyecto {#support}

A partir de la versión 31 de, la variable [AEM Tipo de archivo del proyecto](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=es) AEM se puede utilizar para configurar correctamente un proyecto as a Cloud Service para utilizar scripts empaquetados precompilados.

Además, el tipo de archivos de proyectos AEM configura el [complemento Maven del analizador de compilaciones de SDK de AEM as a Cloud Service](/help/developing/archetype/build-analyzer-maven-plugin.md) para validar tanto las dependencias de nivel de paquete Java como las de nivel de script.
