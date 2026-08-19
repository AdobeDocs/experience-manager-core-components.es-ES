---
title: Componente Búsqueda rápida
description: El componente Búsqueda rápida proporciona funciones de búsqueda en un sitio web y presenta resultados de búsqueda para que los visitantes puedan buscar en el sitio y filtrar los resultados, opcionalmente mediante la búsqueda semántica con tecnología de IA a través de la opción Búsqueda semántica.
role: Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
TQID: https://experienceleague.adobe.com/wU-3pacdEz9ne8b53-mKJy-XxRdyz2gu4Jvj-yFgGOw
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
source-git-commit: f939ce7498d9ec1901bea4b5fbf631365ba923fa
workflow-type: tm+mt
source-wordcount: 909
ht-degree: 41%

---


# Componente Búsqueda rápida {#quick-search-component}

El componente Búsqueda rápida proporciona funciones de búsqueda en un sitio web y presenta resultados de búsqueda para que los visitantes puedan encontrar fácilmente contenido coincidente y ver resultados.

{{traditional-aem}}

## Uso {#usage}

El componente Búsqueda rápida permite a los visitantes del sitio buscar contenido, ver los resultados in situ y navegar fácilmente a las páginas coincidentes. Los nuevos resultados se obtienen de forma dinámica a medida que el usuario se desplaza por los resultados de la búsqueda.

El [cuadro de diálogo de edición](#edit-dialog) permite que el autor del contenido defina dónde debería comenzar la búsqueda en el árbol de contenido y, opcionalmente, ocultar la opción Búsqueda semántica. Con el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede establecer el valor predeterminado de dónde debería comenzar la búsqueda en el árbol de contenido, el tamaño máximo del conjunto de resultados, la longitud mínima del término de búsqueda y si se mostrará a los visitantes la opción Búsqueda semántica de forma predeterminada.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Búsqueda rápida es la versión 3, que se introdujo con [versión 2.32.0](/help/versions.md) de los componentes principales agregando una opción de búsqueda semántica opcional y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 3 | - | Compatible* | Compatible* | Compatible |
| [Versión 2](/help/components/v2/quick-search.md) | - | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/quick-search.md) | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | - | Compatible |

*La opción de búsqueda semántica solo está disponible con AEM as a Cloud Service.

Para obtener más información acerca de las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de componentes principales.](/help/versions.md)

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Búsqueda rápida, ver ejemplos de sus opciones de configuración y la salida de HTML y JSON, visite la [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_search_es)

## Detalles técnicos {#technical-details}

>[!NOTE]
>
>La protección del componente de búsqueda o de cualquier aplicación basada en AEM contra ataques DOS debe implementarse en un nivel superior, por ejemplo utilizando `mod_security` en Dispatcher.

La documentación técnica más reciente sobre el componente Búsqueda rápida [&#x200B; se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_search_v3)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir dónde debería comenzar la búsqueda en el árbol de contenido y, opcionalmente, ocultar la opción Búsqueda semántica.

![Cuadro de diálogo de edición del componente Búsqueda rápida](/help/assets/quick-search-edit-v3.png)

**Raíz de búsqueda**: página raíz desde la que se inicia la búsqueda. La raíz de búsqueda puede ser un modelo maestro, un idioma maestro o una página normal.
* **ID**: esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos.](/help/developing/data-layer/overview.md)
  * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
  * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
  * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.
* **Ocultar opción de búsqueda semántica en esta instancia**: cuando está marcada, la opción de búsqueda semántica está oculta, independientemente de lo que el [cuadro de diálogo de diseño](#design-dialog) esté configurado para mostrar.
  * Deje sin marcar para utilizar la plantilla predeterminada.
  * Esta opción no puede forzar que se muestre la opción en una ubicación en la que el cuadro de diálogo de diseño la oculta.

>[!NOTE]
>
>Si la **Raíz de búsqueda** no está configurada o no se puede resolver, la Búsqueda rápida toma como valor predeterminado la búsqueda debajo de la página actual.

>[!NOTE]
>
>La opción Búsqueda semántica solo devuelve resultados con tecnología de IA cuando el entorno está configurado con AEM Content AI. En entornos AEM 6.5 y AEM 6.5 LTS que no están configurados con inteligencia artificial aplicada al contenido, oculte la opción [usando el cuadro de diálogo de diseño](#design-dialog) para que no se ofrezca a los visitantes un modo de búsqueda que no funcione.

## Cuadro de diálogo Diseño {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el lugar en el que en el árbol de contenido debe comenzar la búsqueda, así como un tamaño máximo del conjunto de resultados, una longitud mínima del término de búsqueda y si la opción Búsqueda semántica se muestra a los visitantes de forma predeterminada.

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente Búsqueda rápida](/help/assets/quick-search-design-v3.png)

* **Raíz de búsqueda**: el valor predeterminado de la raíz de búsqueda cuando un autor de contenido coloca el componente Búsqueda rápida en una página de contenido
* **Tamaño de resultados**: el número máximo de resultados recuperados por una solicitud de búsqueda
* **Longitud mínima del término de búsqueda**: Longitud mínima del término de búsqueda para iniciar la búsqueda.
* **Ocultar alternancia de búsqueda semántica**: cuando está marcada, la opción **Búsqueda semántica** descrita en [Uso](#usage) no se muestra a los visitantes del sitio de forma predeterminada, y el componente se comporta como [el componente v2 (solo búsqueda de texto completo).](/help/components/v2/quick-search.md)
  * Desactivado de forma predeterminada.
  * Los autores de contenido también pueden invalidar esto para un componente de búsqueda rápida individual en el cuadro de diálogo de [edición.](#edit-dialog)

>[!NOTE]
>
>La opción Búsqueda semántica solo devuelve resultados con tecnología de IA cuando el entorno está configurado con AEM Content AI. En entornos AEM 6.5 y AEM 6.5 LTS que no están configurados con IA de contenido, oculte la opción mediante el cuadro de diálogo de diseño para que no se ofrezca a los visitantes un modo de búsqueda que no funcione.

>[!NOTE]
>
>**El tamaño de los resultados** y **la longitud mínima del término de búsqueda** solo se pueden establecer en el modo de diseño y, por lo tanto, solo en el nivel de plantilla, lo que significa que los autores de contenido no pueden modificar estos valores.

>[!CAUTION]
>
>**El tamaño de los resultados** y **la longitud mínima del término de búsqueda** pueden tener un impacto en el rendimiento si se establecen demasiado altos o demasiado bajos, respectivamente.

### Pestaña Estilos {#styles-tab}

El componente Búsqueda rápida es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
