---
title: Personalizar componentes principales de Forms adaptables
description: Aprenda a ampliar o crear un componente principal de Forms adaptable para implementar una funcionalidad adaptada a su organización.
role: Architect, Developer, Admin
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# Personalizar componentes principales de Forms adaptables

La personalización de los componentes principales de Forms adaptables le permite adaptar las funcionalidades integradas para adaptarlas a sus necesidades específicas. Esta guía lo acompaña durante el proceso de personalización de estos componentes para crear una experiencia más personalizada.

## Requisito previo

Antes de sumergirse en la personalización de los componentes principales de Forms adaptables,

* Obtenga información acerca de [arquitectura de los componentes principales](customizing.md#customizing-the-markup-customizing-the-markup) y pasar por el [Documentación oficial de los componentes principales de Adobe Experience Manager](customizing.md). Estos completos recursos sirven como guía durante todo el proceso de personalización.
* Configure su entorno de desarrollo Esto garantiza un flujo de trabajo suave para realizar cambios en los componentes principales. AEM AEM Al configurar el entorno de desarrollo, utilice un proyecto de tipo de archivo basado en el proyecto de tipo de archivo más reciente de la. En función de su entorno, puede:

   * [Configuración de un entorno de desarrollo local para Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [AEM Configuración de un entorno de desarrollo local para Forms de 6.5](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=es)

## Personalización de un componente principal de Forms adaptable

Siga los pasos a continuación para modificar el aspecto, el comportamiento y la funcionalidad de un componente principal de Forms adaptable.

1. **Identificar y duplicar el componente principal**

   Al configurar el entorno de desarrollo, ha creado un proyecto basado en el tipo de archivo. AEM En el proyecto de tipo de archivo de, identifique el componente principal específico que desea personalizar. AEM Una vez identificado, cree un duplicado del componente dentro del proyecto basado en el tipo de archivo de la. Manténgalo en paralelo a otros componentes principales de Forms adaptable. Este paso garantiza que los esfuerzos de personalización no afecten al componente original, lo que le permite experimentar libremente.

1. **Personalización del componente copiado**

   Abra el componente duplicado y empiece a realizar las modificaciones necesarias según sus necesidades:

   * **Personalizar estructura de HTML**: adapte la estructura del HTML para adaptarla a sus necesidades de diseño mientras se adhiere a [BEM (modificador de elemento de bloque)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) prácticas de estilo para código escalable y mantenible.
   * **Actualizar etiqueta**: Actualice la etiqueta del componente para proporcionar un nombre claro y descriptivo para la versión personalizada. Consulte la documentación proporcionada [Plantilla de etiqueta OOTB (predeterminada)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) para mantener la coherencia.
   * **Personalizar widget**: ajuste el widget utilizado dentro del componente (menús desplegables, casillas de verificación) para alinearlo con el caso de uso específico. Consulte la [implementación del widget de muestra](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) como referencia.
   * **Texto de ayuda e información sobre herramientas**: personalice el texto de ayuda o la información de herramientas asociada al componente para ofrecer contexto y orientación a los usuarios. Utilice el [Plantilla de texto de ayuda de OOTB](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) como punto de partida.
   * **Atributos de datos**: Incorpore todos los atributos de datos necesarios dentro de los elementos HTML del componente. Estos atributos son cruciales para el correcto funcionamiento del componente durante la ejecución. Consulte la [documentación](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) para comprender la función de los atributos de datos en los componentes principales de Forms adaptable.

1. **Implementar lógica back-end**

   Si la personalización requiere lógica back-end, puede ampliar los modelos de Sling existentes. Consulte la documentación proporcionada [ejemplo](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) para integrar sin problemas la funcionalidad deseada en el componente personalizado.

1. **Configuración del cuadro de diálogo del componente**

   Configure el cuadro de diálogo asociado al componente personalizado. Utilice el ejemplo [diálogo de componentes](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) se proporciona en la documentación para garantizar que las interacciones y la configuración del usuario se gestionen correctamente.

1. **Implementar y probar el componente en el entorno de desarrollo local**

   Uso [maven para crear e implementar el componente](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) en su entorno de desarrollo local. Una vez implementado el componente, cree un formulario adaptable para probar el componente personalizado.

1. **Implementar el componente personalizado en el entorno de producción**

   Después de probar el componente en el entorno de desarrollo local, impleméntelo en los entornos de producción.

