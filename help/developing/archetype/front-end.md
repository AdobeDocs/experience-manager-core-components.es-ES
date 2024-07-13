---
title: Desarrollo front-end con el tipo de archivo del proyecto de AEM
description: Obtenga información acerca del mecanismo de versión del front-end opcional del tipo de archivo del proyecto de AEM basado en Webpack.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 100%

---


# Desarrollo front-end con el tipo de archivo del proyecto de AEM {#front-end}

El tipo de archivo del proyecto de AEM incluye un mecanismo de versión del front-end opcional basado en Webpack. Por lo tanto, el módulo ui.frontend se convierte en la ubicación central de todos los recursos front-end del proyecto, incluidos los archivos JavaScript y CSS. Para aprovechar plenamente esta función tan útil y flexible, es importante comprender cómo encaja el desarrollo front-end en un proyecto de AEM.

Este documento se centra en los patrones de uso generales del módulo de versión del front-end y en lo que hace por usted. Para obtener opciones de compilación detalladas e instrucciones técnicas, consulte la documentación en el repositorio de GitHub del tipo de archivo.

>[!TIP]
>
>El último tipo de archivo del proyecto de AEM y la documentación técnica asociada [se encuentran en GitHub.](https://github.com/adobe/aem-project-archetype)

## Desarrollo front-end y back-end de AEM {#front-end-back-end}

En términos muy simplificados, los proyectos de AEM se pueden considerar como dos partes separadas pero relacionadas:

* Desarrollo back-end que impulsa la lógica de AEM y produce bibliotecas Java, servicios OSGi, etc.
* Desarrollo front-end que impulsa la presentación y el comportamiento del sitio web resultante y produce bibliotecas JavaScript y CSS

Puesto que estos dos procesos de desarrollo se centran en diferentes partes del proyecto, el desarrollo del back-end y del front-end puede ocurrir en paralelo.

![diagrama del flujo de trabajo de front-end](/help/assets/front-end-flow.png)

Sin embargo, cualquier proyecto resultante debe utilizar los resultados de ambos esfuerzos de desarrollo, es decir, tanto del back-end como el front-end.

## Determinar el marcado {#determining-markup}

Independientemente del flujo de trabajo de desarrollo front-end que decida implementar para su proyecto, los desarrolladores back-end y front-end deben acordar primero el marcado. Normalmente AEM define el marcado, que proporciona los componentes principales. [Sin embargo, esto se puede personalizar si es necesario.](/help/developing/customizing.md#customizing-the-markup).

## Posibles flujos de trabajo de desarrollo front-end {#possible-workflows}

El módulo de versión del front-end es una herramienta útil y muy flexible, pero no impone ninguna opinión particular sobre cómo debe usarse. Los siguientes son dos ejemplos de uso *posible*, pero las necesidades de cada proyecto pueden dictar otros modelos de uso.

### Uso del servidor de desarrollo estático de Webpack {#using-webpack}

Con Webpack puede aplicar estilos y desarrollar en función de la salida estática de páginas web de AEM dentro del módulo ui.frontend.

1. Vista previa de la página en AEM con el modo de vista previa de página o pasando `wcmmode=disabled` en la URL
1. Ver el origen de la página y guardar como HTML estático en el módulo ui.frontend
1. [Inicie Webpack](#webpack-dev-server) y empiece a aplicar estilos y generar el JavaScript y CSS necesarios
1. Ejecute `npm run dev` para generar las clientlibs

En este flujo, un desarrollador de AEM puede realizar los pasos uno y dos y transferir el HTML estático al desarrollador de front-end que se desarrolla en función de la salida HTML de AEM.

>[!TIP]
>
>También se puede aprovechar la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_es) para capturar muestras de la salida de marcado de cada componente para que funcionen a nivel de componente en lugar de a nivel de página.

### Utilizar Storybook {#using-storybook}

Al utilizar [Storybook](https://storybook.js.org) puede realizar un desarrollo del front-end atómico más amplio. Aunque Storybook no está incluido en el tipo de archivo del proyecto de AEM, puede instalarlo y almacenar los artefactos de Storybook dentro del módulo ui.frontend. Cuando estén listos para realizar pruebas en AEM, se pueden implementar como clientlibs ejecutando `npm run dev`.

>[!NOTE]
>
>El tipo de archivo del proyecto de AEM no incluye [Storybooktype](https://storybook.js.org). Si decide usarlo, debe instalarlo por separado.

## Información general sobre las clientlibs {#clientlibs}

El módulo de front-end está disponible mediante un [clientLib de AEM. ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=es). Al ejecutar el script de versión de NPM, la aplicación se crea y el paquete `aem-clientlib-generator` toma la salida de versión resultante y la transforma en un clientlib de este tipo.

Un clientlib constará de los siguientes archivos y directorios:

* `css/`: Archivos CSS que se pueden solicitar en el HTML
* `css.txt`: Indica a AEM el orden y los nombres de los archivos en `css/` para que se puedan combinar
* `js/`: Archivos JavaScript que se pueden solicitar en el HTML
* `js.txt` Indica a AEM el orden y los nombres de los archivos en `js/` para que se puedan combinar
* `resources/`: Mapas de origen, fragmentos de código de punto de entrada (resultantes de la división del código), recursos estáticos (por ejemplo, iconos), etc.

>[!TIP]
>
>Obtenga más información acerca de cómo gestiona AEM las clientlibs en la [documentación de desarrollo de AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=es) y cómo incluirlas en la [Documentación de componentes principales.](/help/developing/including-clientlibs.md)
