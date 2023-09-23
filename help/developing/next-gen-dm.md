---
title: Soporte de Dynamic Media de última generación
description: Obtenga información sobre cómo configurar los componentes principales Imagen y componentes de teaser para admitir recursos de Dynamic Media remotos de próxima generación.
role: Architect, Developer, Admin, User
source-git-commit: 9b8930c2e268f52a1377906725db9a05a089e233
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# Soporte de Dynamic Media de última generación {#next-gen-dm-support}

Obtenga información sobre cómo configurar los componentes principales Imagen y componentes de teaser para admitir recursos de Dynamic Media remotos de próxima generación.

## AEM Obtener la versión más reciente de la {#latest}

La compatibilidad con los recursos remotos de Dynamic Media de próxima generación requiere lo siguiente:

* AEM AEM.5 SP 18+ o as a Cloud Service de la
* Versión 2.23.2 o posterior de los componentes principales

## Configurar HTTPS {#https}

AEM Por lo general, se recomienda ejecutar todas las instancias de producción de la mediante HTTP. Sin embargo, es posible que los entornos de desarrollo local no estén configurados como tales. Sin embargo, los recursos remotos de Dynamic Media de próxima generación requieren HTTPS para funcionar.

[Utilice esta guía](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) para configurar HTTPS donde desee utilizar recursos remotos, incluidos entornos de desarrollo.

## Configurar OSGi {#osgi}

La ubicación de los recursos remotos debe definirse en una configuración OSGi. Configure las variables **Configuración de Dynamic Media de última generación** La configuración de OSGi se establece de la siguiente manera, reemplazando los valores por los del entorno de recursos remoto.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![Ventana de configuración OSGi de la configuración de Dynamic Media de próxima generación](/help/assets/remote-assets-osgi.png)

Para obtener más información sobre cómo configurar OSGi, consulte los siguientes documentos:

* [Configurar OSGi para Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) AEM para el as a Cloud Service
* [Configurar OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=es) AEM para 6,500

## Verificar configuración {#verify}

Ahora puede comprobar que la función de recursos remotos de Dynamic Media de próxima generación funciona. Para ello, puede instalar el sitio de muestra de WKND y los componentes principales.

* [Componentes principales](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) se requiere la versión 2.23.2 o posterior de.
* [Sitio de muestra de WKND](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) se requiere la versión 3.2.0 o posterior de.

Una vez instalados los componentes principales y el sitio WKND, puede probar la función en cualquier página de WKND.

1. AEM Acceda a la instancia de la mediante HTTPS.

1. Abra una página de demostración de WKND en el editor de páginas como `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Añada un componente de imagen a la página.

1. En el cuadro de diálogo Configurar del componente, desactive la opción **Heredar imagen destacada de la página** en el **Recurso** y haga clic en **Seleccionar**.

1. Si la configuración es correcta, aparecerá una lista desplegable con las opciones **Local** y **Remoto**. Seleccionar **Remoto**.

   ![Opciones de selección local y remota para la selección de imágenes](/help/assets/remote-asset-selection.png)

1. Se abrirá un cuadro de diálogo y deberá autenticarse en el servicio remoto.

1. Una vez autenticado, se abrirá un explorador de recursos del servicio remoto. Seleccione el recurso que desee y toque o haga clic en **Seleccionar**.

   ![Selección de un recurso remoto](/help/assets/remote-asset-picker.png)

AEM El recurso remoto se agregará a la página local de la red de distribución de recursos y ha verificado que la característica esté configurada correctamente.

## Uso de recursos remotos {#using}

Una vez configurados, se pueden seleccionar recursos remotos, donde seleccionaría recursos mediante los componentes principales, como en el [Componente de imagen](/help/components/image.md) y el [Componente Teaser.](/help/components/teaser.md)
