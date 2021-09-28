---
title: Scripts agrupados precompilados
description: Obtenga información sobre cómo implementar los scripts de componente mediante paquetes OSGi en Adobe Experience Manager Cloud Service.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Scripts agrupados precompilados

AEM como Cloud Service admite la implementación de los scripts de componente [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) como scripts agrupados precompilados. Esto permite a los desarrolladores precompilar sus scripts en el momento de la compilación y empaquetarlos como paquetes OSGi.

## Las ventajas de implementar scripts precompilados a través de paquetes OSGi

La implementación de los scripts como scripts empaquetados precompilados tiene las siguientes ventajas:

+ la compilación de secuencias de comandos en tiempo de compilación permite a los desarrolladores descubrir errores al principio del proceso de desarrollo
+ Las dependencias de script de la API Java se definen explícitamente mediante los encabezados de paquete `Import-Package` y `Export-Package`
+ la herencia (a través de `sling:resourceSuperType`) y la delegación a otros tipos de recursos (a través del elemento de bloque `data-sly-resource` de HTL o a través de la etiqueta `sling:include` JSP, por ejemplo) se puede asignar a través de los metadatos del paquete
+ las versiones de tipo de recurso se pueden aplicar de forma similar a las API de Java

## Precompilaciones e importaciones de paquetes

El [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) puede validar la sintaxis de los scripts HTL, pero también se puede utilizar para transformar los scripts HTL en clases Java. A continuación, se añaden a la carpeta `generated-sources` del proyecto Maven y la `maven-compiler-plugin` recoge.

Se puede agregar [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) para generar los metadatos del paquete OSGi para las importaciones de la API de Java.

## Herencia y delegación

El marco OSGi proporciona una manera poderosa de definir [Requisitos y capacidades](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) para expresar contratos entre diversos componentes. Se describen mediante metadatos y se aplican durante la ejecución. Las secuencias de comandos agrupadas utilizan este mecanismo para expresar tanto sus relaciones de herencia (`sling:resourceSuperType`) como su delegación (incluidos otros tipos de recursos en el proceso de renderización).

El complemento `bnd` del proyecto [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) puede utilizarse para extraer los requisitos y capacidades correspondientes a las secuencias de comandos proporcionadas por el paquete de contenido [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles).

## Compatibilidad con AEM tipo de archivo del proyecto

A partir de la versión 31, el [AEM tipo de archivo del proyecto](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) se puede utilizar para configurar correctamente un AEM como proyecto de Cloud Service para utilizar scripts empaquetados precompilados. Además, el tipo de archivo del proyecto AEM configura el [AEM como un Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) para validar tanto las dependencias de nivel de paquete Java como las de nivel de script.
