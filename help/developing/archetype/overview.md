---
title: Tipo de archivo del proyecto AEM
description: Obtenga información acerca del Arquetipo de proyecto de AEM que sirve como plantilla para aplicaciones basadas en AEM.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8940285f4c5e5870b6a135dac674f06e4c1d8b5a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 100%

---


# Tipo de archivo del proyecto AEM {#aem-project-archetype}

El tipo de archivo del proyecto de AEM es una plantilla de Maven que crea un proyecto mínimo de Adobe Experience Manager (AEM) basado en las prácticas recomendadas como punto de partida para su sitio web. Esta documentación proporciona una descripción general de las ventajas del tipo de archivo y del uso general. Encontrará instrucciones técnicas detalladas y documentación en el tipo de archivo del repositorio de GitHub.

>[!TIP]
>
>El último tipo de archivo del proyecto de AEM y la documentación técnica asociada [se encuentran en GitHub.](https://github.com/adobe/aem-project-archetype)

## Por qué utilizar el tipo de archivo {#why-use-the-archetype}

El uso del tipo de archivo del proyecto de AEM le permite avanzar hacia la creación de un proyecto de AEM basado en las prácticas recomendadas con solo pulsar unas pocas teclas. Mediante el uso del tipo de archivo, todas las piezas ya estarán en su sitio para que, aunque el proyecto resultante sea mínimo, ya implemente todas las [características clave](/help/developing/archetype/using.md#what-you-get) de AEM para que solo tenga que generar y ampliar.

Por supuesto, hay muchos elementos que entran en un [proyecto de AEM correcto,](/help/developing/success.md) pero el uso del tipo de archivo del proyecto de AEM es una base sólida y se recomienda encarecidamente para cualquier proyecto de AEM.

## Características {#features}

* **Práctica recomendada:** inicie su sitio con todas las prácticas recomendadas más recientes de Adobe.
* **Código bajo:** edite sus plantillas, cree contenido, implemente su CSS y el sitio estará listo para su publicación.
* **Preparado para la nube:** si lo desea, utilice [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=es) para publicarlo en pocos días y facilitar la escalabilidad y el mantenimiento.
* **Dispatcher:** un proyecto se completa solamente con una [configuración de Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=es)que garantice la velocidad y la seguridad.
* **Varios sitios:** si es necesario, el tipo de archivo genera la estructura de contenido para una [configuración de varios idiomas y regiones](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=es).
* **Componentes principales:** los autores pueden crear casi cualquier diseño con nuestro versátil [conjunto de componentes estandarizados](/help/introduction.md).
* **Plantillas editables:** combine prácticamente cualquier [plantilla sin código](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=es) y defina lo que los autores pueden editar.
* **Diseño interactivo:** en plantillas o páginas individuales, [defina el reflujo de los elementos](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=es) para los puntos de interrupción definidos.
* **Encabezado y pie de página:** reúna y localícelos sin código, utilizando las [funciones de localización de los componentes](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=es).
* **Sistema de estilos:** evite crear componentes personalizados al permitir que los autores [les apliquen estilos diferentes](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=es).
* **Compilación front-end:** los desarrolladores de front-end pueden [burlar las páginas de AEM y crear bibliotecas de cliente](front-end.md) con Webpack, TypeScript y SASS.
* **Preparado para aplicaciones web:** Para sitios que utilizan React o Angular, utilice el [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=es) para mantener la [autoría en el contexto de la aplicación](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es).
* **Comercio habilitado:** para proyectos que desean integrar [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=es) con soluciones de comercio como [Magento](https://magento.com/es) utilizando [componentes principales de comercio](https://github.com/adobe/aem-core-cif-components).
* **Código de ejemplo:** cierre la compra del componente HelloWorld y de los modelos, servlets, filtros y programadores de ejemplo.
* **Abrir fuente:** si algo no funciona como debería, [contribuya con sus mejoras](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md).

## Lectura adicional {#further-reading}

* **[Arquetipo de proyecto de AEM GitHub:](https://github.com/adobe/aem-project-archetype)** Para un uso completo y detalles técnicos del tipo de archivo
* **[Uso del tipo de archivo:](using.md)** Una visión general de cómo utilizar el tipo de archivo en el proyecto y los módulos resultantes generados
* **[Desarrollo front-end con el tipo de archivo del proyecto de AEM:](front-end.md)** Cómo utilizar el módulo front-end del tipo de archivo
* **Los siguientes tutoriales están basados en este tipo de archivo:**
   * **[Sitio WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es)** Aprenda a iniciar un nuevo sitio web.
   * **[Aplicación de una sola página WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=es)** Aprenda a crear una aplicación web de React o Angular totalmente legible en AEM.
