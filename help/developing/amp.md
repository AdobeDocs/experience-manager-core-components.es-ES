---
title: Compatibilidad con AMP para Componentes principales
description: 'Los componentes principales admiten AMP: Accelerated Mobile Pages'
role: Architect, Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 100%

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

1. Instale la extensión de compatibilidad con AMP si es necesario.
   * Para proyectos de AEM as a Cloud Service, la extensión está disponible automáticamente con los componentes principales y no es necesario realizar ninguna instalación.
   * Para los proyectos locales y AMS, la extensión debe instalarse explícitamente al instalar los componentes principales.
1. Una vez instalada la extensión de AMP, el autor del componente debe indicar los supertipos de componentes a los de la extensión.
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

### Requisitos de CSS {#css-requirements}

Cuando se utiliza AMP con los componentes principales, la diferencia principal es que AMP requiere que todos los [CSS estén insertados](including-clientlibs.md#inlining) en el elemento `<head>` y que también estén optimizados.

Para admitir esto, se utiliza un componente de página personalizado, que carga solo el CSS específico de AMP para los componentes presentes en la página.

>[!NOTE]
>
>Debido a las limitaciones de diseño de AMP, Adobe no admite el uso de Cuadrícula interactiva con la versión de AMP de su página.

Para obtener más información técnica y requisitos, consulte la [documentación para desarrolladores de GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
