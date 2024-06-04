---
title: 'Componente principal de formularios adaptables: contenedor de formulario'
description: Agregue un formulario adaptable a una página web.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 97%

---

# Contenedor de formulario {#form-container-adaptive-forms-core-component}

Los formularios permiten a los visitantes interactuar con el sitio web proporcionando información valiosa, lo que puede aumentar la participación y la satisfacción del usuario. Un contenedor de formulario adaptable en Adobe Experience Manager (AEM) Sites permite a los propietarios de sitios web agregar fácilmente formularios a sus páginas. Esto ayuda a facilitar la comunicación entre los visitantes del sitio web y su propietario u organización, ya que proporciona una manera optimizada para que los visitantes proporcionen comentarios, hagan consultas y otras acciones.

## Uso {#reasons-to-use-forms-container}

Existen varias razones por las que se puede agregar un formulario a un sitio web:
- **Recopilación de datos**: los formularios pueden utilizarse para recopilar datos de los visitantes de un sitio web con diversos fines, como estudios de mercado, análisis de comportamiento, etc.

- **Generación de posibles clientes**: se puede utilizar un formulario para recopilar información de clientes potenciales, como el nombre y la dirección de correo electrónico, para generar posibles clientes para marketing y ventas.

- **Comercio electrónico**: los formularios pueden servir para comprar en línea, lo que permite a los clientes efectuar pedidos y pagos a través del sitio web.

- **Contacto**: un formulario de contacto permite a los visitantes del sitio web comunicarse fácilmente con el propietario o la organización del sitio web.

- **Encuestas y sondeos**: los formularios pueden usarse para recopilar comentarios y opiniones de visitantes de sitios web a través de encuestas y sondeos.

- **Registro de eventos**: los formularios se pueden destinar al registro en eventos, para que los visitantes del sitio web puedan inscribirse en eventos o seminarios web.

- **Suscripciones**: los formularios pueden emplearse para suscripciones a sitios web, lo que permite a los visitantes suscribirse a una newsletter u otras comunicaciones periódicas.

- **Autenticación de usuarios**: los formularios pueden funcionar para la autenticación de usuarios, lo que permite a los visitantes del sitio web crear cuentas e iniciar sesión para acceder a contenidos o funciones exclusivas.

- **Aumentar tasa de conversión**: un formulario bien diseñado puede aumentar la tasa de conversión al facilitar a los usuarios la realización de las acciones deseadas, como la compra de un producto o la suscripción a un servicio.

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

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Servicios de rellenado previo**: esta opción permite al usuario seleccionar un servicio de rellenado previo para recuperar datos cuando se procesa el formulario adaptable. Más información acerca de [cómo crear y configurar un servicio de rellenado previo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=es#aem-forms-custom-prefill-service).

- **Categoría de biblioteca de cliente**: el usuario puede configurar la biblioteca JavaScript personalizada por formulario adaptable. Se recomienda mantener solo las funciones reutilizables en la biblioteca, que tienen dependencia de las bibliotecas de terceros jquery y underscore.js.
A veces, si hay **reglas de validación complejas**, el script de validación exacta reside en funciones personalizadas y los usuarios llaman a estas funciones personalizadas desde la expresión de validación de campo. Para que esta biblioteca de funciones personalizadas sea conocida y esté disponible mientras se realizan las validaciones del lado del servidor, el usuario del formulario puede configurar el nombre de la biblioteca de cliente de AEM en la pestaña **[!UICONTROL Básico]** de las propiedades del contenedor del formulario adaptable como se muestra a continuación.

El usuario puede configurar la biblioteca customJavaScript para formularios adaptables. En la biblioteca, mantenga solo las funciones reutilizables, que dependen de las bibliotecas de terceros jquery y underscore.js.

### Pestaña Modelo de datos {#data-model-tab}

![Pestaña Envío](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Puede utilizar el modelo de datos del formulario para conectar un formulario a una fuente de datos para enviar y recibir datos en función de las acciones del usuario. También puede conectar un formulario a un esquema JSON para recibir los datos enviados en un formato predefinido. En función del requisito, conecte el formulario a un esquema JSON o a un modelo de datos de formulario:
- Crear un esquema JSON y cargarlo en su entorno
- Crear modelo de datos de formulario

### Pestaña Envío {#submission-tab}

Los usuarios pueden configurar distintas acciones para los envíos de formularios adaptables.

- **Ruta/URL de redireccionamiento**: esta opción permite al usuario configurar una página para cada formulario, a la que se redirige a los usuarios después de enviar un formulario adaptable. Haga clic aquí para obtener más información sobre [configuración de páginas de redireccionamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=es).

![Pestaña Envío](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostrar mensaje**: esta opción permite a los usuarios agregar un mensaje que se muestra cuando el formulario adaptable se envía correctamente. El texto predefinido se incluye en el cuadro de diálogo y el usuario puede modificarlo. El cuadro de diálogo Mostrar mensaje admite herramientas de formato de texto enriquecido que permiten a los usuarios dar formato al texto agregado.

![Pestaña Mostrar mensaje](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Acción de envío**: se activa una acción de envío cuando un usuario hace clic en el botón Enviar en un formulario adaptable. Los usuarios pueden seleccionar acciones de envío en la lista desplegable que se admiten de forma predeterminada. Obtenga información sobre cómo [configurar una acción de envío en la pestaña Envío](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=es#supporting-custom-functions-in-validation-expressions-br).

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Contenedor del formulario.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña de componentes permitidos del cuadro de diálogo Diseño](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

El **Componentes permitidos** permite al editor de plantillas establecer los componentes que se pueden añadir como elementos a los paneles del componente en el editor de Forms adaptable.

### Pestaña Componentes predeterminados {#default-components-tab}

![Pestaña de componente predeterminada del cuadro de diálogo Diseño](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

La pestaña **Componentes predeterminados** facilita al editor de plantillas especificar los componentes visibles de forma predeterminada como elementos en el componente contenedor de formulario del editor de Formularios adaptables.

### Pestaña Configuración adaptable {#responsive-tab}

![Pestaña Configuración adaptable del cuadro de diálogo Diseño](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

La pestaña **Configuración adaptable** permite al editor de plantillas especificar el número de columnas de la cuadrícula dentro del componente contenedor de formulario en el editor de Formularios adaptables.

### Pestaña Estilos {#styles-tab}

El componente principal de los archivos adjuntos de formularios adaptables es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal de contenedor de formularios para formularios adaptables.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Pestaña Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}