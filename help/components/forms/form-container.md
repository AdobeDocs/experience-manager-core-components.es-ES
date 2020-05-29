---
title: Componente Contenedor de formulario
description: El componente Contenedor de formularios de componentes principales permite crear formularios de envío simples.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 3%

---


# Componente Contenedor de formulario {#form-container-component}

El componente Contenedor de formularios de componentes principales permite crear formularios de envío simples.

## Uso {#usage}

El componente Contenedor del formulario permite crear formularios y funciones de envío de información simples mediante la compatibilidad con formularios WCM simples y el uso de una estructura anidada para permitir componentes de formulario adicionales.

Mediante el cuadro de diálogo [de](#configure-dialog) configuración, el editor de contenido puede definir la acción desencadenada por el envío del formulario, dónde se debe almacenar el contenido enviado y si se debe activar un flujo de trabajo. El autor de la plantilla puede utilizar el cuadro de diálogo [de](#design-dialog) diseño para definir los componentes permitidos y sus asignaciones de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de plantillas.

>[!NOTE]
>
>Los componentes principales Componente de Contenedor de formulario solo admiten el uso de componentes principales de los componentes de formulario (botón, texto, oculto, etc.). No se admite el uso de componentes [](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) de base de formularios dentro de los componentes principales del contenedor de formularios (y viceversa).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de Contenedor de formularios es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-container-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para obtener información sobre el componente Contenedor de formularios y ver ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la biblioteca [](https://adobe.com/go/aem_cmp_library_form_container)de componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de Contenedor de formularios [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué acciones se realizan cuando se envía el componente.

Según el tipo **de** acción seleccionado, cambiarán las opciones disponibles en el contenedor. Los tipos de acciones disponibles son:

* [Correo](#mail)
* [Almacenar contenido](#store-content)

Independientemente del tipo, hay una configuración [](#general-settings) general que se aplica a cada acción.

### Correo {#mail}

Cuando se envía el formulario, el tipo de acción de correo electrónico enviará un correo electrónico a los destinatarios designados.

![Opciones de correo en el cuadro de diálogo de edición del componente Contenedor de formulario](/help/assets/form-container-edit-mail.png)

* **Asunto** : el asunto del correo electrónico que se enviará al enviar el formulario
* **Desde** : la dirección de correo electrónico de origen del correo electrónico que se enviará al enviar el formulario
* **Hasta** : las direcciones de los destinatarios que recibirán un correo electrónico al enviar el formulario
   * Toque o haga clic en el botón **Añadir** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico
* **CC** - Las direcciones de los destinatarios que recibirán una copia del correo electrónico enviado al enviar el formulario
   * Toque o haga clic en el botón **Añadir** para agregar direcciones adicionales
   * Toque o haga clic en el botón **Eliminar** para eliminar una dirección de correo electrónico

### Almacenar contenido {#store-content}

Cuando se envía el formulario, el contenido del formulario se almacena en una ubicación de repositorio designada.

![Almacenar opciones de contenido en el cuadro de diálogo de edición del Contenedor de formularios](/help/assets/form-container-edit-store.png)

* **Ruta** de contenido: Ruta del repositorio de contenido donde se almacena el contenido enviado
* **Datos** de Vista: toque o haga clic en la vista de datos enviados almacenados como JSON
* **Flujo de trabajo** de Inicio: configure el inicio de un flujo de trabajo con el contenido almacenado como carga útil tras el envío del formulario

### Configuración general {#general-settings}

Independientemente del tipo de acción seleccionado, siempre se puede definir una página de agradecimiento.

![Opciones generales en el cuadro de diálogo de edición del componente Contenedor de formulario](/help/assets/form-container-edit-general.png)

* **Página** de agradecimiento: el usuario será redirigido a la página especificada una vez completado el envío del formulario.
   * Utilice el cuadro de diálogo Selección para seleccionar un recurso en AEM.
   * Si la página de agradecimiento no está en AEM, especifique la dirección URL absoluta. Las direcciones URL no absolutas se interpretarán en relación con AEM.
   * Deje en blanco para volver a mostrar el formulario después del envío.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir los componentes permitidos y sus asignaciones para el contenedor de forma similar al cuadro de diálogo de diseño para el contenedor de diseño [estándar en el editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de plantillas.

### Ficha Estilos {#styles-tab}

El componente Contenedor de formularios es compatible con el sistema [de](/help/get-started/authoring.md#component-styling)estilos AEM.
