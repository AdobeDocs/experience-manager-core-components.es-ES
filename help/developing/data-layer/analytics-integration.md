---
title: Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Analytics
description: Cómo configurar Adobe Analytics para registrar eventos de componentes principales
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 2%

---


# Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Analytics {#analytics-integration}

Este documento explica cómo configurar una configuración integral basada en AEM, la capa de datos del cliente de Adobe, Adobe Launch y Adobe Analytics para realizar el seguimiento:

* El ID de página almacenado en la capa de datos del cliente de Adobe cuando se carga una página
* Ruta de acceso de imagen almacenada en la capa de datos del cliente de Adobe cuando se hace clic en una imagen

Esto utiliza los componentes principales como ejemplo, pero puede utilizarse para sus propios componentes personalizados.

##  Paso 1: Creación de un grupo de informes en Adobe Analytics {#create-report-suite}

Para acumulado y análisis de los datos, primero debe crearse un grupo de informes.

1. Ir a `https://analytics.adobe.com`.
1. Inicie sesión con su Adobe ID.
1. Click the **Analytics** icon.
1. Vaya a **Administración -> Grupos** de informes.
1. Haga clic en **Crear nuevo -> Grupo** de informes.
1. Rellene el formulario:
   1. **ID de grupo de informes**: `yourSuiteID`
   1. **Título** del sitio: `Your suite description`
   1. **Huso horario**: Según proceda
   1. **Fecha** de lanzamiento: fecha actual o según proceda
   1. **Vistas estimadas de la página por día**: 100 o según proceda
1. Haga clic en **Crear grupo** de informes.

Si se realiza correctamente, recibirá el siguiente mensaje en verde: `Report Suite <yourReportSuite> has been successfully created.`

## Paso 2: Hacer visible el grupo de informes {#make-visible}

Para utilizar el nuevo grupo de informes, debe ser visible.

