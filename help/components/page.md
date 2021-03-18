---
title: Componente de página
description: El componente de página es un componente de página ampliable diseñado para trabajar con el editor de plantillas y permitir que el encabezado/pie de página y los componentes de estructura se ensamblen con el editor de plantillas.
role: Arquitecto, Desarrollador, Administrador, Profesional Empresarial
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 3%

---


# Componente de página{#page-component}

El componente de página es un componente de página ampliable diseñado para trabajar con el [editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) y permite ensamblar el encabezado/pie de página y los componentes de estructura con el editor de plantillas.

## Uso {#usage}

El componente de página forma la base de todas las páginas diseñadas con los componentes principales, así como las plantillas editables. Mediante el componente Página , los encabezados, pies de página y la estructura de la página se pueden definir como una plantilla con los demás componentes principales.

Mediante el [cuadro de diálogo de diseño](#design-dialog), se pueden definir bibliotecas personalizadas del lado del cliente para la página. A diferencia de otros componentes que tienen un cuadro de diálogo de edición accesible directamente desde el componente, ya que el componente de página es la propia página, el [cuadro de diálogo de edición](#edit-dialog) del componente de página es la ventana de propiedades de página.

## Compatibilidad con aplicaciones web progresivas {#pwa-support}

La versión 2.15.0 de los componentes principales introdujo la compatibilidad con las funciones AEM como PWA de las aplicaciones web progresivas integradas de un Cloud Service. Con una configuración simple a nivel de sitio, convierta su experiencia AEM en un PWA!

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de página es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatible | Compatible | Compatible |
| [v1](v1/page-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de página [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Editar cuadro de diálogo {#edit-dialog}

Dado que el componente representa la página completa, la configuración que normalmente estaría en un cuadro de diálogo de edición se encuentra en la ventana [Propiedades de página](https://docs.adobe.com/content/help/es-ES/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Diálogo de diseño {#design-dialog}

Dado que el componente representa la página completa, se accede al cuadro de diálogo de diseño a través de **Información de página -> Política de página** al editar la plantilla de página.

![Política de la página](/help/assets/page-policy.png)

>[!NOTE]
>
>En versiones anteriores de AEM, **Política de página** se llamaba **Diseño de página**.

### Ficha Propiedades {#properties-tab}

Con la ventana Diseño de página , puede definir las bibliotecas de cliente que se van a cargar, así como la biblioteca de recursos web para la página.

* **Bibliotecas de cliente** : define las categorías de biblioteca de cliente que se van a cargar. JavaScript se agrega al final del cuerpo y CSS se agrega al encabezado de la página.
* **Cabecera de página JavaScript de bibliotecas de clientes** : define las categorías de biblioteca de cliente JavaScript que se cargarán en el encabezado de página.
   * Las categorías definidas aquí que también están presentes en el campo **Client Libraries** tendrán JavaScript cargado en el encabezado de la página en lugar de en el final del cuerpo.
   * No se cargará CSS a menos que la categoría también esté presente en el campo **Bibliotecas de cliente**.

* **Biblioteca de cliente de recursos web** : la categoría de biblioteca de cliente que se utiliza para servir recursos web como favoritos.

* **Pasar al selector de elementos de contenido principal** : se utiliza como función de accesibilidad para saltar directamente al contenido principal de la página

![Cuadro de diálogo de diseño de componente de página](/help/assets/page-design.png)

Las bibliotecas se pueden configurar para los campos **Client Libraries** y **Client Libraries JavaScript Page Head** de la siguiente manera:

* Para agregar un nuevo campo, toque o haga clic en el botón **Add** situado debajo de los campos.
* Para quitar un campo, toque o haga clic en el icono de la papelera que hay junto al campo que se va a eliminar.
* Para reorganizar el orden de carga, toque o haga clic en y arrastre el controlador situado junto al campo que desee mover.

Para obtener más información sobre el uso de bibliotecas del lado del cliente, consulte [Uso de bibliotecas del lado del cliente](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>La capacidad de definir por separado las bibliotecas de cliente para el encabezado de página se ha introducido con la versión 2.2.0 de los componentes principales.

### Pestaña Estilos {#styles-tab}

El componente Página es compatible con el sistema de estilos AEM [](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente de página es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
