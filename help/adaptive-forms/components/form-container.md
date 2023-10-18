---
title: 'Componente principal de formularios adaptables: contenedor de formulario'
description: Agregue un formulario adaptable a una página web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 100%

---

# Contenedor del formulario {#form-container-adaptive-forms-core-component}

Los formularios permiten a los visitantes interactuar con el sitio web proporcionando información valiosa, lo que puede aumentar la participación y la satisfacción del usuario. Un contenedor de formulario adaptable en Adobe Experience Manager (AEM) Sites permite a los propietarios de sitios web agregar fácilmente formularios a sus páginas. Esto ayuda a facilitar la comunicación entre los visitantes del sitio web y su propietario u organización, ya que proporciona una manera optimizada para que los visitantes proporcionen comentarios, hagan consultas y otras acciones.

## Uso {#reasons-to-use-forms-container}

Existen varias razones por las que se puede agregar un formulario a un sitio web:

* **Recopilación de datos**: los formularios pueden utilizarse para recopilar datos de los visitantes de un sitio web con diversos fines, como estudios de mercado, análisis de comportamiento, etc.

* **Generación de posibles clientes**: se puede utilizar un formulario para recopilar información de clientes potenciales, como el nombre y la dirección de correo electrónico, para generar posibles clientes para marketing y ventas.

* **Comercio electrónico**: los formularios pueden servir para comprar en línea, lo que permite a los clientes efectuar pedidos y pagos a través del sitio web.

* **Contacto**: un formulario de contacto permite a los visitantes del sitio web comunicarse fácilmente con el propietario o la organización del sitio web.

* **Encuestas y sondeos**: los formularios pueden usarse para recopilar comentarios y opiniones de visitantes de sitios web a través de encuestas y sondeos.

* **Registro de eventos**: los formularios se pueden destinar al registro en eventos, para que los visitantes del sitio web puedan inscribirse en eventos o seminarios web.

* **Suscripciones**: los formularios pueden emplearse para suscripciones a sitios web, lo que permite a los visitantes suscribirse a una newsletter u otras comunicaciones periódicas.

* **Autenticación de usuarios**: los formularios pueden funcionar para la autenticación de usuarios, lo que permite a los visitantes del sitio web crear cuentas e iniciar sesión para acceder a contenidos o funciones exclusivas.

* **Aumentar tasa de conversión**: un formulario bien diseñado puede aumentar la tasa de conversión al facilitar a los usuarios la realización de las acciones deseadas, como la compra de un producto o la suscripción a un servicio.


## Versión y compatibilidad {#version-and-compatibility}

El componente principal de acordeón de formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o posteriores |
|---|---|---|
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de contenedor de formulario adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor de formularios para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de contenedor de formularios con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **Servicios de rellenado previo**: esta opción permite al usuario seleccionar un servicio de rellenado previo para recuperar datos cuando se procesa el formulario adaptable. Más información acerca de [cómo crear y configurar un servicio de rellenado previo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=es#aem-forms-custom-prefill-service).

* **Categoría de biblioteca de cliente**: el usuario puede configurar la biblioteca JavaScript personalizada por formulario adaptable. Se recomienda mantener solo las funciones reutilizables en la biblioteca, que tienen dependencia de las bibliotecas de terceros jquery y underscore.js.

### Pestaña Envío {#submission-tab}

![Pestaña Envío](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Los usuarios pueden configurar distintas acciones para los envíos de formularios adaptables.

* **Ruta/URL de redireccionamiento**: esta opción permite al usuario configurar una página para cada formulario, a la que se redirige a los usuarios después de enviar un formulario adaptable. Haga clic aquí para obtener más información sobre [configuración de páginas de redireccionamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=es).

![Pestaña Mostrar mensaje](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Mostrar mensaje**: esta opción permite a los usuarios agregar un mensaje que se muestra cuando el formulario adaptable se envía correctamente. El texto predefinido se incluye en el cuadro de diálogo y el usuario puede modificarlo. El cuadro de diálogo Mostrar mensaje admite herramientas de formato de texto enriquecido que permiten a los usuarios dar formato al texto agregado.

* **Acción de envío**: se activa una acción de envío cuando un usuario hace clic en el botón Enviar en un formulario adaptable. Los usuarios pueden seleccionar acciones de envío en la lista desplegable que se admiten de forma predeterminada. Obtenga información sobre cómo [configurar una acción de envío en la pestaña Envío](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=es#supporting-custom-functions-in-validation-expressions-br).

## Artículo relacionado {#related-article}

* [Creación de un formulario adaptable en una página de AEM Sites o un fragmento de experiencia](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=es)

* [Creación de un formulario adaptable independiente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es)


>[!MORELIKETHIS]
>
>* [Acordeón](/help/adaptive-forms/components/accordion.md)
>* [Botón](/help/adaptive-forms/components/button.md)
>* [Grupo de casillas de verificación](/help/adaptive-forms/components/checkbox-group.md)
>* [Selector de fecha](/help/adaptive-forms/components/date-picker.md)
>* [Lista desplegable](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de correo electrónico](/help/adaptive-forms/components/email-input.md)
>* [Archivo adjunto](/help/adaptive-forms/components/file-attachment.md)
>* [Pie de página](/help/adaptive-forms/components/footer.md)
>* [Encabezado](/help/adaptive-forms/components/header.md)
>* [Pestañas horizontales](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagen](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Contenedor de panel](/help/adaptive-forms/components/panel-container.md)
>* [Botón de opción](/help/adaptive-forms/components/radio-button.md)
>* [Botón Restablecer](/help/adaptive-forms/components/reset-button.md)
>* [Botón Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de teléfono](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Asistente](/help/adaptive-forms/components/wizard.md)

## Vea también {#see-also}

{{see-also}}