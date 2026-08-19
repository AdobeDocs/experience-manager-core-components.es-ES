---
title: Configuración del componente Búsqueda por IA de contenido
description: El componente Búsqueda por IA de contenido proporciona a los visitantes del sitio una búsqueda generativa basada en IA. Obtenga información sobre cómo habilitar este componente para los autores de contenido.
role: Developer, Admin
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# Configuración del componente Búsqueda por IA de contenido {#configure-content-ai-search-component}

El componente Búsqueda por IA de contenido proporciona a los visitantes del sitio una búsqueda generativa basada en IA. Obtenga información sobre cómo habilitar este componente para los autores de contenido.

## Requisitos previos {#prerequisites}

* Al menos un [Source de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) ya se ha creado y con el estado **Disponible**.
* La configuración OSGi **Cliente de inteligencia artificial aplicada al contenido de AEM** (`ContentAIClientImpl`) se configuró en Autor y Publicación, con una credencial de API válida y un valor **Source de contenido predeterminado**. Consulte el documento [Configurar un proyecto de Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) para obtener las credenciales.

## Crear un componente proxy {#proxy-component}

Al igual que todos los componentes principales, se recomienda crear un componente proxy para el componente de Búsqueda por IA de contenido predeterminado que se envía con AEM. Al mantener los cambios específicos del proyecto en el componente proxy en `/apps`, Adobe actualiza automáticamente los componentes base en `/libs` y el componente del proyecto hereda automáticamente estas actualizaciones. Consulte los documentos [Uso de componentes principales](/help/get-started/using.md#aemaacs) y [Directrices de componentes](/help/developing/guidelines.md) para obtener más información.

## Configurar bibliotecas de cliente {#clientlib}

El componente Búsqueda por IA de contenido no sigue [el patrón estándar para incluir bibliotecas de cliente en los componentes principales.](/help/developing/including-clientlibs.md) En su lugar, siga estos pasos.

Agregue lo siguiente al componente de página del proyecto `customheaderlibs.html` (para CSS) y `customfooterlibs.html` (para JS):

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

Si el proyecto coloca su propio estilo de marca encima, agregue una segunda categoría para la biblioteca de cliente del proyecto después de esta.

## Uso del componente Búsqueda por IA de contenido {#using}

Los autores de contenido ahora pueden colocar el componente Búsqueda por IA de contenido en sus páginas. Consulte el documento [Componente de Búsqueda por IA de contenido](/help/components/ai-search.md) para obtener más información.

## Cómo utiliza el componente la IA de contenido {#how-it-works}

* Las consultas de búsqueda estándar se proporcionan mediante la misma capa de recuperación que el índice de Content Source, y devuelven páginas, fragmentos o recursos coincidentes del origen configurado.
* Cuando se habilita el resumen generado por IA, el componente también llama al punto de conexión generativo de la inteligencia artificial aplicada al contenido de AEM, basa la respuesta en el mismo contenido indexado y muestra las fuentes junto al resumen para que los visitantes puedan verificarlo.
* Dado que ambas funciones se leen desde el mismo Content Source controlado, los resultados y resúmenes son coherentes con el contenido indexado actualmente. Volver a ejecutar la adquisición (consulte [Control de los orígenes de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)) actualiza ambos.

## Siguientes pasos {#next-steps}

* [Controle sus fuentes de contenido](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources): cree y administre el Source de contenido que busca este componente.
* [Configurar un proyecto de Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project): obtenga las credenciales que usa la configuración del cliente de inteligencia artificial aplicada al contenido de OSGi.
* [Referencia de la API de inteligencia artificial aplicada al contenido](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/): comprenda los extremos de búsqueda y resumen generativo subyacentes a los que llama este componente.
