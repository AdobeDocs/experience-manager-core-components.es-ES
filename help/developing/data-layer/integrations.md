---
title: Integraciones y la capa de datos del cliente de Adobe
description: Descubra cómo la capa de datos del cliente de Adobe se puede integrar con sus componentes personalizados y cómo las integraciones con Adobe Analytics y Adobe Target pueden ayudarle a obtener perspectivas en su sitio web
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 100%

---

# Integraciones con la capa de datos del cliente de Adobe {#integrations}

La capa de datos del cliente de Adobe reduce el esfuerzo por instrumentar sitios web al proporcionar un método estandarizado para exponer y acceder a cualquier tipo de datos para cualquier script.

La capa de datos del cliente de Adobe se puede integrar con sus componentes personalizados y las integraciones con Adobe Analytics y Adobe Target pueden ayudarle a obtener información sobre su sitio web.

## Activación de la capa de datos para componentes personalizados {#enabling-custom-components}

Para añadir automáticamente un componente personalizado a la capa de datos:

1. Defina las propiedades del modelo de componentes personalizado del que debe realizarse un seguimiento.
1. Añada el atributo `data-cmp-data-layer` al componente personalizado HTL. Por ejemplo, `data-cmp-data-layer="${mycomponent.data.json}"`.

Para convertir automáticamente el activador de la capa de datos en un evento `cmp:click` cada vez que se hace clic en un elemento específico del componente personalizado, agregue el atributo `data-cmp-clickable` al elemento al que se va a realizar el seguimiento en el componente personalizado HTL.

Se puede consultar el atributo `data-cmp-data-layer-enabled` en el lado del cliente para comprobar si la capa de datos está habilitada.

>[!TIP]
>
>Para obtener más información técnica sobre la integración de la capa de datos del cliente de Adobe con los componentes principales y cómo habilitar la capa de datos en los componentes personalizados, consulte el archivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) en el repositorio de componentes principales.

## Integración con Adobe Analytics y Adobe Target {#analytics-target}

Junto con Adobe Analytics y Adobe Target, la capa de datos del cliente de Adobe se convierte en la base de un conjunto de herramientas muy potente y flexible para obtener información sobre sus experiencias digitales. Los siguientes tutoriales le guían a través de integraciones de ejemplo.

### Recopilación de datos de página con Adobe Analytics {#collect-page-data}

Aprenda a utilizar las funciones integradas de la capa de datos del cliente de Adobe con los componentes principales de AEM para recopilar datos sobre una página en Adobe Experience Manager Sites. Experience Platform Launch y la extensión de Adobe Analytics se utilizarán para crear reglas para enviar datos de página a Adobe Analytics.

[Vea el tutorial aquí.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html?lang=es)

### Seguimiento de componentes en los que se hizo clic con Adobe Analytics {#track-clicked-components}

Utilice la capa de datos del cliente de Adobe impulsada por eventos con componentes principales de AEM para rastrear clics de componentes específicos en un sitio de Adobe Experience Manager. Obtenga información sobre cómo utilizar las reglas en Experience Platform Launch para detectar eventos de clic, filtrar por componente y enviar los datos a un Adobe Analytics con una señalización de seguimiento de vínculos.

[Vea el tutorial aquí.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html?lang=es)
