---
title: Compatibilidad de AMP con los componentes principales
description: Los componentes principales admiten AMP - Páginas móviles aceleradas
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---


# Compatibilidad de AMP con los componentes principales {#amp-support}

A partir de la [versión 2.11.0](/help/versions.md) de los componentes principales, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) son totalmente compatibles.

Este documento proporciona información general sobre cómo se admite AMP, así como sobre cómo habilitarlo para sus sitios. Sin embargo, para obtener más información técnica, consulte la [documentación del desarrollador de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## ¿Qué es AMP? {#what-is-amp}

Accelerated Mobile Pages o AMP es un marco de trabajo de código abierto diseñado originalmente por Google para optimizar las páginas para la navegación móvil. Las páginas AMP generalmente se cargan mucho más rápido que las páginas web estándar, lo que ofrece mejores experiencias móviles.

## AMP en los componentes principales {#amp-in-core-components}

La compatibilidad con AMP en los componentes principales es [totalmente configurable.](#enabling-amp) Las versiones AMP de las páginas se pueden servir exclusivamente, junto con las versiones HTML estándar, o no.

Los componentes principales utilizan `amp` como selector de Sling para procesar una página de AMP. Por ejemplo: `example.html` representaría la página normal y `example.amp.html` sería la versión de AMP.

Los proyectos individuales pueden decidir si aprovechar o no la AMP. De hecho, como AMP y las páginas HTML estándar se pueden entregar en paralelo, un proyecto puede elegir utilizar AMP solo en determinadas páginas del proyecto.

## Introducción a la compatibilidad con AMP en su proyecto {#getting-started}

Aunque el soporte de AMP oferta una buena cantidad de flexibilidad, para empezar a utilizarlo rápidamente sólo se requieren unos pocos pasos sencillos:

1. Instale la extensión de soporte AMP si es necesario.
   * Para AEM como proyectos de Cloud Service, la extensión está disponible automáticamente con los componentes principales y no es necesaria ninguna instalación.
   * Para los proyectos in situ y AMS, la extensión debe instalarse explícitamente al instalar los componentes principales.
1. Una vez instalada la extensión AMP, el autor del componente simplemente debe señalar los supertipos de componente a los de la extensión.
1. [Habilite la ](#enabling-amp) compatibilidad con AMP en el nivel de plantilla o en sus páginas individuales.
1. [Implemente ](#css-requirements) CSS alineadas según sea necesario.

### Habilitación de AMP para páginas {#enabling-amp}

Para habilitar AMP para una página, el **modo AMP** debe estar seleccionado en la [Directiva de página.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opciones de directiva de página AMP](/help/assets/amp-policy.png)

* **Sin AMP** : la página solo se entrega como HTML estándar.
* **AMP**  emparejada: la página se entrega como AMP y como HTML.
* **Solo**  AMP: la página se entrega como AMP solamente.

La configuración de AMP de una página también se puede anular en [Propiedades de la página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) para una página individual.

![Propiedades de página AMP](/help/assets/amp-page-properties.png)

* **Heredar de plantilla**  de página: es el valor predeterminado, que permite tomar la configuración de la directiva de la plantilla de página.
* **Sin AMP** : la página solo se entrega como HTML estándar.
* **AMP**  emparejada: la página se entrega como AMP y como HTML.
* **Solo**  AMP: la página se entrega como AMP solamente.

### Requisitos de CSS {#css-requirements}

Cuando se utiliza AMP con los componentes principales, la diferencia principal es que AMP requiere que todos los [CSS estén alineados](including-clientlibs.md#inlining) en el elemento `<head>` y optimizados.

Para admitir esto, se utiliza un componente de página personalizado, que carga solo la CSS específica de AMP para los componentes presentes en la página.

Para obtener más detalles técnicos y requisitos, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
