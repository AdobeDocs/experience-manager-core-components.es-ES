---
title: Compatibilidad de AMP con los componentes principales
description: Los componentes principales admiten AMP - Páginas móviles aceleradas
translation-type: tm+mt
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---


# Compatibilidad de AMP con los componentes principales {#amp-support}

Desde la [versión 2.11.0](/help/versions.md) de los componentes principales, [AMP - Accelerated Mobile Pages](https://developers.google.com/amp) - es totalmente compatible.

Este documento proporciona información general sobre cómo se admite AMP, así como sobre cómo habilitarlo para sus sitios. Sin embargo, para obtener más información técnica, consulte la documentación para desarrolladores de [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## ¿Qué es AMP? {#what-is-amp}

Accelerated Mobile Pages o AMP es un marco de trabajo de código abierto diseñado originalmente por Google para optimizar las páginas para la navegación móvil. Las páginas AMP generalmente se cargan mucho más rápido que las páginas web estándar, lo que ofrece mejores experiencias móviles.

## AMP en los componentes principales {#amp-in-core-components}

La compatibilidad con AMP en los componentes principales es [totalmente configurable.](#enabling-amp) Las versiones AMP de las páginas se pueden servir exclusivamente, junto con las versiones HTML estándar, o no.

Los componentes principales se utilizan `amp` como selector de Sling para procesar una página de AMP. Por ejemplo `example.html` , representaría la página normal y `example.amp.html` sería la versión de AMP.

### Requisitos {#requirements}

Cuando se utiliza AMP con los componentes principales, la diferencia principal es que AMP requiere que todas las CSS estén alineadas en el `<head>` elemento y optimizadas.

Para admitir esto, se utiliza un componente de página personalizado, que carga solo la CSS específica de AMP para los componentes presentes en la página.

Para obtener más detalles técnicos y requisitos, consulte la documentación para desarrolladores de [GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### Uso de AMP en los componentes principales {#using-amp}

Los proyectos individuales pueden decidir si aprovechar o no la AMP. De hecho, como AMP y las páginas HTML estándar se pueden entregar en paralelo, un proyecto puede elegir utilizar AMP solo en determinadas páginas del proyecto.

### Instalación de compatibilidad con AMP {#installing-amp}

Dado que AMP es opcional, se entrega como extensión a los componentes principales.

* Para AEM como proyectos Cloud Service, la extensión está disponible automáticamente.
* Para los proyectos in situ y AMS, la extensión debe instalarse explícitamente al instalar los componentes principales.

Una vez instalada la extensión, el autor del componente simplemente debe señalar los supertipos del componente a los de la extensión.

### Activación de AMP para páginas {#enabling-amp}

Para habilitar AMP para una página, el modo **** AMP debe estar seleccionado en la directiva [de página.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![Opciones de directiva de página AMP](/help/assets/amp-policy.png)

* **Sin AMP** : la página se entrega solo como HTML estándar.
* **AMP** emparejada: la página se entrega como AMP y como HTML.
* **Solo** AMP: la página se entrega como AMP solamente.

La configuración de AMP de una página también se puede anular en las Propiedades [de](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) página de una página individual.

![Propiedades de página AMP](/help/assets/amp-page-properties.png)

* **Heredar de plantilla** de página: es el valor predeterminado, que permite tomar la configuración de la directiva de la plantilla de página.
* **Sin AMP** : la página se entrega solo como HTML estándar.
* **AMP** emparejada: la página se entrega como AMP y como HTML.
* **Solo** AMP: la página se entrega como AMP solamente.