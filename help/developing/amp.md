---
title: Compatibilidad con AMP para Componentes principales
description: 'Los componentes principales admiten AMP: Accelerated Mobile Pages'
role: Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
TQID: https://experienceleague.adobe.com/5v1tXLzHNRvAxy6-aJipN-ZYzsPJ1xFNc1hKmz73wic
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 59ca85e0f0b99ba46bb2b85f383f1fefd2b1c5fd
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 76%

---


# Compatibilidad con AMP para Componentes principales {#amp-support}

Desde la [versión 2.11.0](/help/versions.md) de los componentes principales, [AMP: Accelerated Mobile Pages](https://developers.google.com/amp) son totalmente compatibles.

Este documento proporciona información general sobre cómo se admite AMP, así como sobre cómo habilitarlo para sus sitios. Sin embargo, para obtener información técnica completa, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## ¿Qué es AMP? {#what-is-amp}

Accelerated Mobile Pages o AMP es un marco de código abierto diseñado originalmente por Google para optimizar las páginas para la navegación móvil. Las páginas de AMP generalmente se cargan mucho más rápido que las páginas web estándar, lo que ofrece mejores experiencias móviles.

## AMP en los componentes principales {#amp-in-core-components}

La compatibilidad con AMP en los componentes principales es [totalmente configurable.](#enabling-amp) Las versiones AMP de las páginas se pueden servir exclusivamente, junto con las versiones HTML estándar, o no.

Los componentes principales utilizan `amp` como selector de Sling para procesar una página de AMP. Por ejemplo, `example.html` renderizaría la página normal y `example.amp.html` sería la versión de AMP.

Los proyectos individuales pueden decidir si se utiliza o no AMP. De hecho, como las páginas AMP y HTML estándar se pueden entregar en paralelo, un proyecto puede elegir utilizar AMP solo en determinadas páginas del proyecto.

## Introducción a la compatibilidad con AMP en su proyecto {#getting-started}

Aunque la compatibilidad con AMP ofrece un buen nivel de flexibilidad, para empezar a utilizarla rápidamente se necesita completar unos pocos pasos sencillos:

1. [Instalación de los componentes principales](/help/get-started/using.md#download-and-install)
   * Para los proyectos de AEM as a Cloud Service, los componentes principales están disponibles de forma predeterminada y no es necesaria ninguna instalación adicional.
   * Para los proyectos locales y de AMS, puede [descargar el paquete de contenido más reciente para los componentes principales desde GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalarlo en sus entornos de AEM.
   * Si el proyecto On-Premise o AMS utiliza una versión de componentes principales anterior a la 2.14.0, también debe instalar la extensión AMP disponible como parte de la versión en GitHub.
1. Dirija su componente `resourceSuperType`s a `core/wcm/extensions/amp/components/page/v1/page`.
   * Si usó [el tipo de archivo del proyecto de AEM](/help/developing/archetype/using.md) para su proyecto como práctica recomendada y eligió [la opción para habilitar la compatibilidad con AMP](https://github.com/adobe/aem-project-archetype/tree/develop), esto se hizo automáticamente.
1. [Habilite la compatibilidad con AMP](#enabling-amp) en el nivel de plantilla o en sus páginas individuales.
1. [Implemente CSS en línea](#css-requirements) según sea necesario.

### Habilitar AMP para páginas {#enabling-amp}

Para habilitar la AMP para una página, el **modo AMP** debe estar seleccionado en la [Política de la página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es#editing-a-template-page-policy-template-author-developer)

![Opciones de política de la página de AMP](/help/assets/amp-policy.png)

* **Sin AMP**: la página se entrega solo como HTML estándar.
* **AMP emparejado**: la página se entrega como AMP, así como HTML.
* **Solo AMP**: la página se entrega como AMP solamente.

La configuración de AMP para una página también se puede sobrescribir en [Propiedades de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=es) para una página individual.

![Propiedades de página de AMP](/help/assets/amp-page-properties.png)

* **Heredar de la plantilla de página**: este es el valor predeterminado, que permite que la configuración se tome de la política de la plantilla de página.
* **Sin AMP**: la página se entrega solo como HTML estándar.
* **AMP emparejado**: la página se entrega como AMP, así como HTML.
* **Solo AMP**: la página se entrega como AMP solamente.

Estas opciones aparecen en la interfaz de usuario solo si `resourceSuperType` está configurado correctamente para la compatibilidad con AMP. El contenido de muestra WKND predeterminado no tiene `resourceSuperType` establecido y, por lo tanto, las opciones de AMP no están visibles en la interfaz de usuario.

### Requisitos de CSS {#css-requirements}

Cuando se utiliza AMP con los componentes principales, la diferencia principal es que AMP requiere que todos los [CSS estén insertados](including-clientlibs.md#inlining) en el elemento `<head>` y que también estén optimizados.

Para admitir esto, se utiliza un componente de página personalizado, que carga solo el CSS específico de AMP para los componentes presentes en la página.

>[!NOTE]
>
>Debido a las limitaciones de diseño de AMP, Adobe no admite el uso de Cuadrícula interactiva con la versión de AMP de su página.

Para obtener más información técnica y requisitos, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
