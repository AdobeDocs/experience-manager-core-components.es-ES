---
title: Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Launch
description: Cómo configurar Adobe Launch para registrar eventos de componentes principales mediante Adobe Launch
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Uso de la capa de datos del cliente de Adobe para integrar componentes principales y Adobe Launch {#launch-integration}

Los componentes principales se pueden integrar con Adobe Launch mediante la capa de datos del cliente de Adobe. En este documento se describe cómo configurar Adobe Launch para rastrear los eventos de clics de los componentes de imagen como ejemplo.

Cuando se configura, Launch generará el siguiente resultado en la consola del explorador cuando se haga clic en un componente de imagen principal.

![Ejemplo de salida de consola](/help/assets/launch-console-output.png)

## Iniciar integración con AEM {#launch-aem}

El primer Adobe Launch debe estar integrado con el sitio de AEM.

### Paso 1: Creación de una integración en Adobe I/O {#create-io-integration}

Inicie sesión en Adobe I/O para inicio y configurar una integración.

1. Ir a `https://console.adobe.io`.
1. Inicie sesión con su Adobe ID.
1. En la sección Inicio rápido, haga clic en **Crear integración**.
1. Select **Access an API** and click **Continue**.
1. Seleccione **Experience Platform Launch API** debajo de Adobe Experience Platform y haga clic en **Continuar**.

### Paso 2: Creación de una configuración de IMS en AEM {#ims-configuration}

En AEM, debe definir la integración que comenzó a configurar en Adobe I/O.

1. Vaya a la página de inicio de AEM, haga clic en **Herramientas -> Seguridad -> Configuraciones** de Adobe IMS.
1. Haga clic en **Crear**.
1. Como Solución **** de Cloud, seleccione **Adobe Launch**.
1. Marque **Crear nuevo certificado**.
1. Introduzca un alias para el certificado, como **aem-launch-certificate**.
1. Haga clic en **Crear certificado** y, en la ventana emergente, haga clic en **Aceptar** para crear el certificado.
1. Haga clic en **Descargar clave** pública y, en la ventana emergente, haga clic en **Descargar**.

### Paso 3: Finalizar la configuración de Adobe I/O {#finish-io}

Con el certificado y la clave creados en la configuración de AEM IMS, puede finalizar la configuración de Adobe I/O.

1. Vuelva a la consola de Adobe I/O como en el [paso 1.](#create-io-integration)
1. En la ventana **Crear una nueva integración** , introduzca un nombre y una descripción como capa **de datos de** AEM Launch.
1. En Certificados **de claves** públicas, cargue el certificado que ha creado en el [paso 2.](#ims-configuration)
1. Seleccione el perfil **Iniciar - Prod**.
1. Click **Create integration**.
1. Haga clic en **Continuar para ver los detalles** de la integración. Necesitará estos detalles más adelante para finalizar la configuración de IMS en su instancia de AEM.

### Paso 4: Finalizar la configuración de IMS {#finish-ims}

Con los detalles de la integración de Adobe I/O, puede finalizar la configuración de AEM IMS.

1. En la ficha AEM, en la ficha Configuración **de cuenta técnica de** Adobe IMS del [paso 2,](#ims-configuration) haga clic en **Siguiente**.
1. Introduzca un título como, por ejemplo, la configuración de **IMS para Adobe Launch**.
1. En la ficha Adobe I/O, copie la clave de **API (ID de cliente)**.
1. En la ficha AEM, pegue la clave copiada anterior en el campo **Clave de** API.
1. En Adobe I/O, haga clic en **Recuperar secreto** de cliente y cópielo.
1. En la ficha AEM, péguela en el campo Secreto del **cliente** .
1. En la ficha Adobe I/O, seleccione la ficha **JWT** y copie la URL como `https://ims-na1.adobelogin.com`.
1. En la ficha AEM, pegue la dirección URL en el campo **Servidor** de autorización.
1. En la ficha Adobe I/O, copie la carga útil JWT (el código entre llaves).
1. En la ficha AEM, péguela en el campo **Carga útil** .
1. Haga clic en **Crear** para crear la configuración de IMS en AEM.

### Paso 5a: Creación de una propiedad en Adobe Launch {#create-property}

Una propiedad define las funciones que Launch puede insertar en el sitio.

1. Vaya a Adobe Launch en `https://launch.adobe.com`.
1. Inicie sesión con su Adobe ID.
1. Haga clic en **Nueva propiedad**.
1. Escriba un nombre como **Iniciar capa** de datos de AEM.
1. Escriba su dominio.
1. Haga clic en **Guardar**.

### Paso 5b: Creación de una regla en el lanzamiento {#launch-rule}

Con la propiedad que ha creado, puede definir una regla que especifique lo que debe suceder cuando se produce una acción.

1. Haga clic en la propiedad recientemente agregada del [paso 5](#create-property) **Iniciar capa** de datos de AEM.
1. Seleccione la ficha **Reglas** y haga clic en **Crear nueva regla**.
1. Escriba un nombre como, por ejemplo, clic **en una** imagen.
1. Haga clic en el botón **+** debajo de **Eventos**.
1. Seleccione **Core** as **Extension**, **Haga clic** como **Tipo de evento** e introduzca **.cmp-image** **** como selector CSS.
1. Haga clic en **Mantener cambios**.
1. Haga clic en el botón **+** debajo de **Acciones**.
1. Seleccione **Core** as **Extension**, **Custom Code** as **Action Type** y haga clic en **Abrir editor**.
1. En el editor, introduzca el código siguiente: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Haga clic en **Guardar**.
1. Haga clic en **Mantener cambios**.
1. Haga clic en **Guardar** para crear la nueva regla.

### Paso 6: Publicación de la regla de inicio {#publish-rule}

Para que la nueva regla esté disponible para el sitio de AEM, debe publicarla.

1. En la ficha **Adobe Launch** , seleccione la ficha **Publishing** .
1. Haga clic en **Añadir nueva biblioteca**.
1. Introduzca un **Nombre** como corresponda, como **demo-1**.
1. Para **Entornos** , seleccione según corresponda, como **Desarrollo (desarrollo)**.
1. Haga clic en **Añadir un recurso**.
1. Seleccione **Reglas -> clic en la imagen -> Última** y haga clic en **Seleccionar y crear una nueva revisión**.
1. Haga clic en **Guardar y crear para desarrollo**.
1. En la ventana emergente, haga clic en **Aplicar actualizaciones y continuar**.
1. Cuando se cree la biblioteca, haga clic en el icono de puntos suspensivos y seleccione **Enviar para aprobación**.
1. En la ventana emergente, haga clic en **Enviar**.
1. Haga clic en el icono de puntos suspensivos y seleccione **Generar para ensayo**.
1. Cuando la compilación haya terminado, haga clic en el icono de puntos suspensivos y seleccione **Aprobar para publicación**.
1. En la ventana emergente, haga clic en **Aprobar**.
1. Haga clic en el icono de puntos suspensivos y seleccione **Generar y publicar en producción**.
1. En la ventana emergente, haga clic en **Publicar**.

### Paso 7: Habilitar las configuraciones de nube para el sitio {#enable-configurations}

Para utilizar la integración, debe asignarse en AEM como configuración de nube.

1. En la consola de AEM, haga clic en **Herramientas -> General -> Navegador** de configuración.
1. Consulte los ejemplos **de componentes** principales y haga clic en **Propiedades**.
1. Compruebe las configuraciones de **Cloud** y haga clic en **Guardar y cerrar**.

### Paso 8: Creación de una integración de inicio con su sitio en AEM {#create-launch-integration}

Se necesita una integración de Launch para que AEM funcione con Launch

1. En la consola de AEM, haga clic en **Herramientas -> Cloud Services -> Adobe Launch Configurations**.
1. Seleccione Ejemplos **de componentes** principales y haga clic en **Crear**.
1. Introduzca un **Título** , como la configuración **** Iniciar.
1. Seleccione la configuración de IMS que creó en el [paso 4.](#finish-ims)
1. Como **Compañía** , selecciónela según corresponda.
1. Como **propiedad** , seleccione la propiedad Launch recientemente agregada, creada en el [paso 5.](#create-property)
1. Mueva el control deslizante **Incluir código de producción en Autor** a la derecha y haga clic en **Siguiente**.
1. Haga clic en **Siguiente**. 
1. Haga clic en **Siguiente**. 
1. Haga clic en **Crear**.

### Paso 9: Conexión del sitio de AEM al lanzamiento de la integración {#connect-aem}

Para que AEM utilice la integración de Launch, debe asignarse como configuración de nube.

1. En la consola de AEM, haga clic en **Sitios** y compruebe el sitio **de** componentes principales.
1. Haga clic en **Propiedades**.
1. Select the **Advanced** tab.
1. Como Configuración **de** nube, seleccione los ejemplos **de componentes** principales y haga clic en **Seleccionar**.
1. Click **Save &amp; Close**.

### Paso 10: Verifique que la lógica de inicio se aplique a la página {#verify-launch}

Pruebe que los pasos hasta ahora han tenido éxito.

1. Abra la página Imagen de la biblioteca de componentes principales en modo de previsualización: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Haga clic en una imagen y compruebe que el mensaje `A Core Image was clicked` se muestra en la consola del explorador.

## Iniciar la integración con AEM y la capa de datos {#data-layer-launch}

Ahora que la integración entre AEM y Launch está configurada, podemos integrarla con la capa de datos.

### Paso 1: Creación de una regla en Adobe Launch {#create-rule}

Repita los pasos del [paso 5](#launch-rule) para agregar una nueva regla en Adobe Launch con los siguientes valores.

* Nombre: `image-click-data-layer`
* EVENTOS:
   * Extensión: Núcleo
   * Tipo de evento: DOM Ready
* ACCIONES:
   * Extensión: Núcleo
   * Tipo de acción: Código personalizado
   * Código:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Paso 2: Publicación de la regla de inicio para que esté disponible en el sitio de AEM {#publish-rule-2}

Repita los pasos del [paso 6](#publish-rule) para publicar la nueva regla.

### Paso 3: Verifique que la lógica de inicio se aplique a la página {#verify}

1. Abra la página Imagen de la biblioteca de componentes principales en modo de previsualización: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Haga clic en una imagen y compruebe que se muestra el siguiente mensaje en la consola del explorador:

   ![Salida de la consola de capa de datos](/help/assets/data-layer-console-output.png)
