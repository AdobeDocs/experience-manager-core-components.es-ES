---
title: Rutas de éxito con los componentes principales
description: Implementar el proyecto con los componentes principales con éxito
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: b1d38310a3f05e2dd2a68de1574a278bac2c78e7
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 100%

---


# Rutas de éxito con los componentes principales {#paths-to-success}

Los componentes principales son completos, flexibles y fáciles de usar y personalizar. Seguir algunas directrices clave como se describe en este documento garantizará que el proyecto con los componentes principales sea un éxito.

## Dos rutas para alcanzar el éxito {#two-paths}

Existen dos enfoques básicos para la aplicación de los componentes principales, que pueden permitir alcanzar el éxito pero tienen sus propios aspectos clave que deben tenerse en cuenta proyecto por proyecto.

1. Asigne sus diseños a los componentes principales y tome el HTML que proporcionan. O bien
1. Si tiene que cumplir con estándares HTML ya definidos, necesitará más esfuerzo y no obtendrá todas las ventajas de los componentes principales.

## Problemas comunes en la implementación de componentes {#common-pitfalls}

Dos problemas comunes que hacen que los proyectos no tengan éxito con los componentes principales son:

* **Diseños finalizados**: estos pueden incluso aprobarse a nivel C y entregarse al equipo de desarrollo para que se implementen en píxeles perfectos sin preocuparse por la tecnología subyacente.
* **Guía de estilo HTML para toda la empresa**: estas guías a menudo rigen el funcionamiento de los componentes que aplican estilos desde una perspectiva descendente.

En ambos casos, los requisitos realizados para los componentes son tan estrictos y específicos que es difícil hacer que los componentes principales o cualquier componente listo para usar los cumplan, lo que conduce al desarrollo masivo de componentes personalizados.

## Inicio temprano {#start-early}

En lugar de tener en cuenta únicamente los componentes principales en la fase de implementación del proyecto, comience a tenerlos en cuenta durante la fase de composición y diseño.

### Usar la biblioteca de componentes {#component-library}

Haga referencia a la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_es) que ya se encuentra en la fase de diseño. Los componentes principales son completos y flexibles y pueden convertirse en un gran punto de partida. Añada únicamente componentes personalizados cuando exista una necesidad empresarial real que realmente no se pueda lograr razonablemente con un componente principal.

### Uso del kit de IU para Adobe XD {#ui-kit}

Tan pronto como exista una necesidad comprobada de un componente personalizado, aproveche el kit de interfaz de usuario para Adobe XD, [que se puede descargar aquí,](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd?lang=es) para que los diseñadores puedan empezar a crear los modelos de alambres y los diseños con los componentes principales como componentes básicos.

## No pase por alto funciones muy útiles {#powerful-features}

Las funciones de AEM y los componentes principales pueden ser muy completas, pero también muy sutiles y muchas de las posibilidades que ofrecen podrían pasar desapercibidas para un diseñador.

### Fragmentos de contenido {#content-fragments}

Los [fragmentos de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html?lang=es) permiten crear contenido neutro con respecto al canal, así como variaciones (posiblemente específicas del canal). Después se pueden usar estos fragmentos, y sus variaciones, al crear páginas de contenido.

Junto con el exportador JSON actualizado, los fragmentos de contenido estructurados también se pueden utilizar para distribuir contenidos de AEM mediante servicios de contenido a canales en lugar de páginas de AEM.

### Plantillas de fragmento de experiencia {#experience-fragment-templates}

Si un creador desea reutilizar partes (un fragmento de una experiencia) de una página. Sin [fragmentos de experiencias](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html?lang=es), el creador tendría que copiar y pegar ese fragmento. Crear y mantener estas experiencias de copia y pegado es un proceso laborioso y es posible que el usuario cometa errores. Los fragmentos de experiencias eliminan la necesidad de copiar y pegar.

### El componente Insertar {#embed-component}

[El componente Insertar](/help/components/embed.md) no solo permite la inclusión sencilla de recursos externos como contenido de vídeo de YouTube, sino que también se puede ampliar para que quepa contenido específico para las necesidades de un proyecto.
