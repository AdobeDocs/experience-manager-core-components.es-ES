---
title: 'Componente principal de Forms adaptable: contenedor de formularios'
description: Agregar un formulario adaptable a una página web.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 3%

---


# Contenedor del formulario {#form-container-adaptive-forms-core-component}

Forms permite que los visitantes del sitio web interactúen con el sitio web proporcionando información valiosa, lo que puede aumentar la participación y la satisfacción del usuario. Un contenedor de formularios adaptables en Adobe Experience Manager (AEM) Sites permite a los propietarios de sitios web agregar fácilmente formularios a sus páginas. Esto ayuda a facilitar la comunicación entre los visitantes del sitio web y el propietario u organización del sitio web, ya que proporciona una manera optimizada para que los visitantes proporcionen comentarios, realicen consultas y realicen otras acciones.

## Uso {#reasons-to-use-forms-container}

Existen varias razones por las que se puede agregar un formulario a un sitio web:

* **Recopilación de datos**: Forms se puede utilizar para recopilar datos de visitantes de sitios web con distintos fines, como investigación de mercado, análisis de comportamiento de los usuarios, etc.

* **Generación de posibles clientes**: Se puede utilizar un formulario para recopilar información de clientes potenciales, como el nombre y la dirección de correo electrónico, para generar posibles clientes en los esfuerzos de marketing y ventas.

* **Comercio electrónico**: Forms puede utilizarse para realizar compras en línea, lo que permite a los clientes realizar pedidos y realizar pagos a través del sitio web.

* **Contacto**: Un formulario de contacto permite a los visitantes del sitio web comunicarse fácilmente con el propietario o la organización del sitio web.

* **Encuestas y encuestas**: Forms se puede usar para recopilar comentarios y opiniones de visitantes de sitios web a través de encuestas y encuestas.

* **Registro de eventos**: Forms se puede usar para el registro de eventos, lo que permite a los visitantes del sitio web registrarse en eventos o seminarios web.

* **Suscripciones**: Forms se puede utilizar para suscripciones a sitios web, lo que permite a los visitantes registrarse en un boletín informativo u otras comunicaciones regulares.

* **Autenticación de usuarios**: Forms se puede utilizar para la autenticación de usuarios, lo que permite a los visitantes de un sitio web crear cuentas e iniciar sesión para acceder a contenido o funciones exclusivos.

* **Aumentar tasa de conversión**: Un formulario bien diseñado puede aumentar la tasa de conversión al facilitar a los usuarios la realización de las acciones deseadas, como la compra de un producto o la suscripción a un servicio.


## Versión y compatibilidad {#version-and-compatibility}

El componente principal del contenedor de Forms adaptable se lanzó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del contenedor de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor de formularios para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de contenedor de formularios con facilidad para una experiencia de usuario perfecta.

### Ficha básica {#basic-tab}

![Ficha Básico](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Servicios de precarga** - Esta opción permite al usuario seleccionar un servicio de rellenado previo para recuperar datos cuando se procesa el formulario adaptable. Más información sobre [cómo crear y configurar un servicio de relleno previo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **Categoría de biblioteca de cliente** - El usuario puede configurar la biblioteca JavaScript personalizada por formulario adaptable. Se recomienda mantener solo las funciones reutilizables en la biblioteca de , que tienen dependencia de las bibliotecas de terceros jquery y underscore.js .

### Pestaña Envío {#submission-tab}

![Ficha Envío](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Los usuarios pueden configurar distintas acciones para los envíos de formularios adaptables.

* **Dirección URL/ruta de redireccionamiento** : esta opción permite al usuario configurar una página para cada formulario, a la que se redirige a los usuarios después de enviar un formulario adaptable. Haga clic aquí para obtener más información sobre [configuración de páginas de redireccionamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Mostrar ficha Mensaje](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Mostrar mensaje** - Esta opción permite a los usuarios agregar un mensaje que se muestra cuando el formulario adaptable se envía correctamente. El texto predefinido se incluye en el cuadro de diálogo y el usuario puede modificarlo. El cuadro de diálogo Mostrar mensaje admite herramientas de formato de texto enriquecido que permiten a los usuarios dar formato al texto agregado.

* **Enviar acción** - Se activa una acción de envío cuando un usuario hace clic en el botón Enviar de un formulario adaptable. Los usuarios pueden seleccionar Enviar acciones en la lista desplegable que se admiten de forma predeterminada. Obtenga información sobre cómo [configurar una acción de envío en la ficha Envío](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).




