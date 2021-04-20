---
title: Ampliación de la capa de datos del cliente de Adobe
description: La capa de datos del cliente de Adobe se puede ampliar siguiendo algunos patrones básicos
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# Ampliación de la capa de datos del cliente de Adobe {#extending-acdl}

Puede ampliar los componentes principales con opciones de cuadro de diálogo personalizadas que permiten a los autores de contenido introducir información adicional relacionada con la capa de datos.

Para incluir estos campos en la capa de datos proporcionada por los componentes principales, debe ampliar el modelo del componente que implementa sus propios métodos de capa de datos específicos.

## Ejemplo: Componente de título {#example}

Un componente principal como [Title component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) extiende [Component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) que tiene un método `getData` que de forma predeterminada devuelve [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa los campos predefinidos que el componente puede implementar, como  `getDataLayerLinkUrl` y  `getDataLayerTitle` para  [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Por lo tanto, el modelo Sling personalizado puede tener un método `getData` que devuelve un objeto que se extiende `ComponentData` para devolver más campos.

Al hacerlo, agregará un atributo `data-cmp-data-layer` al elemento HTML de su componente con el JSON de los datos que se rellenarán en la capa de datos. En este punto, puede implementar secuencias de comandos que escuchen estos datos o eventos relacionados.

>[!TIP]
>
>Para explorar más en profundidad la flexibilidad de la capa de datos, revise las opciones de integración, incluido cómo habilitar la capa de datos para los componentes personalizados.