1. Ir a `https://adminconsole.adobe.com`.
1. Inicie sesión con su Adobe ID.
1. Haga clic en la tarjeta **Adobe Analytics - &lt;yourSite>**
1. Haga clic en el vínculo **Adobe Analytics - &lt;yourSite>**
1. Select the **Permissions** tab
1. Haga clic en el botón **Editar** de la fila Grupos **de** informes
1. Haga clic en el botón **+** del grupo de informes que creó en el [paso 1](#create-report-suite) para agregarlo a la categoría Elementos **de permisos** incluidos.
1. Haga clic en **Guardar**.

## Paso 3: Integración del sitio de AEM con Adobe Launch {#integrate-launch}

Launch debe estar integrado con el sitio de AEM para generar datos.

Siga los pasos que se describen en [Uso de la capa de datos del cliente de Adobe para integrar componentes principales y documento de Adobe Launch](launch-integration.md) .

## Paso 4: Instalación y configuración de Adobe Analytics Extension en Adobe Launch {#install-extension}

Adobe Analytics Extension permite la integración de Analytics con Launch.

1. En Adobe Launch, seleccione la propiedad recientemente agregada que ha creado en el [paso 3.](#integrate-launch)
1. Vaya a la ficha **Extensiones** y seleccione **Catálogo**.
1. Busque **Adobe Analytics**.
1. Haga clic en **Instalar**.
1. Configure la extensión.
   1. Introduzca la ID **del grupo de informes de** Analytics creada en el [paso 1](#create-report-suite) para los entornos correspondientes
   1. Definir conjunto **de caracteres** en UTF-8
1. Haga clic en Guardar

## Paso 5: Creación de un elemento de datos en Adobe Launch para el ID de página {#create-data-element}

Se requiere un elemento de datos en Launch para poder rastrear el ID de página.

1. En Adobe Launch, seleccione la propiedad creada en el [paso 3.](#integrate-launch)
1. Seleccione la ficha Elementos **** de datos y haga clic en **Añadir elemento** de datos:
   1. **Nombre**: `dl-page-id`
   1. **Extensión**: **Núcleo**
   1. **Tipo** de elemento de datos: **Código personalizado**
1. Haga clic en **Abrir editor**
1. En el editor, introduzca el código: `return adobeDataLayer.getState().page.id;`
1. Haga clic en **Guardar**.
1. Haga clic en **Guardar** para crear el elemento de datos.

## Paso 6: Creación de una regla en Adobe Launch para realizar el seguimiento del ID de página en Analytics {#track-page}

Las reglas permiten el seguimiento de atributos de navegación como el ID de página en Analytics.

Repita los pasos de la parte 5b de [Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Launch](launch-integration.md#launch-rule) documento para agregar la siguiente regla en Adobe Launch:

* **Nombre**: `track-dl-page-id`
* EVENTOS:
   * **Extensión**: **Núcleo**
   * **Tipo de evento**: **Final de página**
* ACCIÓN 1:
   * **Extensión**: **Adobe Analytics**
   * **Tipo** de acción: **Establecer variables**
   * **prop1**: `%dl-page-id%`
* ACCIÓN 2:
   * **Extensión**: **Adobe Analytics**
   * **Tipo** de acción: **Enviar señalización**
   * Comprobar **s.t(): Enviar datos a Adobe Analytics y tratarlos como una vista de página**

## Paso 7: Creación de una regla en Adobe Launch para registrar el Evento de clics en imágenes {#register-click}

Las reglas permiten el seguimiento de atributos de navegación como eventos de clic en Analytics.

Repita los pasos de la parte 5b de [Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Launch](launch-integration.md#launch-rule) documento para agregar la siguiente regla en Adobe Launch:

* **Nombre**: `register-dl-image-click`
* EVENTOS:
   * **Extensión**: **Núcleo**
   * **Tipo de evento**: **Final de página**
* ACCIÓN 1:
   * **Extensión**: **Núcleo**
   * **Tipo** de acción: **Código personalizado**
   * Editor: Introduzca el siguiente código

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Paso 8: Creación de una regla en Adobe Launch para realizar el seguimiento del Evento de clics de imágenes en Analytics {#track-click}

Las reglas permiten el seguimiento de atributos de navegación como eventos de clic en Analytics.

Repita los pasos de la parte 5b de [Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Launch](launch-integration.md#launch-rule) documento para agregar la siguiente regla en Adobe Launch:

* **Nombre**: `track-dl-image-click`
* EVENTOS:
   * **Extensión**: **Núcleo**
   * **Tipo de evento**: **Llamada directa**
   * **Identificador**: `dlImageClicked`
* ACCIÓN 1:
   * **Extensión**: **Adobe Analytics**
   * **Tipo** de acción: **Establecer variables**
   * **prop2**: Establecer como `%event.detail%`
* ACCIÓN 2:
   * **Extensión**: **Adobe Analytics**
   * **Tipo** de acción: **Enviar señalización**
   * Comprobar **s.t(): Enviar datos a Adobe Analytics y tratarlos como una vista de página**

## Paso 9: Publicación del código de inicio en el sitio web {#publish-launch}

Para habilitar el seguimiento de estas reglas y propiedades en Launch, se debe publicar el código.

1. En la ficha **Adobe Launch** , seleccione la ficha **Publishing** .
1. Haga clic en **Añadir nueva biblioteca**.
1. Cuando **Nombre** escriba: `data-layer-analytics-1`.
1. Como **Entorno** seleccione **Desarrollo (desarrollo)**.
1. Haga clic en **Añadir todos los recursos** modificados.
1. Para cada una de las tres reglas (`track-dl-page-id`, `register-dl-image-click` y `track-dl-image-click`):
1. Seleccione **Reglas -> Regla -> Última** y haga clic en **Seleccionar y crear una nueva revisión**.
1. Haga clic en **Guardar y crear para desarrollo**.

## Paso 10: Activación de la página para enviar información a Adobe Analytics {#trigger-page}

En este paso, instalará las extensiones Chrome **Launch y DTM Switch**. Con esta extensión solo necesita crear e implementar el código de Launch en el entorno de desarrollo. No es necesario implementar los entornos Ensayo y Producción.

1. Instale la extensión Chrome **Launch y DTM Switch** desde Discovery.
1. Haga clic en el icono **Iniciar conmutador** y establezca la depuración en *ON*.
1. Volver a cargar página `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Abra la consola del navegador y debería ver algo similar a lo siguiente.

![Salida de la consola de Analytics](/help/assets/analytics-console-output.png)

>[!TIP]
>
>También puede instalar la extensión **Experience Cloud Debugger** para Chrome para vista a Adobe Launch y a la información específica de Analytics sobre la página.

## Paso 11: Vista de la información rastreada en Adobe Analytics {#view-info}

Ahora puede realizar la vista de los eventos activados en Adobe Analytics.

1. Ir a `https://analytics.adobe.com`.
1. Inicie sesión con su Adobe ID.
1. Click the **Analytics** icon.
1. Select the **Reports** tab.
1. En el menú desplegable de la parte superior derecha, seleccione el grupo de informes que creó en el [paso 1.](#create-report-suite)
1. En la primera columna, seleccione Tráfico **personalizado -> Tráfico personalizado 1-10 -> Perspectiva personalizada 1** para vista de los ID de página (rutas) rastreados almacenados en la capa de datos. Debe aparecer de forma similar a la siguiente.

   ![Perspectiva personalizada 1](/help/assets/custom-insight-1.png)

1. Acceda a la **Perspectiva personalizada 2** para realizar la vista de las rutas de imagen rastreadas almacenadas en la capa de datos. Debe aparecer de forma similar a la siguiente.

   ![Perspectiva personalizada 2](/help/assets/custom-insight-2.png)
