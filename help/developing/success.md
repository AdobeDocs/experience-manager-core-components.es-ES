---
title: Rutas para el éxito con los componentes principales
description: Cómo realizar el proyecto con éxito con los componentes principales
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# Rutas para el éxito con los componentes principales {#paths-to-success}

Los componentes principales son potentes, flexibles y fáciles de usar y personalizar. Si sigue algunas directrices clave como se describe en este documento, se asegurará de que el proyecto con los componentes principales sea un éxito.

## Dos rutas para el éxito {#two-paths}

Existen dos enfoques básicos para la aplicación de los componentes básicos, que pueden dar lugar al éxito pero tienen sus propios compromisos que deben considerarse proyecto por proyecto.

1. Asigne los diseños a los componentes principales y tome el código HTML que proporcionan. O bien
1. Si tiene que cumplir con estándares HTML ya definidos, necesitará más esfuerzo y no obtendrá todas las ventajas de los componentes principales.

## Problemas comunes en la implementación de componentes {#common-pitfalls}

Dos problemas comunes que llevan a proyectos que no tienen éxito con los componentes principales son:

* **Diseños** finalizados - Éstos pueden incluso ser aprobados de nivel C y se entregan al equipo de desarrollo para que se implementen en píxeles perfectos sin preocuparse por la tecnología subyacente.
* **Guía** de estilo HTML para toda la compañía: estas guías con demasiada frecuencia deben ir seguidas dogmáticamente por los componentes que aplican estilos desde una perspectiva descendente.

En ambos casos, los requisitos de los componentes son tan estrictos y específicos, que es difícil que los componentes principales o cualquier componente incorporado los cumplan, lo que lleva al desarrollo masivo de componentes personalizados.

## Inicio temprano {#start-early}

En lugar de considerar únicamente los componentes principales en la fase de implementación del proyecto, ya se ha realizado un inicio con los componentes principales durante la fase de diseño y wireframing.

### Uso de la biblioteca de componentes {#component-library}

Haga referencia a la biblioteca [de](https://adobe.com/go/aem_cmp_library) componentes que ya se encuentra en la fase de diseño. Los componentes principales son potentes y flexibles y pueden llevarle hasta el punto de partida. Agregue sólo componentes personalizados cuando haya una necesidad comercial real que realmente no pueda alcanzarse razonablemente con un componente principal.

### Uso del kit de IU para Adobe XD {#ui-kit}

Tan pronto como haya una necesidad comprobada de un componente personalizado, aproveche el kit de [interfaz de usuario para Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) de modo que los diseñadores puedan crear inicios en la creación de los esquemas y los diseños con los componentes principales como componentes básicos.

## No pase por alto las potentes funciones {#powerful-features}

Las funciones de AEM y los componentes principales pueden ser muy potentes, pero también muy sutiles y las posibilidades de determinadas funciones podrían no ser evidentes de inmediato para un diseñador.

### Fragmentos de contenido {#content-fragments}

[Los fragmentos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) de contenido le permiten crear contenido neutro para el canal, junto con variaciones (posiblemente específicas del canal). Después se pueden usar estos fragmentos, y sus variaciones, al crear páginas de contenido.

Junto con el exportador JSON actualizado, los fragmentos de contenido estructurados también se pueden utilizar para distribuir contenidos de AEM mediante servicios de contenido a canales en lugar de páginas de AEM.

### Plantillas de fragmento de experiencias {#experience-fragment-templates}

Si un creador desea reutilizar partes (un fragmento de una experiencia) de una página. Without [Experience Fragments,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) the author would need to copy and paste that fragment. Crear y mantener estas experiencias de copia y pegado es un proceso laborioso y es posible que el usuario cometa errores. Los fragmentos de experiencias eliminan la necesidad de copiar y pegar.

### El componente Incrustar {#embed-component}

[El componente](/help/components/embed.md) Incrustar no sólo permite la simple inclusión de recursos externos como el contenido de vídeo de YouTube, sino que también se puede ampliar para permitir que se ajuste a contenido específico de las necesidades de un proyecto.