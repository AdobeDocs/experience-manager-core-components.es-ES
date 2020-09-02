---
title: Ampliación de la capa de datos del cliente de Adobe
description: La capa de datos del cliente de Adobe se puede ampliar siguiendo algunos patrones básicos
translation-type: tm+mt
source-git-commit: 896ed679ed3351cb309a34b38bf97fe81adc2cfe
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Ampliación de la capa de datos del cliente de Adobe {#extending-acdl}

Puede ampliar los componentes principales con opciones de cuadro de diálogo personalizadas que permiten a los autores de contenido introducir información adicional relacionada con la capa de datos.

Para incluir estos campos en la capa de datos proporcionada por los componentes principales, debe ampliar el modelo del componente que implementa sus propios métodos de capa de datos específicos.

## Ejemplo: Componente de título {#example}

Un componente principal como el componente [](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) Título amplía [Componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) que tiene un `getData` método que, de forma predeterminada, devuelve [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa los campos predefinidos que el componente puede implementar, como `getDataLayerLinkUrl` y `getDataLayerTitle` para el [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Por lo tanto, el modelo Sling personalizado puede tener un `getData` método que devuelva un objeto que se extienda `ComponentData` a más campos.

Al hacer esto, se agregará un `data-cmp-data-layer` atributo al elemento HTML del componente con el JSON de los datos que se rellenarán en la capa de datos. En este punto, puede implementar secuencias de comandos que escuchen estos datos o eventos relacionados.
