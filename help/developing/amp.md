---
title: Compatibilidad con AMP para los componentes principales
description: Los componentes principales admiten AMP - Accelerated Mobile Pages
role: Arquitecto, Desarrollador, Administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---


# Compatibilidad con AMP para los componentes principales {#amp-support}

Desde la [versión 2.11.0](/help/versions.md) de los componentes principales, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) son totalmente compatibles.

Este documento proporciona información general sobre cómo se admite AMP, así como sobre cómo habilitarlo para sus sitios. Sin embargo, para obtener información técnica completa, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## ¿Qué es AMP? {#what-is-amp}

Accelerated Mobile Pages o AMP es un marco de código abierto diseñado originalmente por Google para optimizar las páginas para la navegación móvil. Las páginas de AMP generalmente se cargan mucho más rápido que las páginas web estándar, lo que ofrece mejores experiencias móviles.

## AMP en los componentes principales {#amp-in-core-components}

La compatibilidad con AMP en los componentes principales es [totalmente configurable.](#enabling-amp) Las versiones AMP de las páginas se pueden servir exclusivamente, junto con las versiones HTML estándar, o no.

Los componentes principales utilizan `amp` como selector de Sling para procesar una página de AMP. Por ejemplo, `example.html` renderizaría la página normal y `example.amp.html` sería la versión de AMP.

Los proyectos individuales pueden decidir si se utiliza o no AMP. De hecho, como las páginas AMP y HTML estándar se pueden entregar en paralelo, un proyecto puede elegir utilizar AMP solo en determinadas páginas del proyecto.

## Introducción a la compatibilidad con AMP en su proyecto {#getting-started}

Aunque la compatibilidad con AMP ofrece un bueno nivel de flexibilidad, para empezar a utilizarla rápidamente solo se necesitan unos pocos pasos sencillos:

1. Instale la extensión de soporte AMP si es necesario.
   * Para AEM como proyectos de Cloud Service, la extensión está disponible automáticamente con los componentes principales y no es necesario realizar ninguna instalación.
   * Para los proyectos locales y AMS, la extensión debe instalarse explícitamente al instalar los componentes principales.
1. Una vez instalada la extensión AMP, el autor del componente debe simplemente señalar los supertipos de componentes a los de la extensión.
1. [Habilite la ](#enabling-amp) compatibilidad con AMP en el nivel de plantilla o en sus páginas individuales.
1. [Implemente ](#css-requirements) CSS en línea según sea necesario.

### Habilitación de AMP para páginas {#enabling-amp}

Para habilitar la AMP para una página, el **modo AMP** debe estar seleccionado en la [Política de página.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opciones de directiva de página AMP](/help/assets/amp-policy.png)

* **Sin AMP** : la página se entrega solo como HTML estándar.
* **AMP emparejado** : la página se entrega como AMP, así como como como HTML.
* **Solo AMP** : la página se entrega como AMP solamente.

La configuración de AMP para una página también se puede sobrescribir en [Propiedades de página](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) para una página individual.

![Propiedades de página de AMP](/help/assets/amp-page-properties.png)

* **Heredar de la plantilla de página** : este es el valor predeterminado, que permite que la configuración se tome de la política de la plantilla de página.
* **Sin AMP** : la página se entrega solo como HTML estándar.
* **AMP emparejado** : la página se entrega como AMP, así como como como HTML.
* **Solo AMP** : la página se entrega como AMP solamente.

### Requisitos de CSS {#css-requirements}

Cuando se utiliza AMP con los componentes principales, la diferencia principal es que AMP requiere que todos los [CSS estén insertados](including-clientlibs.md#inlining) en el elemento `<head>` y que también estén optimizados.

Para admitir esto, se utiliza un componente de página personalizado, que carga solo el CSS específico de AMP para los componentes presentes en la página.

>[!NOTE]
>
>Debido a las limitaciones de diseño de AMP, el Adobe no admite el uso de Cuadrícula interactiva con la versión de AMP de su página.

Para obtener más información técnica y requisitos, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
