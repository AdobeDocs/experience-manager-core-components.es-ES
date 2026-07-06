---
title: 'Componente principal de formularios adaptables: contenedor de formulario'
description: Agregue un formulario adaptable a una página web.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# Contenedor del formulario {#form-container-adaptive-forms-core-component}

<span class="preview"> Este artículo describe las características de **Borradores** y **Compatibilidad con menús de Hamburger**, que son características previas al lanzamiento. Solo se puede acceder a la función de versión preliminar mediante nuestro [canal de versión preliminar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=es#new-features).</span>

Los formularios permiten a los visitantes interactuar con el sitio web proporcionando información valiosa, lo que puede aumentar la participación y la satisfacción del usuario. Un contenedor de formulario adaptable en Adobe Experience Manager (AEM) Sites permite a los propietarios de sitios web agregar fácilmente formularios a sus páginas. Esto ayuda a facilitar la comunicación entre los visitantes del sitio web y su propietario u organización, ya que proporciona una manera optimizada para que los visitantes proporcionen comentarios, hagan consultas y otras acciones

{{traditional-aem}}

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

El componente principal Acordeón de los formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales 2.0.4 para Cloud Service y componentes principales 1.1.12 para AEM 6.5.16.0 Forms o versiones posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| v1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). 
-->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de contenedor de formulario adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del contenedor de formularios para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de contenedor de formularios con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Servicios de rellenado previo**: esta opción permite al usuario seleccionar un servicio de rellenado previo para recuperar datos cuando se procesa el formulario adaptable. Más información acerca de [cómo crear y configurar un servicio de rellenado previo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=es#aem-forms-custom-prefill-service).

- **Función**: la función es un atributo de HTML que se utiliza para especificar la finalidad de un elemento de HTML para tecnologías de asistencia como los lectores de pantalla. El atributo de función se utiliza para proporcionar un contexto y un significado semántico adicionales a un elemento, lo que facilita a los lectores de pantalla la interpretación y el anuncio del contenido al usuario. Por ejemplo, en AEM Forms, la etiqueta de un campo de formulario puede tener la función “label” y su campo de entrada puede tener la función “textbox”. Esto ayuda al lector de pantalla a comprender la relación entre la etiqueta y el campo de entrada, y a anunciarlas correctamente al usuario.

- **Categoría de biblioteca de cliente**: el usuario puede configurar la biblioteca JavaScript personalizada por formulario adaptable. Se recomienda mantener solo las funciones reutilizables en la biblioteca, que tienen dependencia de las bibliotecas de terceros jquery y underscore.js.A veces, si hay **reglas de validación complejas**, el script de validación exacta reside en funciones personalizadas y los usuarios llaman a estas funciones personalizadas desde la expresión de validación de campo. Para que esta biblioteca de funciones personalizadas sea conocida y esté disponible mientras se realizan las validaciones del lado del servidor, el usuario del formulario puede configurar el nombre de la biblioteca de cliente de AEM en la pestaña **[!UICONTROL Básica]**.El usuario puede configurar la biblioteca customJavaScript para formularios adaptables. En la biblioteca, mantenga solo las funciones reutilizables, que dependen de las bibliotecas de terceros jquery y underscore.js.

- **Habilitar el menú de hamburguesa para la vista móvil**: seleccione la casilla de verificación para integrar un menú de hamburguesa en el formulario para la vista móvil. Representado por tres líneas horizontales apiladas verticalmente, este menú proporciona una visualización clara y despejada para paneles en dispositivos más pequeños, especialmente en dispositivos móviles. Para obtener más información sobre el menú de hamburguesa, consulte la sección [Más información sobre el menú de hamburguesa](#learn-more-about-the-hamburger-menu).


### Pestaña Modelo de datos {#data-model-tab}

![Ficha Modelo de datos](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Puede utilizar el modelo de datos de formulario para conectar un formulario a una fuente de datos para enviar y recibir datos en función de las acciones del usuario. También puede conectar un formulario a un esquema JSON para recibir los datos enviados en un formato predefinido. En función del requisito, conecte el formulario a un esquema JSON o a un modelo de datos de formulario:
- **Ninguno**: no asocie el formulario con un modelo de datos.
- **Esquema**: conecte el formulario a un esquema JSON cargado en su entorno.
- **Modelo de datos de formulario**: conecte el formulario a un modelo de datos de formulario para integrarlo con fuentes de datos externas.
- **Conector**: conecte el formulario a un origen de datos basado en conector.
- **Plantillas de formulario**: asocie el formulario con una plantilla de formulario.

### Pestaña Borradores {#drafts-tab}

![Ficha Borradores](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **Guardar borradores automáticamente**: seleccione la casilla de verificación **Guardar borradores automáticamente** para habilitar la acción de guardar formularios como borradores.
- **Guardar preferencia**: configure **Guardar preferencia** como **Guardar borradores a intervalos regulares** para guardar automáticamente el formulario después de un intervalo de tiempo específico.
  **Guardar frecuencia de intervalo (segundos)**: especifique el intervalo de tiempo (en segundos) para establecer la duración que desencadena la acción de guardar automáticamente el formulario en el intervalo definido.

### Pestaña Envío {#submission-tab}

Los usuarios pueden configurar distintas acciones para los envíos de formularios adaptables.

- **Al enviar** - Elija **Redirigir a la URL** para enviar a los usuarios de un formulario a una página configurada después del envío, o **Mostrar mensaje** para mostrar un mensaje de confirmación en el formulario.

- **Ruta/URL de redireccionamiento**: esta opción permite al usuario configurar una página para cada formulario, a la que se redirige a los usuarios después de enviar un formulario adaptable. Haga clic aquí para obtener más información sobre [configuración de páginas de redireccionamiento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=es).

![Pestaña Envío](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Mostrar mensaje**: esta opción permite a los usuarios agregar un mensaje que se muestra cuando el formulario adaptable se envía correctamente. El texto predefinido se incluye en el cuadro de diálogo y el usuario puede modificarlo. El cuadro de diálogo Mostrar mensaje admite herramientas de formato de texto enriquecido que permiten a los usuarios dar formato al texto agregado.

![Pestaña Mostrar mensaje](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Acción de envío**: se activa una acción de envío cuando un usuario hace clic en el botón Enviar en un formulario adaptable. Los usuarios pueden seleccionar acciones de envío en la lista desplegable que se admiten de forma predeterminada. Obtenga información sobre cómo [configurar una acción de envío en la pestaña Envío](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=es#supporting-custom-functions-in-validation-expressions-br).

- **Configuración de la acción**: configure asignaciones para pasar valores de campo como parámetros de solicitud de la página Gracias.

- **Habilitar solicitud POST**: seleccione esta opción para enviar los datos del formulario mediante una solicitud HTTP POST.

### Pestaña Documento de registro {#document-of-record-tab}

![Ficha Documento de registro](/help/adaptive-forms/assets/formcontainer_dortab.png)

Un [documento de registro (DoR)](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components) es una representación formal e imprimible de los datos enviados a través del formulario. Utilice la ficha **Documento de registro** para configurar cómo se genera un DoR cuando un usuario envía el formulario:

- **Ninguno** - No genere un documento de registro para el formulario.
- **Asociar plantilla de formulario como la plantilla de documento de registro** - Usar una plantilla de formulario existente como plantilla de documento de registro.
- **Generar documento de registro**: genere automáticamente un documento de registro basado en los datos del formulario enviado.
- **Excluir archivos adjuntos del documento de registro**: seleccione esta opción para omitir los archivos adjuntos del documento de registro generado.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente Contenedor del formulario.

### Pestaña Componentes permitidos {#allowed-components-tab}

![Pestaña de componentes permitidos del cuadro de diálogo Diseño](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

La pestaña **Componentes permitidos** permite que el editor de plantillas defina los componentes que se pueden añadir como elementos a los paneles en el componente del editor de formularios adaptables.

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

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.

- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden del nombre de la propiedad personalizada y el valor de la propiedad personalizada.

## Más información sobre el menú de hamburguesa {#learn-more-about-the-hamburger-menu}

Un menú de hamburguesa, a menudo denominado menú móvil o cajón de navegación, es un elemento de diseño popular en las interfaces de usuario móviles. Cuenta con tres líneas horizontales apiladas verticalmente, parecidas a una hamburguesa. El diseño ahorra espacio de pantalla de forma eficaz al ocultar las opciones de navegación secundarias hasta que son necesarias, especialmente en dispositivos más pequeños como dispositivos móviles. Los formularios AEM se pueden organizar de forma eficaz dentro del menú de hamburguesa, lo que permite a los usuarios acceder a varios paneles dentro de un formulario sin saturar la interfaz principal.

Imagine un escenario en el que una institución financiera ofrece un formulario de solicitud de préstamo en línea que requiere que los usuarios proporcionen información detallada en varios paneles, como detalles personales, información financiera, preferencias de préstamo y documentos de apoyo. El formulario incluye varios paneles y opciones que pueden saturar la interfaz, especialmente en dispositivos móviles. Los usuarios necesitan una forma organizada de navegar por estos paneles sin sentirse abrumados. El menú de hamburguesa se implementa para mejorar la experiencia del usuario en dispositivos móviles.

### Componentes del menú de hamburguesa

![Menú Hamburguesa](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Menú de hamburguesa**: El menú de hamburguesa incluye un panel de navegación que se desliza o se cae cuando se pulsa o se hace clic en el icono de hamburguesa. El menú muestra los encabezados del panel y, al seleccionar un panel, se desplaza el enfoque a ese panel. Permite a los usuarios navegar fácilmente entre diferentes paneles.

![Menú Hamburguesa](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Ruta de exploración**: Las rutas de exploración indican la ubicación actual del usuario dentro del formulario. Ofrecen un registro jerárquico que muestra la ruta de navegación del usuario y le ayuda a comprender su posición en el formulario.

**C. Panel activo**: el panel activo hace referencia a la sección o parte del formulario que se está mostrando en ese momento. Cuando un usuario selecciona una opción del menú de hamburguesa, el panel correspondiente se convierte en el panel activo, mostrando los campos y la información relevantes para esa sección.

### Puntos a tener en cuenta al trabajar con el menú de hamburguesas

- El menú de hamburguesa muestra únicamente los nombres de los paneles. Estos son diferentes escenarios que ilustran cómo aparece el nombre del panel en el panel de navegación del menú de hamburguesa en función de las propiedades de configuración del panel:

   - Si establece las propiedades del panel en hidden, el nombre del panel no aparece en el panel de navegación del menú de hamburguesa. Por ejemplo, si configura las propiedades del panel `Financial Information` como `hidden`, el nombre del panel no aparecerá en el panel de navegación del menú de hamburguesa.

     ![Panel oculto](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - Si establece las propiedades del panel en `disabled`, su nombre aparecerá en el panel de navegación del menú de hamburguesa, pero no podrá seleccionarlo ni editarlo. Por ejemplo, si configura las propiedades del panel `Financial Information` como `disabled`, el nombre del panel aparecerá en el panel de navegación, pero no se podrá seleccionar ni editar.

     ![Panel deshabilitado](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - Si oculta el título del panel, no aparecerá en el panel de navegación del menú de hamburguesa. En su lugar, aparece un espacio en blanco, pero puede navegar a los campos del panel haciendo clic en ese espacio. Por ejemplo, si oculta el título del panel `Financial Information`, el espacio en blanco aparecerá en su lugar en el panel de navegación del menú de hamburguesa. Puede navegar a los campos del panel haciendo clic en el espacio en blanco.

     ![Panel de título oculto](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- De forma predeterminada, el panel de navegación del componente Ruta de exploración admite hasta tres niveles de navegación. Sin embargo, con el componente personalizado, puede configurar la jerarquía de navegación para que quepa tantos niveles como sea necesario.
- Al utilizar el menú de hamburguesa, el usuario puede navegar entre paneles mediante flechas. Sin embargo, una vez seleccionado un panel, el menú se cierra automáticamente y el enfoque cambia a los campos dentro del panel elegido.

<!--
### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}