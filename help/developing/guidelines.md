---
title: Instrucciones de los componentes
description: Los componentes principales siguen patrones de implementación modernos que son muy diferentes de los componentes básicos.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 2%

---


# Instrucciones de los componentes {#component-guidelines}

Los componentes [principales](overview.md) siguen patrones de implementación modernos que son muy diferentes de los componentes básicos.

Esta página explica estos patrones y cuándo utilizarlos para crear sus propios componentes de creación. La primera sección Patrones [de componentes](#general-component-patterns) generales se aplica a cualquier tipo de componente, mientras que la segunda sección Patrones [de componentes](#reusable-component-patterns) reutilizables se aplica a los componentes que se van a reutilizar en sitios o proyectos, como los componentes principales, por ejemplo.

## Patrones de componentes generales {#general-component-patterns}

Las directrices de esta sección se recomiendan para cualquier tipo de componente, independientemente de si el componente es específico de un solo proyecto o de si el componente debe reutilizarse ampliamente en sitios o proyectos.

### Componentes configurables {#configurable-components}

Los componentes pueden tener diálogos con una variedad de opciones. Esto debería aprovecharse para hacer que los componentes sean flexibles y configurables, y evitar implementar múltiples componentes que son principalmente variaciones entre sí.

Normalmente, si un modelo de alambre o diseño contiene variaciones de elementos similares, estas variaciones no deben implementarse como componentes diferentes, sino como el único componente con opciones para elegir entre las variaciones.

Para ir más allá, si los componentes se reutilizan en sitios o proyectos, consulte la sección Capacidades [](#pre-configurable-capabilities) preconfigurables.

### Separación de preocupaciones {#separation-of-concerns}

Mantener la lógica (o el modelo) de un componente separado de la plantilla de marcado (o vista) suele ser una buena práctica. Existen varias formas de lograrlo, pero la recomendada es utilizar modelos [Sling](https://sling.apache.org/documentation/bundles/models.html) para la lógica y el lenguaje [de plantilla](https://docs.adobe.com/content/help/es-ES/experience-manager-htl/using/overview.html) HTML (HTL) para el marcado, como también lo hacen los componentes principales.

Los modelos Sling son un conjunto de anotaciones Java para acceder fácilmente a las variables necesarias de los POJO y, por lo tanto, oferta una forma sencilla, potente y eficaz de implementar la lógica Java para los componentes.

HTL ha sido diseñado para ser un lenguaje de plantilla seguro y sencillo, adaptado a AEM. Puede llamar a muchas formas de lógica, lo que la hace muy flexible.

## Patrones de componentes reutilizables {#reusable-component-patterns}

Las directrices de esta sección se pueden usar también para cualquier tipo de componente, pero tienen más sentido para los componentes que se van a reutilizar en sitios o proyectos, como los componentes principales, por ejemplo. Por lo tanto, estas directrices se pueden ignorar para los componentes que solo se utilizan en un único sitio o proyecto.

### Capacidades preconfigurables {#pre-configurable-capabilities}

Además del cuadro de diálogo de edición que utilizan los autores de páginas, los componentes también pueden tener un cuadro de diálogo de diseño para que los autores de plantillas los preconfiguren. El Editor [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) plantillas permite configurar todas estas preconfiguraciones, que se denominan &quot;Directivas&quot;.

Para que los componentes sean lo más reutilizables posible, se les deben proporcionar opciones significativas para preconfigurarlos. Esto permitirá habilitar o deshabilitar las características de los componentes para que coincidan con las necesidades específicas de los distintos sitios.

### Patrón de componentes proxy {#proxy-component-pattern}

Dado que cada recurso de contenido tiene una `sling:resourceType` propiedad que hace referencia al componente para representarlo, es recomendable que estas propiedades apunten a componentes específicos del sitio, en lugar de apuntar a componentes compartidos por varios sitios. Esto oferta más flexibilidad y evita la refactorización de contenido si un sitio necesita un comportamiento diferente para un componente, ya que esta personalización se puede lograr en el componente específico del sitio y no afectará a los otros sitios.

Sin embargo, para que los componentes específicos del proyecto no tengan duplicado con ningún código, deben hacer referencia al componente principal compartido con la `sling:resourceSuperType` propiedad. Estos componentes específicos del proyecto que en su mayoría solo hacen referencia a componentes principales se denominan &quot;componentes proxy&quot;. Los componentes proxy pueden estar completamente vacíos si heredan completamente la funcionalidad o pueden redefinir algunos aspectos del componente.

### Versiones de componentes {#component-versioning}

Los componentes deben ser totalmente compatibles con el tiempo, pero a veces son necesarios cambios que no pueden ser compatibles. Una solución a estas necesidades opuestas es introducir el control de versiones de componentes agregando un número en la ruta de tipo de recurso y en los nombres de clase Java completos de sus implementaciones. Este número de versión representa una versión principal, tal como se define en las directrices [de versiones](https://semver.org/)semánticas, que se incrementa únicamente para los cambios que no son compatibles con versiones anteriores.

Si se realizan cambios incompatibles en los siguientes aspectos de los componentes, se generará una nueva versión de los mismos:

* Modelos Sling (siguiendo las directrices semánticas de versiones)
* Plantillas y secuencias de comandos HTL
* Marcado HTML y selectores CSS
* Representación JSON
* Cuadros de diálogo

Para obtener más información, consulte el documento de políticas [de](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) versiones en GitHub.

El control de versiones de componentes crea una forma de contrato que es importante para las actualizaciones, ya que aclara cuándo es necesario refactorizar algo. Consulte también la sección Compatibilidad de [actualización de las personalizaciones](customizing.md#upgrade-compatibility-of-customizations), que explica las consideraciones que requieren las distintas formas de personalización para una actualización.

Para evitar las dolorosas migraciones de contenido, es importante nunca señalar directamente a los componentes con versiones desde los recursos de contenido. Por regla general, una parte `sling:resourceType` del contenido nunca debe tener un número de versión, o para actualizar los componentes es necesario refactorizar también el contenido. La mejor manera de evitarlo es seguir el patrón [de componentes](#proxy-component-pattern) proxy descrito anteriormente.

### Interfaces de modelo {#model-interfaces}

Este patrón se refiere a la instrucción de HTL para que apunte a una interfaz de Java, mientras que la implementación del modelo de Sling también se está registrando en el tipo de recurso del componente. `data-sly-use`

Cuando se combina con el patrón [de componentes](#proxy-component-pattern) proxy descrito anteriormente, esta forma de ofertas de enlace de doble sigue puntos de extensión agradables:

1. Un sitio puede redefinir la implementación de un modelo Sling registrándolo en el tipo de recurso del componente proxy, sin tener que preocuparse por el archivo HTL, que aún puede apuntar a la interfaz.
1. Un sitio puede redefinir el marcado HTML de un componente sin tener en cuenta a qué lógica de implementación debe apuntar.

## Colocando todo juntos {#putting-it-all-together}

A continuación se muestra una descripción general de toda la estructura de enlace de tipo de recurso, tomando como ejemplo el componente principal de título. Muestra cómo un componente proxy específico del sitio permite resolver el control de versiones de componentes, para evitar que el recurso de contenido contenga un número de versión cualquiera. A continuación, muestra cómo se utiliza el archivo `title.html` HTL [del componente en la interfaz del modelo, mientras que la implementación se enlaza a la versión específica del componente mediante anotaciones del modelo](https://docs.adobe.com/content/help/es-ES/experience-manager-htl/using/overview.html) de [](https://sling.apache.org/documentation/bundles/models.html) sling.

![Información general de enlace de recursos](/help/assets/chlimage_1-32.png)

A continuación se muestra otra descripción general, que no muestra los detalles del POJO de implementación, pero revela cómo se hace referencia a [las plantillas y políticas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html) asociadas.

La `cq:allowedTemplates` propiedad indica qué plantillas se pueden utilizar para un sitio y `cq:template` indica a cada página cuál es la plantilla asociada. Cada plantilla consta de las tres partes siguientes:

* **estructura** : contiene los recursos que se forzará a que cada página esté presente y que el autor de la página no podrá eliminarla, como por ejemplo los componentes de encabezado y pie de página.
* **inicial** : contiene el contenido inicial que se duplicará en la página cuando se cree.
* **políticas** : contiene para cada componente la asignación a una política, que es la preconfiguración del componente. Esta asignación permite reutilizar las directivas en todas las plantillas y, por lo tanto, administrarlas de forma centralizada.

![Plantillas y descripción general de directiva](/help/assets/screen_shot_2018-12-07at093102.png)

## Tipo de archivo del proyecto AEM {#aem-project-archetype}

[El arquetipo](/help/developing/archetype/overview.md) del proyecto AEM crea un proyecto Adobe Experience Manager mínimo como punto de partida para sus propios proyectos, incluyendo un ejemplo de componentes HTML personalizados con SlingModels para la lógica y la correcta implementación de los componentes principales con el patrón proxy recomendado.

**Consulte lo siguiente:**

* [Uso de componentes](/help/get-started/using.md) principales: obtenga y ejecute los componentes principales en su propio proyecto.
* [Personalización de componentes](customizing.md) principales: para aprender a diseñar y personalizar los componentes principales.
