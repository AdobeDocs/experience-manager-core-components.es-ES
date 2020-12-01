---
title: Integraciones y la capa de datos del cliente de Adobe
description: Conozca cómo la capa de datos del cliente de Adobe puede integrarse con sus componentes personalizados y cómo las integraciones con Adobe Analytics y Adobe Target pueden ayudarle a obtener perspectivas en su sitio web
translation-type: tm+mt
source-git-commit: ea7a0e08ea1b769b400fce275c8ce7e0db6f9407
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Integraciones con la capa de datos del cliente de Adobe {#integrations}

La capa de datos del cliente de Adobe reduce el esfuerzo de instrumentar sitios web al proporcionar un método estandarizado para exponer y acceder a cualquier tipo de datos para cualquier secuencia de comandos.

La capa de datos del cliente de Adobe puede integrarse con sus componentes personalizados y las integraciones con Adobe Analytics y Adobe Target pueden ayudarle a obtener perspectivas en el sitio web.

## Habilitación de la capa de datos para los componentes personalizados {#enabling-custom-components}

Para agregar automáticamente un componente personalizado a la capa de datos:

1. Defina las propiedades del modelo de componentes personalizado que debe rastrearse.
1. Añada el atributo `data-cmp-data-layer` al HTL del componente personalizado. Por ejemplo: `data-cmp-data-layer="${mycomponent.data.json}"`.

Para hacer que el activador de capa de datos sea automáticamente un evento `cmp:click` cada vez que se hace clic en un elemento específico del componente personalizado, agregue el atributo `data-cmp-clickable` al elemento que se rastreará en el componente personalizado HTL.

Se puede consultar el atributo `data-cmp-data-layer-enabled` en el lado del cliente para comprobar si la capa de datos está habilitada.

>[!TIP]
>
>Para obtener más detalles técnicos sobre la integración de la capa de datos del cliente de Adobe con los componentes principales y cómo habilitar la capa de datos en los componentes personalizados, consulte el archivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) en el repositorio de componentes principales.

## Integración con Adobe Analytics y Adobe Target {#analytics-target}

Junto con Adobe Analytics y Adobe Target, la capa de datos del cliente de Adobe se convierte en la base de un conjunto de herramientas muy potente y flexible para obtener perspectivas sobre sus experiencias digitales. Los siguientes tutoriales le guían a través de integraciones de muestra.

### Recopilar datos de página con Adobe Analytics {#collect-page-data}

Aprenda a utilizar las funciones integradas de la capa de datos del cliente de Adobe con AEM componentes principales para recopilar datos sobre una página en Adobe Experience Manager Sites. Experience Platform Launch y la extensión Adobe Analytics se utilizarán para crear reglas que envíen datos de página a Adobe Analytics.

[Vista el tutorial aquí.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Seguimiento de componentes en los que se hizo clic con Adobe Analytics {#track-clicked-components}

Utilice la capa de datos del cliente de Adobe impulsada por evento con AEM componentes principales para rastrear los clics de componentes específicos en un sitio de Adobe Experience Manager. Obtenga información sobre cómo utilizar las reglas en Experience Platform Launch para detectar eventos de clics, filtrar por componente y enviar los datos a un Adobe Analytics con una señalización de seguimiento de vínculos.

[Vista el tutorial aquí.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
