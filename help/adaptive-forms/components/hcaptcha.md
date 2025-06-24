---
title: hCaptcha en AEM Adaptive Forms
description: Mejore la seguridad sin esfuerzo con el servicio hCaptcha®. Guía paso a paso en el interior
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---


# Componente hCaptcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Esta función se encuentra en el programa para primeros usuarios. Puede escribir a aem-forms-ea@adobe.com desde su ID de correo electrónico oficial para unirse al programa de primeros usuarios y solicitar acceso a esta funcionalidad. </span>

El servicio hCaptcha® protege sus formularios de bots, correos no deseados y abusos automatizados. Plantea un desafío tipo Widget de la casilla de verificación y evalúa la respuesta del usuario para determinar si es un humano o un bot el que interactúa con el formulario. Evita que el usuario continúe si la prueba falla y ayuda a que las transacciones en línea sean seguras al impedir que los bots publiquen contenido no deseado o actividades maliciosas.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

{{traditional-aem}}

## Uso {#usage}

Existen varias razones por las que resulta beneficioso incluir un desafío hCaptcha en el proceso de envío de un formulario, son estas:

- **Prevención de bots**: garantiza que el formulario lo está enviando un humano, lo que reduce los correos no deseados y los envíos automatizados.

- **Seguridad**: añade una capa adicional de seguridad, que verifica la legitimidad de cada envío de formulario y protege contra ataques maliciosos.

- **Integridad de datos**: al evitar envíos múltiples o fraudulentos, ayuda a mantener la integridad y la precisión de los datos recopilados a través del formulario.

- **Verificación del usuario**: verifica la identidad del usuario que envía el formulario, lo que garantiza que solo los usuarios autenticados puedan llevar a cabo transacciones confidenciales.

- **Administración de carga**: ayuda a administrar la carga del servidor controlando la tasa de envíos de formularios, lo que evitaría la sobrecarga del sistema durante los periodos de mucho tráfico.

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente hCaptcha en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

Especifique las propiedades del componente hCaptcha en el [cuadro de diálogo de configuración](#configure-dialog). El cuadro de diálogo de configuración forma parte de los componentes principales que logran facilitar la generación de formularios y proporcionar una forma eficaz de crear formularios complejos.

## Versión y compatibilidad {#version-and-compatibility}


El componente hCaptcha de formularios adaptables se publicó en mayo de 2024 como parte de [Componentes principales 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente las propiedades del componente hCaptcha en su cuadro de diálogo de configuración, donde se incluyen una Ficha básica y una pestaña Validación para personalizar las distintas propiedades.

### Pestaña Básicos {#basic-tab}

- **[!UICONTROL Nombre]:** especifique el nombre del componente hCaptcha, puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas.
- **[!UICONTROL Título]:** especifique el título del componente hCaptcha.
- **[!UICONTROL Ajustes de configuración]:** seleccione una configuración de nube configurada para hCaptcha®.
- **Tamaño de Captcha:** puede seleccionar el tamaño de visualización del cuadro de diálogo de desafío de hCaptcha®. Utilice la opción **[!UICONTROL Compacto]** para mostrar un tamaño pequeño y la opción **[!UICONTROL Normal]** para mostrar un cuadro de diálogo de desafío de hCaptcha® de tamaño relativamente grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Ficha básica de hCaptcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Pestaña Validación {#validation-tab}

- **[!UICONTROL Mensaje de validación]:** proporcione un mensaje de validación para la validación de Captcha en el envío del formulario.
- **[!UICONTROL Mensaje de validación de secuencia de comandos]**: utilice esta opción para introducir un mensaje con indicaciones si fallara la validación de la secuencia de comandos.

  ![Pestaña Validación de hCaptcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® es una marca comercial registrada de Intuition Machines, Inc.**

**Más información** acerca de otros **Componentes Captcha** y sus servicios, como:

- [Uso de hCaptcha en un formulario adaptable para componentes principales](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [Uso de hCaptcha en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Uso de Turnstile CAPTCHA en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Uso de Google reCAPTCHA en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
