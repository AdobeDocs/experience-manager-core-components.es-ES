---
title: Ampliación de la capa de datos del cliente de Adobe
description: La capa de datos del cliente de Adobe se puede ampliar siguiendo algunos patrones básicos
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
TQID: 'https://experienceleague.adobe.com/67YSpRfwNRMDgcBARHKLz51-Er6xb4vp1rXX0r0sbfE'
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: d9d38edd-df1b-480c-8f5e-72b62576f390
    internal-label: Site and page features
  - id: d429a63e-ade4-4117-b04e-9b996d1c94ef
    internal-label: Integrations
subfeature_v2:
  - id: c43ff1f6-5a6d-4e8c-b3cc-6bdb3fa6e092
    internal-label: Core components
  - id: a94e5c13-4138-47ec-b9c8-e804e17aaca2
    internal-label: Adobe Client Data Layer
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 025b8134f7675b4515f4586910a94a2732bfa2ee
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%
---
# Ampliación de la capa de datos del cliente de Adobe {#extending-acdl}

Puede ampliar los componentes principales con opciones de cuadro de diálogo personalizadas que permiten a los autores de contenido introducir información adicional relacionada con la capa de datos.

Para incluir estos campos en la capa de datos proporcionada por los componentes principales, debe ampliar el modelo del componente que implementa sus propios métodos de capa de datos específicos.

## Ejemplo: Componente Título {#example}

Un componente principal como [componente Título](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) extiende [Componente](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java), que tiene un método `getData` que de forma predeterminada devuelve [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serializa los campos predefinidos que el componente puede implementar, como `getDataLayerLinkUrl` y `getDataLayerTitle` para [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Por lo tanto, el modelo Sling personalizado puede tener un método `getData` que devuelve un objeto que se extiende `ComponentData` para devolver más campos.

Al hacerlo, agregará un atributo `data-cmp-data-layer` al elemento HTML de su componente con el JSON de los datos que se rellenarán en la capa de datos. En este punto, puede implementar scripts que escuchen estos datos o eventos relacionados.

>[!TIP]
>
>Para explorar más en profundidad la flexibilidad de la capa de datos, revise las opciones de integración, incluido cómo habilitar la capa de datos para los componentes personalizados.
