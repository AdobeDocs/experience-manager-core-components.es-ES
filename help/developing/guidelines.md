---
title: Instrucciones de los componentes
description: Los componentes principales siguen patrones de implementación modernos que son bastante diferentes de los componentes de base.
role: Architect, Developer, Admin
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: ee18626280f74a51a799f16d6bf3f5b0be9cd6b9
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 99%

---

# Instrucciones de los componentes {#component-guidelines}

Los [componentes principales](overview.md) siguen patrones de implementación modernos que son bastante diferentes de los componentes de base.

En esta página se explican estos patrones y cuándo utilizarlos para crear sus propios componentes legibles. La primera sección [Patrones de componentes generales](#general-component-patterns) se aplica a cualquier tipo de componente, mientras que la segunda sección [Patrones de componentes reutilizables](#reusable-component-patterns) se aplica a componentes que se van a reutilizar en sitios o proyectos, como los componentes principales, por ejemplo.

## Patrones de componentes generales {#general-component-patterns}

Las directrices de esta sección se recomiendan para cualquier tipo de componente, independientemente de si es específico de un solo proyecto o de si debe reutilizarse ampliamente en sitios o proyectos.

### Componentes configurables {#configurable-components}

Los componentes pueden tener cuadros de diálogo con diversas opciones. Esto debe aprovecharse para que los componentes sean flexibles y configurables, y para evitar implementar varios componentes que en su mayoría son variaciones entre sí.

Normalmente, si un modelo de malla metálica o diseño contiene variaciones de elementos similares, estas variaciones no deben implementarse como componentes diferentes, sino como un único componente con opciones para elegir entre las variaciones.

Para ir más lejos, si los componentes se reutilizan en sitios o proyectos, consulte la sección [Funciones preconfigurables](#pre-configurable-capabilities).

### Separación de preocupaciones {#separation-of-concerns}

Normalmente se recomienda mantener la lógica (o el modelo) de un componente separado de la plantilla (o vista) de marcado. Existen varias formas de conseguirlo, pero la recomendada es utilizar [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) para la lógica y el [Lenguaje de plantilla HTML](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=es) (HTL) para el marcado, como también lo hacen los componentes principales.

Los modelos Sling son un conjunto de anotaciones Java para acceder fácilmente a las variables necesarias desde los POJO y, por lo tanto, ofrecen una forma sencilla, potente y eficaz de implementar la lógica Java para los componentes.

HTL ha sido diseñado para ser un lenguaje de plantilla seguro y sencillo, adaptado para AEM. Puede llamar a muchas formas de lógica, lo que la hace muy flexible.

## Patrones de componente reutilizables {#reusable-component-patterns}

Las directrices de esta sección se pueden utilizar también para cualquier tipo de componente, pero tienen más sentido para los que se van a reutilizar en sitios o proyectos, como los componentes principales, por ejemplo. Por lo tanto, estas directrices se pueden ignorar para los componentes que solo se utilizan en un sitio o proyecto único.

### Capacidades preconfigurables {#pre-configurable-capabilities}

Además del cuadro de diálogo de edición que utilizan los autores de páginas, los componentes también pueden tener un cuadro de diálogo de diseño para que los autores de plantillas los preconfiguren. El [Editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) permite configurar todas estas preconfiguraciones, que se denominan &quot;Directivas&quot;.

Para que los componentes sean lo más reutilizables posible, se les deben proporcionar opciones significativas para preconfigurarlos. Esto permitirá habilitar o deshabilitar las características de los componentes para que coincidan con las necesidades específicas de distintos sitios.

### Patrón de componentes proxy {#proxy-component-pattern}

Dado que cada recurso de contenido tiene una propiedad `sling:resourceType` que hace referencia al componente para representarlo, normalmente se recomienda tener estas propiedades que apunten a componentes específicos del sitio, en lugar de apuntar a componentes que comparten varios sitios. Esto ofrecerá más flexibilidad y evitará la refactorización de contenido si un sitio necesita un comportamiento diferente para un componente, ya que esta personalización se puede conseguir en el componente específico del sitio y no afectará a los otros sitios.

Sin embargo, para que los componentes específicos del proyecto no dupliquen ningún código, cada uno debe hacer referencia al componente principal compartido con la propiedad `sling:resourceSuperType`. Estos componentes específicos del proyecto que en su mayoría solo hacen referencia a componentes principales se denominan &quot;componentes proxy&quot;. Los componentes proxy pueden estar completamente vacíos si heredan completamente la funcionalidad o si pueden redefinir algunos aspectos del componente.

>[!TIP]
>
>Consulte [Uso de componentes principales](/help/get-started/using.md#create-proxy-components) para obtener más información sobre cómo crear componentes proxy.

### Versiones de componentes {#component-versioning}

Los componentes deben ser totalmente compatibles con el paso del tiempo, pero a veces son necesarios cambios que no pueden mantenerse compatibles. Una solución a estas necesidades opuestas es introducir el control de versiones de componentes añadiendo un número en su ruta de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal tal como se define en las [directrices semánticas de versiones](https://semver.org/), que se incrementa solo para los cambios que no son compatibles con versiones anteriores.

Los cambios incompatibles en los siguientes aspectos de los componentes resultarán en una nueva versión de ellos:

* Modelos Sling (siguiendo las directrices semánticas de versiones)
* Plantillas y scripts HTL
* Marcado HTML y selectores CSS
* Representación JSON
* Cuadros de diálogo

Para obtener más información, consulte el documento [Directivas de versiones](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) en GitHub.

El control de versiones de componentes crea una forma de contrato que es importante para las actualizaciones, ya que aclara cuándo puede ser necesario refactorizar algo. Consulte también la sección [Compatibilidad de la actualización de las personalizaciones](customizing.md#upgrade-compatibility-of-customizations), que explica qué consideraciones requieren diferentes formas de personalizaciones para una actualización.

Para evitar migraciones de contenido dolorosas, es importante no señalar nunca directamente los componentes con versiones de los recursos de contenido. Como regla general, un `sling:resourceType` del contenido nunca debe tener un número de versión, o actualizar componentes requerirá que el contenido también se refactorice. La mejor manera de evitar esto es seguir el [Patrón de componentes proxy](#proxy-component-pattern) descrito anteriormente.

### Interfaces de modelo {#model-interfaces}

Este patrón trata de la instrucción `data-sly-use` de HTL para señalar a una interfaz de Java, mientras que la implementación del modelo Sling también se registra al tipo de recurso del componente.

Cuando se combina con el [Patrón de componentes proxy](#proxy-component-pattern) descrito anteriormente, esta forma de enlace doble ofrece los siguientes puntos de extensión:

1. Un sitio puede redefinir la implementación de un modelo Sling registrándolo en el tipo de recurso del componente proxy, sin tener que preocuparse por el archivo HTL, que aún puede apuntar a la interfaz.
1. Un sitio puede redefinir el marcado HTL de un componente, sin tener que preocuparse por la lógica de implementación a la que debería apuntar.

## En resumen {#putting-it-all-together}

A continuación se ofrece una descripción general de toda la estructura de enlace de tipo de recurso, tomando como ejemplo el componente principal de título. Muestra cómo un componente proxy específico del sitio permite resolver el control de versiones de los componentes, para evitar que el recurso de contenido contenga ningún número de versión. A continuación, muestra cómo utiliza el archivo `title.html` [HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) del componente en la interfaz del modelo, mientras que la implementación se une a la versión específica del componente mediante anotaciones del [Modelo Sling](https://sling.apache.org/documentation/bundles/models.html).

![Información general de enlace de recursos](/help/assets/chlimage_1-32.png)

A continuación se muestra otra descripción general, que no muestra los detalles del la implementación POJO, pero revela cómo se hace referencia a las [plantillas y directivas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html) asociadas.

La propiedad `cq:allowedTemplates` indica qué plantillas se pueden utilizar para un sitio y la `cq:template` indica a cada página qué es la plantilla asociada. Cada plantilla consta de las siguientes tres partes:

* **estructura**: contiene los recursos que se forzarán en cada página a estar presentes y que el autor de la página no podrá eliminar, como los componentes de encabezado y pie de página de la página.
* **inicial**: contiene el contenido inicial que se duplicará en la página cuando se cree.
* **directivas**: contiene para cada componente la asignación a una directiva, que es la preconfiguración del componente. Esta asignación permite reutilizar las directivas en todas las plantillas y, por lo tanto, administrarlas de forma centralizada.

![Información general sobre plantillas y directivas](/help/assets/screen_shot_2018-12-07at093102.png)

## Tipo de archivo del proyecto AEM {#aem-project-archetype}

[El archivo del proyecto de AEM](/help/developing/archetype/overview.md) procesa un proyecto mínimo de Adobe Experience Manager como punto de partida para sus propios proyectos, incluido un ejemplo de componentes personalizados de HTL con modelos Sling para la lógica y la implementación correcta de los componentes principales con el patrón de proxy recomendado.

**Consulte lo siguiente:**

* [Uso de componentes principales](/help/get-started/using.md): ponga en marcha los componentes principales con sus propios proyectos.
* [Personalizar componentes principales](customizing.md): para aprender a aplicar estilos y personalizar los componentes principales.
