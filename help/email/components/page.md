---
title: Componente de página de correo electrónico
description: El componente Página de correo electrónico
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 40%

---


# Componente de página de correo electrónico {#email-page-component}

El componente Página de correo electrónico es un componente de página ampliable diseñado para trabajar con la variable [editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y permite que el encabezado y pie de página y los componentes de estructura se ensamblen con el editor de plantillas, diseñado para crear contenido de Adobe Campaign.

## Uso {#usage}

El componente Página de correo electrónico constituye la base de todas las páginas diseñadas con los componentes principales de correo electrónico y las plantillas editables. Mediante el componente Página de correo electrónico , los encabezados, pies de página y la estructura de la página se pueden definir como una plantilla con los demás componentes principales de correo electrónico.

* Al usar la variable [diálogo de diseño,](#design-dialog) se pueden definir bibliotecas personalizadas del lado del cliente para la página.
* A diferencia de otros componentes que tienen un cuadro de diálogo de edición accesible directamente desde el componente, dado que el componente Página de correo electrónico es la propia página, la variable [cuadro de diálogo editar](#edit-dialog) del componente Página de correo electrónico es la ventana de propiedades de página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de página de correo electrónico es v1, que se introdujo con la versión X de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales de correo electrónico, consulte el documento [Versiones de componentes principales de correo electrónico](/help/email/versions.md)

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de página [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

Dado que el componente representa la página completa, la configuración que normalmente estaría en un cuadro de diálogo de edición se encuentra en la ventana [Propiedades de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=es).

### Pestaña Cloud Services {#cloud-services}

Para que los componentes principales de correo electrónico puedan recuperar las variables y los datos de campaña, la página debe estar vinculada a una configuración de Adobe Campaign.

![Propiedades de página de correo electrónico](/help/email/assets/email-page-properties.png)

En **Configuración del Cloud Service** , en la lista desplegable seleccione **Agregar configuración**.

En **Adobe Campaign** seleccione la configuración para la integración con Adobe Campaign.

Consulte el documento [Uso de los componentes principales de correo electrónico](/help/email/using.md) para obtener más información sobre la configuración de los componentes principales de correo electrónico.

### Ficha Correo electrónico {#email-tab}

La pestaña Email define las propiedades de los correos electrónicos enviados mediante Adobe Campaign en función del contenido de esta página, como el asunto del correo electrónico y el contenido de texto sin formato.

![Propiedades de página de correo electrónico](/help/email/assets/email-page-properties-email.png)

* **Asunto** - El asunto del correo electrónico enviado por Adobe Campaign basado en esta página
   * Haga clic en el **Seleccione la variable Adobe Campaign** para abrir [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **Encabezado previo**
   * Haga clic en el **Seleccione la variable Adobe Campaign** para abrir [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **Texto sin formato** - Versión de texto sin formato del correo electrónico enviado por Adobe Campaign
   * Haga clic en el **Seleccione la variable Adobe Campaign** para abrir [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **Url De Referencia**

## Cuadro de diálogo de diseño {#design-dialog}

Dado que el componente representa la página completa, se accede al cuadro de diálogo de diseño a través de **Información de página -> Política de página** al editar la plantilla de página.

![Política de la página](/help/assets/page-policy.png)

### Pestaña Propiedades {#properties-tab}

Con la ventana Diseño de página, puede definir las bibliotecas de cliente que se van a cargar, así como la biblioteca de recursos web para la página.

![Cuadro de diálogo de diseño de los componentes de la página de correo electrónico](/help/email/assets/email-page-design.png)

* **Bibliotecas de cliente**: define las categorías de biblioteca de cliente que se van a cargar. JavaScript se agrega al final del cuerpo y CSS se agrega al encabezado de la página.
* **Cabecera de página JavaScript de bibliotecas de clientes** : define las categorías de la biblioteca de cliente JavaScript que se cargarán en el encabezado de página.
   * Las categorías definidas aquí que también están presentes en el campo **Bibliotecas de cliente** tendrán JavaScript cargado en el encabezado de la página en lugar de en el final del cuerpo.
   * No se cargará CSS a menos que la categoría también esté presente en el campo **Bibliotecas de cliente**.
* **Carga asíncrona de bibliotecas JavaScript** - Si está habilitado, las bibliotecas de JavaScript personalizadas se cargarán asincrónicamente.
* **Biblioteca de cliente de recursos web**: categoría de la biblioteca de cliente que se usa para publicar recursos web, como los iconos favoritos.
* **Saltar al selector de elementos de contenido principal**: se utiliza como función de accesibilidad para saltar directamente al contenido principal de la página

Las bibliotecas se pueden configurar para los campos **Bibliotecas de cliente** y **Encabezado de página de bibliotecas de cliente de JavaScript** de la siguiente manera:

* Para agregar un nuevo campo, toque o haga clic en el botón **Agregar** debajo de los campos.
* Para quitar un campo, toque o haga clic en el icono de la papelera situado junto al campo que desea eliminar.
* Para reorganizar el orden de carga, arrastre el controlador situado junto al campo que desee mover.

Para obtener más información sobre el uso de bibliotecas del lado del cliente, consulte [Uso de bibliotecas del cliente.](https://helpx.adobe.com/es/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Pestaña Estilos {#styles-tab}

El componente Página es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
