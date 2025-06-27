---
title: ¿Cómo obtener temáticas y plantillas de muestra para los componentes principales de AEM Forms?
description: Los componentes principales de AEM Forms proporcionan ejemplos de temáticas de formularios adaptables, plantillas y modelos de datos de formulario.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
level: Intermediate
exl-id: aef6e88b-dcae-4777-9893-9257d7702f43
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Temáticas, plantillas y modelos de datos de formulario de ejemplo {#sample-themes-templates-and-data-models}

Los componentes principales de [!DNL AEM Forms] proporcionan temáticas de ejemplo, plantillas y modelos de datos de formulario listos para usar para crear formularios adaptables versátiles rápidamente. También ayudan a los autores de formularios a conocer la extensibilidad, adaptabilidad y capacidad de respuesta de los [componentes principales de AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es) para crear fácilmente formularios simples en poco tiempo y formularios complejos mientras se conectan con la base de datos sin problemas.

Las temáticas, las plantillas y los modelos de datos de formulario incluidos en el paquete de contenido de referencia son los siguientes:

| Plantillas | Temáticas | Modelos de datos de formulario |
---------|----------|---------
| [Blank](#Blank) | [Lienzo](#Canvas) | Microsoft® Dynamics 365 |
| [Contáctenos](#Contact-Us) | [WKND](#WKND) | Salesforce |
| [Actualización de los detalles de contacto](#Contact-Details-Update) | [Caballete](#Easel) |   |
| [Formulario de consentimiento](#Consent-Form) | [FSI](#FSI) |  |
| [Solicitud de servicio de registro](#Log-Service-Request) | [Atención sanitaria](#Healthcare) |  |
| [Enviar comentarios](#Give-Feedback) |  |  |
| [Inscripción en beneficios](#Benefits-Enrollment) |  |   |
| [Resumen de los beneficios de empleados](#Employee-Benefits-Summary) |   |   |
| [Solicitud del extracto de cuenta](#Request-for-Account-Statement) |   |   |
| [Formulario de inspección de seguridad](#Safety-Inspection) |   |   |
| [Inspección de control de calidad](#Quality-Control-Inspection) |   |   |
| [Solicitud de compra](#Purchase-Request) |  |  |

{{traditional-aem}}

## Temáticas de ejemplo {#Sample-Themes}

Las temáticas de ejemplo de referencia ayudan a los autores a definir y personalizar el estilo de los formularios. Los autores que tengan incluso un conocimiento básico de CSS pueden personalizar la temática según los requisitos.

**¿Cómo obtener estas temáticas?**
Para obtener estas temáticas, siga los pasos que se indican a continuación para el entorno **AEM as a Cloud Service**:

1. [Habilite los componentes principales de formularios adaptables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=es)
1. [Implemente un proyecto AEM Archetype 47 en su entorno](https://github.com/adobe/aem-project-archetype)


Al implementar un arquetipo AEM, solo puede utilizar las temáticas OOTB en los formularios. Para personalizar las temáticas según sus necesidades, [Utilice la canalización front-end](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=es) para implementar las temáticas.

>[!NOTE]
>
> * Las temáticas no están disponibles en el entorno **AEM 6.5**.

<!--

1. **AEM 6.5**

    1. [Enable Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=es)
    1. [Deploy an AEM Archetype 47 or later project to your environment](https://github.com/adobe/aem-project-archetype)


    When you deploy an AEM Archetype, you can only use the OOTB themes in your forms, To customize the themes as per your requirements, [Use the front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=es) to deploy the themes.

-->


<!--

### Deploying an AEM Archetype 47 or later project to your environment {#using-archetype-to-deploy-themes}

You can get these themes by deploying an [AEM Archetype 47 or later](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

### Enable core components and use front-end pipeline to deploy themes {#use-front-end-pipeline-to-deploy-themes}

1. To get these themes on **Forms as a Cloud Service** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=es) and use the [front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=es) to deploy these themes.
    
1. To get these themes on **AEM 6.5 Forms** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=es) and use the [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=es) to deploy these themes.

[Learn to use and customize themes in AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=es). 

[Learn to use and customize themes in AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=es).

-->

Las temáticas **disponibles de forma predeterminada** de los [Componentes principales de formularios adaptables](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es) son los siguientes:

![Temas de OOTB](/help/adaptive-forms/assets/archetype-45-themes-1.png)

### Lienzo {#Canvas}

El lienzo es la temática predeterminada para formularios, y enfatiza el uso de colores básicos, transparencia e iconos planos. En la captura de pantalla siguiente, puede ver el aspecto del tema del lienzo.

![Temática Lienzo](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

La temática WKND encarna un diseño dinámico, imaginativo y atractivo para mostrar un aspecto elegante a sus formularios. La temática se basa en el aspecto y el estilo de [Sitio WKND](https://wknd.site/us/es.html) que es un sitio web de viajes y aventura basado en [Componentes principales de Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es).

![Tema WKND](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Caballete {#Easel}

La temática Caballete ayuda a crear un aspecto del formulario que es atractivo y fácil de configurar, está personalizado para la simplicidad y la facilidad de uso. El caballete es una temática que se basa en el concepto de un stand portátil utilizado por los artistas para apoyar un lienzo mientras trabajan en sus pinturas.

![Temática Caballete](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

### FSI (servicios financieros y seguros) {#FSI}

FSI es una temática que pone énfasis en darle a su formulario un aspecto limpio y práctico. El suave tono azul suave se aplica al formulario cuando se aplica la temática FSI, como se puede ver en la imagen.

![Temática FSI](/help/adaptive-forms/assets/fsi-theme-new1.png)


### Atención sanitaria {#Healthcare}

La temática para el sector sanitario emplea tonos vivo y verdes para acentuar elementos como pestañas, paneles, cuadros de texto y botones dentro del formulario.

![Temática de atención médica](/help/adaptive-forms/assets/healthcare-new-theme.png)


## Plantillas de muestra {#Sample-templates}

Las plantillas definen la estructura inicial del formulario, el contenido y las acciones que se duplicarán en él o utilizarán una estructura de plantilla similar a la del formulario, por ejemplo, un formulario de consentimiento, un formulario de inscripción en beneficios y mucho más.

**¿Cómo obtener estas plantillas?**

Puede obtener estas plantillas implementando [AEM Archetype 47 o versiones posteriores](https://github.com/adobe/aem-project-archetype) en su entorno **AEM Forms as a Cloud Service** o el entorno **AEM 6.5 Forms**.

<!--

>[!NOTE]
>
> * If you have [enabled core components and used front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes), you need not to deploy an AEM Archetype.
> * You can find list of all OOTB templates when you create a form.

-->


Las plantillas **disponibles de forma predeterminada** de [Componentes principales de formularios adaptables](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es) son los siguientes:

![Plantillas de referencia](/help/adaptive-forms/assets/reference-templates-core-components.png)

<!--

### Basic {#Basic}

A basic template helps you quickly create an enrollment experience form. You can also use it to preview the functionality of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es). It provides a wizard layout for section-by-section presentation of data.

![Basic Template](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

-->

### En blanco {#Blank}

Se utiliza una plantilla de lienzo en blanco para crear una estructura de formulario adaptable, contenido y reglas desde cero. No hay componentes de formulario incorporados previamente en la plantilla en blanco.

![Plantilla en blanco](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Contacto {#Contact-Us}

La plantilla de formulario Contacto se utiliza para crear un formulario para facilitar la comunicación entre los visitantes del sitio web y los administradores del formulario. Los usuarios pueden enviar consultas, comentarios o solicitudes de asistencia a través del formulario.

![Plantilla de contacto](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Actualización de los detalles de contacto {#Contact-Details-Update}

La plantilla de actualización de datos de contacto ayuda a los autores a crear un formulario para la actualización de la dirección y los datos de contacto de los clientes. El formulario también ayuda a los clientes a actualizar la información personal relacionada con la suscripción o los beneficios para garantizar una comunicación fluida y un acceso ininterrumpido a los servicios o beneficios.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Formulario de consentimiento {#Consent-Form}

La plantilla de formulario de consentimiento se utiliza para crear un formulario para obtener un documento legal de los participantes que participan en una actividad específica, estudio de investigación, procedimiento médico o cualquier situación en la que su información personal o sus derechos puedan estar involucrados. El formulario garantiza la transparencia, protege los derechos del participante y establece una comprensión clara de lo que el individuo está de acuerdo.

![Formulario de consentimiento](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Solicitud de servicio de registro {#Log-Service-Request}

La plantilla de solicitud del servicio de registro ayuda a crear un formulario que solicita servicios de registro específicos de un proveedor de servicios. El formulario sirve como solicitud formal para crear un ticket para eventos, actividades o datos registrados para la monitorización o el seguimiento del estado.

![Plantilla de solicitud de servicio de registro](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Enviar comentarios {#Give-Feedback}

La plantilla del formulario Enviar comentarios crea un formulario para proporcionar comentarios constructivos a otra persona o equipo. El formulario garantiza que los comentarios sean claros, específicos y procesables, lo que promueve la comunicación abierta y la mejora.

![Plantilla para enviar comentarios](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Inscripción en beneficios {#Benefits-Enrollment}

La plantilla de formulario de inscripción en beneficios se utiliza para crear un formulario para recopilar información esencial de sus empleados sobre sus beneficios preferidos y las opciones de cobertura. Por lo general, acompaña al período anual de inscripción en las prestaciones.

![Plantilla de inscripción en beneficios](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Resumen de los beneficios de empleados {#Employee-Benefits-Summary}

La plantilla del formulario Resumen de los beneficios de empleados se utiliza para crear un formulario con el fin de recopilar detalles esenciales sobre los beneficios de una persona. Ayuda a evaluar la cobertura de forma rápida y precisa y proporciona una visión general completa para asistencia y soporte eficientes.
![Resumen de los beneficios de empleados](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Solicitud de extracto de cuenta {#Request-for-Account-Statement}

La plantilla de solicitud de extracto de cuenta ayuda a crear un formulario que inicia el proceso de obtención de un extracto preciso y actualizado de los clientes.  La declaración proporciona un registro detallado de transacciones financieras, actividades u otra información relevante acerca de los clientes que usan este formulario.

![Request-for-account-statement](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Inspección de seguridad {#Safety-Inspection}

La plantilla del formulario Inspección de seguridad crea un formulario para introducir detalles para un entorno de trabajo seguro. Mediante la realización de inspecciones periódicas utilizando este formulario, pueden identificarse los peligros potenciales. El formulario cubre varios aspectos, como salidas de emergencia, seguridad contra incendios, seguridad eléctrica, materiales peligrosos, equipo de protección personal, ergonomía de la estación de trabajo para la seguridad y el bienestar de los empleados, visitantes y clientes.

![Formulario de inspección de seguridad](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Inspección del control de calidad {#Quality-Control-Inspection}

La plantilla de formulario de inspección de control de calidad se utiliza para crear un formulario para evaluar y documentar el aspecto visual, las dimensiones, la funcionalidad, la documentación, los resultados de las pruebas y la calidad general de un producto o elemento. Ayuda a identificar defectos, incumplimientos y acciones correctivas necesarias para garantizar el cumplimiento de los estándares de calidad.

![Inspección del control de calidad](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Solicitud de compra {#Purchase-Request}

La plantilla del formulario de solicitud de compra crea un formulario para iniciar el proceso de adquisición y permitir a los empleados solicitar formalmente la compra de los bienes o servicios necesarios para su trabajo. El formulario captura detalles esenciales como la descripción del artículo, la cantidad, el proveedor preferido (si corresponde), la asignación del presupuesto, la justificación de la compra, la información de entrega y las aprobaciones requeridas.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Modelos de datos de formulario de referencia {#reference-models}

Después de crear un formulario adaptable basado en [Componente principal](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=es), puede conectar el formulario con la base de datos de los servidores de Microsoft® Dynamics 365 y Salesforce para habilitar los flujos de trabajo empresariales. Por ejemplo:

* Escriba los datos en Microsoft® Dynamics 365 y Salesforce al enviar los formularios adaptables.
* Escriba los datos en Microsoft® Dynamics 365 y Salesforce a través de entidades personalizadas definidas en el modelo de datos de formulario y viceversa.
* Consulte el servidor de Microsoft® Dynamics 365 y Salesforce para obtener los datos y rellenar previamente formularios adaptables.
* Lea los datos del servidor de Microsoft® Dynamics 365 y Salesforce.

Puede obtener los siguientes modelos de datos de formulario instalando el [Paquete de contenido de referencia](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/es/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip):

* Microsoft® Dynamics 365
* Salesforce

Para obtener información sobre el uso de estos modelos, consulte la [Configuración de los servicios en la nube de Microsoft® Dynamics 365 y Salesforce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html?lang=es#configure-dynamics-cloud-service)
