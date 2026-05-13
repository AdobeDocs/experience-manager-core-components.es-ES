---
title: Componente Página (v2)
description: El componente Página es un componente de página ampliable diseñado para trabajar con el editor de plantillas y permitir que el encabezado/pie de página y los componentes de estructura se ensamblen con el editor de plantillas.
role: Developer, Admin, User
exl-id: e85fe4db-6de4-4a84-a54c-bd07a67efed3
index: false
TQID: https://experienceleague.adobe.com/p1V-3XLpA6H-rC-zWIYFqbPkd6HW7bBLWFXaj8aeNAs
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
subfeature_v2: id: f86a5563-8f73-4ec0-be7d-a1782604870a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 662
ht-degree: 100%

---

# Componente Página (v2) {#page-component}

El componente Página es un componente de página ampliable diseñado para trabajar con el [editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es) y permite ensamblar el encabezado/pie de página y los componentes de estructura con el editor de plantillas.

## Uso {#usage}

El componente Página forma la base de todas las páginas diseñadas con los componentes principales, así como las plantillas editables. Mediante el uso del componente Página, los encabezados, los pies de página y la estructura de la página se pueden definir como una plantilla que utilice los demás componentes principales.

Mediante el [cuadro de diálogo de diseño](#design-dialog), se pueden definir bibliotecas personalizadas del lado del cliente para la página. A diferencia de otros componentes que tienen un cuadro de diálogo de edición accesible directamente desde el componente, ya que el componente Página es la propia página, el [cuadro de diálogo de edición](#edit-dialog) del componente Página es la ventana de propiedades de página.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 2 del componente Página, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018.

>[!CAUTION]
>
>Este documento describe la versión 2 del componente Página.
>
>Para obtener más información sobre la versión actual del componente Página, consulte el documento [Componente Página](/help/components/page.md).

## Compatibilidad con la aplicación web progresiva {#pwa-support}

La versión 2.15.0 de los componentes principales introdujo la compatibilidad con las [funciones de aplicaciones web progresivas (PWA) ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html?lang=es) integradas de AEM as a Cloud Service. Con una configuración simple a nivel de sitio, convierta su experiencia AEM en una PWA.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de página [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_page_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

Dado que el componente representa la página completa, la configuración que normalmente estaría en un cuadro de diálogo de edición se encuentra en la ventana [Propiedades de página](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=es).

## Cuadro de diálogo de diseño {#design-dialog}

Dado que el componente representa la página completa, se accede al cuadro de diálogo de diseño a través de **Información de página -> Política de página** al editar la plantilla de página.

![Política de la página](/help/assets/page-policy.png)

>[!NOTE]
>
>En versiones anteriores de AEM, **Política de página** se llamaba **Diseño de página**.

### Pestaña Propiedades {#properties-tab}

Con la ventana Diseño de página, puede definir las bibliotecas de cliente que se van a cargar, así como la biblioteca de recursos web para la página.

* **Bibliotecas de cliente**: define las categorías de biblioteca de cliente que se van a cargar. JavaScript se agrega al final del cuerpo y CSS se agrega al encabezado de la página.
* **Encabezado de página JavaScript de bibliotecas de clientes**: define las categorías de biblioteca de cliente JavaScript que se cargarán en el encabezado de página.
   * Las categorías definidas aquí que también están presentes en el campo **Bibliotecas de cliente** tendrán JavaScript cargado en el encabezado de la página en lugar de en el final del cuerpo.
   * No se cargará CSS a menos que la categoría también esté presente en el campo **Bibliotecas de cliente**.

* **Biblioteca de cliente de recursos web**: categoría de la biblioteca de cliente que se usa para publicar recursos web, como los iconos favoritos.

* **Saltar al selector de elementos de contenido principal**: se utiliza como función de accesibilidad para saltar directamente al contenido principal de la página

![Cuadro de diálogo de diseño de componente de página](/help/assets/page-design.png)

Las bibliotecas se pueden configurar para los campos **Bibliotecas de cliente** y **Encabezado de página de bibliotecas de cliente de JavaScript** de la siguiente manera:

* Para agregar un nuevo campo, toque o haga clic en el botón **Añadir** situado debajo de los campos.
* Para quitar un campo, pulse el icono de la papelera que hay junto al campo que se va a eliminar o haga clic en él.
* Para reorganizar el orden de carga, haga clic o arrastre el controlador situado junto al campo que desee mover.

Para obtener más información sobre el uso de bibliotecas del lado del cliente, consulte [Uso de bibliotecas del lado del cliente](https://helpx.adobe.com/es/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>La capacidad de definir por separado las bibliotecas de cliente para el encabezado de página se ha introducido con la versión 2.2.0 de los componentes principales.

### Pestaña Estilos {#styles-tab}

El componente Página es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente de página es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
