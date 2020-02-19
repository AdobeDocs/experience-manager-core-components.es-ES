---
title: Componente de página
description: El componente Página es un componente de página extensible diseñado para trabajar con el editor de plantillas y permitir que el encabezado/pie de página y los componentes de estructura se ensamblen con el editor de plantillas.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de página{#page-component}

El componente Página es un componente de página extensible diseñado para trabajar con el editor [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) plantillas y permite ensamblar el encabezado/pie de página y los componentes de estructura con el editor de plantillas.

## Uso {#usage}

El componente de página forma la base de todas las páginas diseñadas con los componentes principales, así como plantillas editables. Mediante el uso del componente de página, los encabezados, los pies de página y la estructura de la página se pueden definir como una plantilla con los demás componentes principales.

Mediante el cuadro de diálogo [de](#design-dialog)diseño, se pueden definir bibliotecas personalizadas del lado del cliente para la página. A diferencia de otros componentes que tienen un cuadro de diálogo de edición al que se puede acceder directamente desde el componente, dado que el componente es la propia página, el cuadro de diálogo [de](#edit-dialog) edición del componente de página es la ventana de propiedades de página.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Página es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como Cloud Service |
|---|---|---|---|---|
| v2 | Compatible | Compatible | Compatible | Compatible |
| [v1](v1/page-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](/help/versions.md)principales.

>[!NOTE]
>
>Para habilitar la redirección a `cq:Page` nivel para la versión 2 del componente de página y AEM 6.3, se requiere [el Service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) o posterior. Esta redirección no estaba disponible en versiones anteriores.

## Ejemplo de salida de componente {#sample-component-output}

El siguiente es un ejemplo tomado de [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Captura de pantalla {#screenshot}

![](/help/assets/chlimage_1.png)

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Página [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_page_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Edit Dialog {#edit-dialog}

Dado que el componente representa toda la página, la configuración que normalmente estaría en un cuadro de diálogo de edición se encuentra en la ventana Propiedades [de la](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) página.

## Cuadro de diálogo Diseño {#design-dialog}

Dado que el componente representa toda la página, se accede al cuadro de diálogo de diseño mediante Información de **página -> Política** de página al editar la plantilla de página.

![](/help/assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>En versiones anteriores de AEM, la política **de** página se denominaba Diseño **de** página.

### Ficha Propiedades {#properties-tab}

Mediante la ventana Diseño de página, puede definir las bibliotecas de cliente que se van a cargar, así como la biblioteca de recursos web de la página.

* **Bibliotecas** de clienteDefine las categorías de biblioteca de cliente que se van a cargar. JavaScript se agrega al final del cuerpo y CSS al encabezado de la página.
* **Bibliotecas de clientes Cabecera** de página JavaScriptDefine las categorías de biblioteca del cliente JavaScript que se cargarán en el encabezado de página.
   * Las categorías definidas aquí que también están presentes en el campo Bibliotecas **de** cliente tendrán JavaScript cargado en el encabezado de página en lugar de en el extremo del cuerpo.
   * No se cargará CSS a menos que la categoría también esté presente en el campo **Bibliotecas** de clientes.

* **Biblioteca** del cliente de recursos web La categoría de la biblioteca del cliente que se utiliza para proporcionar recursos web, como favoritos.

![](/help/assets/screenshot_2018-10-19at104949.png)

Las bibliotecas se pueden configurar para los campos **Biblioteca** de clientes y Bibliotecas de **clientes Cabecera** de página JavaScript de la siguiente manera:

* Para agregar un nuevo campo, toque o haga clic en el botón **Agregar** debajo de los campos.
* Para eliminar un campo, toque o haga clic en el icono de la papelera situado junto al campo que desee eliminar.
* Para reorganizar el orden de carga, toque o haga clic y arrastre el controlador situado junto al campo que desee mover.

Para obtener más información sobre el uso de bibliotecas del lado del cliente, consulte [Uso de bibliotecas](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)del lado del cliente.

>[!CAUTION]
>
>La capacidad de definir por separado las bibliotecas de cliente para el encabezado de página se introdujo con la versión 2.2.0 de los componentes principales.

### Ficha Estilos {#styles-tab}

El componente Página admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
