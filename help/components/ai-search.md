---
title: Componente Búsqueda por IA de contenido
description: El componente Búsqueda por IA de contenido proporciona a los visitantes del sitio una búsqueda generativa basada en IA.
role: Developer, Admin, User
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# Componente Búsqueda por IA de contenido {#content-ai-search-component}

El componente Búsqueda por IA de contenido proporciona a los visitantes del sitio una búsqueda generativa basada en IA.

{{traditional-aem}}

## Uso {#usage}

El componente Búsqueda por IA de contenido permite a los visitantes buscar en un [Source de contenido](https://experienceleague.adobe.com/es/docs/experience-manager-content-ai/using/contentsources) directamente desde una página y, opcionalmente, ver un resumen de los resultados generado por IA. Combina un cuadro de búsqueda semántica/de texto completo estándar con un panel **Mostrar resumen generado por IA** con tecnología de IA de contenido de AEM que se puede alternar.

El [cuadro de diálogo de edición](#edit-dialog) permite que el autor del contenido defina el ámbito de contenido de la búsqueda, el comportamiento de búsqueda y la configuración generativa. No hay ningún cuadro de diálogo de diseño, ya que no hay configuraciones disponibles en el nivel de plantilla.

>[!NOTE]
>
>Para utilizar el componente Búsqueda por IA de contenido, debe tener acceso a una Source de inteligencia artificial aplicada al contenido y el administrador debe haber habilitado el componente para su proyecto. Consulte el documento [Configuración del componente Búsqueda por IA de contenido](/help/developing/ai-search.md) para obtener más información.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Búsqueda por IA de contenido es la versión 1, que se introdujo con la versión 2.32.0 de los componentes principales en julio de 2026 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | - | - | - | En curso |

Para obtener más información acerca de las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de componentes principales.](/help/versions.md)

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Búsqueda por IA de contenido y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_ai_search).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Búsqueda por IA de contenido [&#x200B; se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el ámbito de contenido de la búsqueda, el comportamiento de búsqueda y la configuración generativa. No hay ningún cuadro de diálogo de diseño, ya que no hay configuraciones disponibles en el nivel de plantilla.

### Pestaña Ámbito de contenido {#content-scope}

![Pestaña Ámbito de contenido del cuadro de diálogo de edición](/help/assets/content-ai-search-edit-content-scope.png)

* **ID**: esta opción permite controlar el identificador único del componente en HTML y en la [capa de datos.](/help/developing/data-layer/overview.md)
  * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
  * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
  * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.
* **Tipo de Source de contenido**: este campo define el tipo de origen de contenido. Al seleccionar un tipo, se rellena la lista desplegable **Source de contenido** con orígenes coincidentes.
  * **ADQUISICIÓN**: valor predeterminado utilizado para orígenes públicos de acceso anónimo indizados mediante una canalización de rastrea/adquisición
  * **AEM_AUTHOR**: un origen del lado de la inteligencia artificial aplicada al contenido cuyo contenido se ingirió desde una instancia de autor de AEM
  * **AEM_PUBLISH**: un origen del lado de IA de contenido cuyo contenido se ingirió desde una instancia de publicación de AEM
  * **PERSONALIZADO**: un origen registrado fuera de las canalizaciones de ingesta propias de AEM
* **Fuentes de contenido**: define el Source de contenido que busca este componente.
  * Las entradas disponibles coinciden con orígenes de contenido que ya existen y están **disponibles**, y también con el tipo establecido en **Tipo de Source de contenido**
  * Consulte el documento [Configurar y administrar las fuentes de inteligencia artificial aplicada al contenido](https://experienceleague.adobe.com/es/docs/experience-manager-content-ai/using/contentsources) para obtener más información.

### Pestaña Comportamiento de búsqueda {#search-behavior}

![Pestaña Comportamiento de búsqueda del cuadro de diálogo de edición](/help/assets/content-ai-search-edit-search-behavior.png)

* **Diseño de resultados**: esta opción define cómo se muestran los resultados de búsqueda al visitante.
  * **Tarjetas**: esta opción muestra los resultados en formato de cuadrícula.
  * **Lista**: esta opción muestra los resultados en formato de lista.
* **Tamaño de resultados**: define el número de resultados recuperados por solicitud de búsqueda.
  * El valor predeterminado es `12`.
  * Los visitantes pueden cargar más resultados cuando hay coincidencias adicionales disponibles.
* **Texto de marcador de posición**: este es el texto que se muestra en el campo de entrada de búsqueda vacío antes de que el visitante entre en una consulta de búsqueda.

### Pestaña Búsqueda generativa {#generative-search}

![Pestaña Búsqueda generativa del cuadro de diálogo de edición](/help/assets/content-ai-search-edit-generative-search.png)

* **Mostrar alternancia de resumen generativo a los visitantes**: cuando no está marcada, los visitantes no pueden cambiar si se muestra el resumen de IA.
  * El valor predeterminado está habilitado.
* **Mostrar resumen generativo de forma predeterminada**: esta opción controla el estado predeterminado de la opción de cara al visitante para el resumen generado por IA.
  * El valor predeterminado está habilitado.
* **Reserva de error GenSearch**: define cómo debería comportarse la búsqueda o el error.
  * **Solo resultados (ocultar error)**: si hay un error, se muestran solo los resultados devueltos, no el error ni ningún botón de reintento. Este es el valor predeterminado.
  * **Mostrar error con reintento** - Si hay un error, mostrar el error con un botón de reintento.
  * **Mostrar solo mensaje de error**: si hay un error, mostrar solo el mensaje de error, sin resultados.
