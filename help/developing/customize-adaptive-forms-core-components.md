---
title: Personalizar los componentes principales de los formularios adaptables
description: Descubra cómo ampliar o crear un componente principal de formularios adaptables para implementar funciones a medida para su organización.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 79cedf7099e2dc267a4cb1c25c06d4f0460367b2
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 100%

---

# Personalizar los componentes principales de los formularios adaptables

La personalización de los componentes principales de los formularios adaptables le permite ajustar las funcionalidades preconfiguradas a sus necesidades específicas. Esta guía le mostrará el proceso de personalización de estos componentes con el fin de crear una experiencia más personalizada.

## Requisito previo

Antes de empezar a personalizar los componentes principales de los formularios adaptables,

* Obtenga información acerca de la [arquitectura de los componentes principales](customizing.md#customizing-the-markup-customizing-the-markup) y consulte la [documentación oficial de los componentes principales de Adobe Experience Manager](customizing.md). Estos recursos exhaustivos le servirán de guía a lo largo del proceso de personalización.
* Configure su entorno de desarrollo. Esto garantiza un flujo de trabajo sin complicaciones para realizar cambios en los componentes principales. Al configurar el entorno de desarrollo, utilice un tipo de archivo del proyecto AEM basado en el último tipo de archivo del proyecto AEM. En función de su entorno, puede hacer lo siguiente:

   * [Configurar un entorno de desarrollo local para Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html?lang=es).
   * [Configurar un entorno de desarrollo local para AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=es)

## Personalizar un componente principal de formularios adaptables

Siga los pasos que aparecen a continuación para modificar la apariencia, el comportamiento y la funcionalidad de un componente principal de formularios adaptables.

1. **Identificar y duplicar el componente principal**

   Al configurar el entorno de desarrollo, usted ha creado un proyecto basado en el tipo de archivo. En el proyecto de tipo de archivo de AEM, identifique el componente principal específico que desea personalizar. Una vez identificado, cree un duplicado del componente en su proyecto basado en el tipo de archivo de AEM. Manténgalo en paralelo con otros componentes principales de formularios adaptables. Este paso garantiza que sus esfuerzos de personalización no afecten al componente original, permitiéndole experimentar con total libertad.

1. **Personalizar el componente copiado**

   Abra el componente duplicado y empiece a realizar las modificaciones pertinentes según sus necesidades:

   * **Personalizar la estructura HTML**: adapte la estructura HTML a sus necesidades de diseño, sin dejar de respetar las prácticas de estilo [BEM (Modificador de elementos de bloque)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) para conseguir un código escalable y fácil de mantener.
   * **Actualizar etiqueta**: actualice la etiqueta del componente para proporcionar un nombre claro y descriptivo para la versión personalizada. Consulte la [plantilla de etiqueta OOTB (predeterminada)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) suministrada para mantener la uniformidad.
   * **Personalizar widget**: ajuste el widget utilizado dentro del componente (menús desplegables, casillas de verificación) para adaptarlo a su caso de uso específico. Consulte la [implementación de widgets de muestra](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) como referencia.
   * **Texto de ayuda e información sobre herramientas**: personalice el texto de ayuda o la información sobre herramientas asociada al componente para ofrecer contexto y orientación a los usuarios. Utilice la [Plantilla de texto de ayuda OOTB](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) como punto de partida.
   * **Atributos de datos**: incorpore todos los atributos de datos necesarios en los elementos HTML del componente. Estos atributos son fundamentales para el correcto funcionamiento del componente durante la ejecución. Consulte la [documentación](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) para comprender la función de los atributos de datos en los componentes principales de formularios adaptables.

1. **Implementar la lógica de back-end**

   Si su personalización requiere una lógica de back-end, puede ampliar los modelos de Sling existentes. Consulte el [ejemplo](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) proporcionado para integrar a la perfección la funcionalidad deseada en su componente personalizado.

1. **Configurar el cuadro de diálogo del componente**

   Configure el cuadro de diálogo asociado a su componente personalizado. Utilice el [cuadro de diálogo del componente](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) de ejemplo proporcionado en la documentación para garantizar que las interacciones y la configuración del usuario se administran adecuadamente.

1. **Implementar y probar el componente en su entorno de desarrollo local**

   Utilice [Maven para generar e implementar el componente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=es#building-and-installing) en su entorno de desarrollo local. Una vez implementado el componente, cree un formulario adaptable para probar el componente personalizado.

1. **Implementar el componente personalizado en el entorno de producción**

   Una vez probado el componente en su entorno de desarrollo local, impleméntelo en los entornos de producción.
