---
title: AEM Chcaptcha en Forms adaptable de
description: Mejore la seguridad de los formularios con el servicio hCaptcha&reg; sin esfuerzo. Guía paso a paso en el interior
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: 08d44e4db42594fb5aaf33d7d42df6fe19c70f59
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 17%

---

# Componente Captcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Esta función se encuentra en el Programa para usuarios que la adoptaron por anticipado. Puede escribir a aem-forms-ea@adobe.com desde su ID de correo electrónico oficial para unirse al programa de primeros usuarios y solicitar acceso a esta funcionalidad. </span>

El servicio Captcha® protege sus formularios de bots, spam y abusos automatizados. Plantea un desafío de widget de casilla de verificación y evalúa la respuesta del usuario para determinar si es un humano o un bot que interactúa con el formulario. Evita que el usuario continúe si la prueba falla y ayuda a que las transacciones en línea sean seguras al impedir que los bots publiquen contenido no deseado o actividades malintencionadas.

![Captcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Uso {#usage}

Existen varias razones por las que es beneficioso incluir un desafío Chcaptcha en un proceso de envío de formularios, estas son:

- **Prevención de bots**: garantiza que el formulario lo envíe un usuario, lo que reduce el correo no deseado y los envíos automatizados.

- **Seguridad**: agrega una capa adicional de seguridad, que verifica la legitimidad de cada envío de formulario y protege contra ataques maliciosos.

- **Integridad de datos**: Al evitar envíos múltiples o fraudulentos, ayuda a mantener la integridad y precisión de los datos recopilados a través del formulario.

- **Verificación del usuario**: verifica la identidad del usuario que envía el formulario, lo que garantiza que solo los usuarios autenticados puedan completar transacciones confidenciales.

- **Administración de carga**: ayuda a administrar la carga del servidor controlando la tasa de envíos de formularios, lo que evita la sobrecarga del sistema durante los períodos de alto tráfico.

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente Captcha en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

Especifique las propiedades del componente Captcha utilizando el [diálogo de configuración](#configure-dialog). El cuadro de diálogo de configuración forma parte de los componentes principales creados para facilitar la creación de los formularios y proporcionar una forma eficaz de crear formularios complejos.

## Versión y compatibilidad {#version-and-compatibility}


El componente hCaptcha de Forms adaptable se publicó en mayo de 2024 como parte de [Componentes principales 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente las propiedades del componente Captcha con su cuadro de diálogo de configuración que tiene una pestaña básica y una pestaña de validación para personalizar varias propiedades.

### Pestaña Básicos {#basic-tab}

- **[!UICONTROL Nombre]:** Especifique el nombre del componente Captcha, puede identificar fácilmente un componente del formulario con su nombre único tanto en el formulario como en el editor de reglas.
- **[!UICONTROL Título]:** Especifique el título del componente Captcha.
- **[!UICONTROL Ajustes de configuración]:** Seleccione una Configuración de nube configurada para Chcaptcha®.
- **Tamaño de Captcha:** Puede seleccionar el tamaño de visualización del cuadro de diálogo de desafío hCaptcha®. Utilice el **[!UICONTROL Compacto]** opción para mostrar un tamaño pequeño y el **[!UICONTROL Normal]** opción para mostrar un cuadro de diálogo de desafío hCaptcha® de tamaño relativamente grande.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Ficha básica de Captcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Pestaña Validación {#validation-tab}

- **[!UICONTROL Mensaje de validación]:** Proporcione un mensaje de validación para la validación de Captcha en el envío del formulario.
- **[!UICONTROL Mensaje de validación de script]** : Utilice esta opción para introducir un mensaje de solicitud si falla la validación de la secuencia de comandos.

  ![Pestaña Validación de Captcha](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**Captcha® es una marca comercial registrada de Intuition Machines, Inc.**

**Más información** acerca de otros **Componentes Captcha** y sus servicios, como:

- [Uso de Chcaptcha en un formulario adaptable para componentes principales](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Utilizar Chcaptcha en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [Usar CAPTCHA de torniquete en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Usar Google reCAPTCHA en un formulario adaptable para componentes de base](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}