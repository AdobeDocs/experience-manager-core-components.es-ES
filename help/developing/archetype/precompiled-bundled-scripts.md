---
title: Scripts agrupados precompilados
description: Obtenga información sobre cómo implementar scripts de componentes con paquetes OSGi en Adobe Experience Manager Cloud Service.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: b39cd395d17f6aab7376e01fc01a7c0e98b2460f
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 100%

---


# Scripts agrupados precompilados

AEM as a Cloud Service admite la implementación de los scripts de componentes [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#code-packages-%2F-osgi-bundles) como scripts agrupados precompilados. Esto permite a los desarrolladores precompilar sus scripts en el momento de la compilación y empaquetarlos como paquetes OSGi.

## Ventajas de implementar scripts precompilados a través de paquetes OSGi

La implementación de los scripts como scripts empaquetados precompilados tiene las siguientes ventajas:

+ La compilación de scripts en tiempo de compilación permite a los desarrolladores descubrir errores al principio del proceso de desarrollo
+ Las dependencias de script de la API de Java se definen explícitamente mediante los encabezados de paquete `Import-Package` y `Export-Package`
+ La herencia (a través de `sling:resourceSuperType`) y la delegación a otros tipos de recursos (a través del elemento de bloque `data-sly-resource` de HTL o a través de la etiqueta JSP `sling:include`, por ejemplo) se puede asignar a través de los metadatos del paquete
+ Las versiones de tipo de recurso se pueden aplicar de forma similar a las API de Java

## Precompilaciones e importaciones de paquetes

El [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) puede validar la sintaxis de los scripts HTL, pero también se puede utilizar para transformar los scripts HTL en clases de Java. A continuación, se añaden a la carpeta `generated-sources` del proyecto Maven y `maven-compiler-plugin` los recoge.

Se puede agregar [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) para generar los metadatos del paquete OSGi para las importaciones de la API de Java.

## Herencia y delegación

El marco OSGi proporciona una gran opción para definir [Requisitos y capacidades](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) para expresar contratos entre diversos componentes. Se describen mediante metadatos y se aplican durante la ejecución. Los scripts agrupados utilizan este mecanismo para expresar tanto sus relaciones de herencia (`sling:resourceSuperType`) como su delegación (incluidos otros tipos de recursos en el proceso de renderización).

El complemento `bnd` del proyecto [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) puede utilizarse para extraer los requisitos y las capacidades correspondientes a los scripts que ofrece el paquete de contenido [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=es#code-packages-%2F-osgi-bundles).

## Compatibilidad con archivos de proyectos AEM

A partir de la versión 31, el [tipo de archivos de proyectos AEM](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=es) se puede utilizar para configurar correctamente un proyecto de AEM as a Cloud Service para utilizar scripts empaquetados precompilados. Además, el tipo de archivos de proyectos AEM configura el [complemento Maven del analizador de compilaciones de SDK de AEM as a Cloud Service](/help/developing/archetype/build-analyzer-maven-plugin.md) para validar tanto las dependencias de nivel de paquete Java como las de nivel de script.
