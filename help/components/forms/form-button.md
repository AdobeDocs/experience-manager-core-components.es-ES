---
title: Componente Botón de formulario
description: El componente principal Formulario oculto permite incluir un campo oculto en un formulario.
role: Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
TQID: https://experienceleague.adobe.com/GzfypWAMUQGej1-z15cKVe27SOkrovYOL5E-FsTRBkE
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 416
ht-degree: 100%

---

# Componente Botón de formulario {#form-button-component}

El componente principal Botón de formulario permite incluir un botón para activar una acción en una página.

## Uso {#usage}

El componente principal Botón de formulario permite crear un campo de botón, a menudo para activar el envío del formulario y está pensado para utilizarse junto con el [componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir las propiedades del botón en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón de formulario es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 2 | Compatible con la <br>[versión 2.17.4](/help/versions.md) y anteriores | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/form-button-v1.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Botón de formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_button_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Botón de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite que el autor del contenido defina los parámetros del botón.

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de edición del componente Botón de formulario](/help/assets/form-button-edit.png)

* **Tipo**

   * **Botón**
   * **Enviar**

* **Título**: texto que se muestra en el botón

   * Si no se proporciona ninguno, el valor predeterminado es el tipo de botón

* **Nombre**: el nombre del botón, que se envía con los datos del formulario
* **Valor:** el valor del botón, que se envía con los datos del formulario

* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón de formulario es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).
