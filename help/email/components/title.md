---
title: Componente Título de correo electrónico
description: El componente Título de correo electrónico es un componente de encabezado de sección de los correos electrónicos que incluye la edición in situ.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 100%

---


# Componente Título de correo electrónico {#email-title-component}

El componente Título de correo electrónico es un componente de encabezado de sección de los correos electrónicos que incluye la edición in situ.

## Uso {#usage}

El componente Título de correo electrónico está diseñado para utilizarse como título o encabezado de una sección del correo electrónico.

* El autor de la plantilla puede definir los niveles de encabezado disponibles en el [cuadro de diálogo de diseño.](#design-dialog)
* El autor del contenido puede seleccionar entre los niveles de encabezados disponibles en el [cuadro de diálogo de edición.](#edit-dialog)

Para ofrecer una mayor comodidad, también está disponible la edición in situ simple del texto del encabezado.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Título de correo electrónico es la versión 1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible  | - |

Para obtener más información acerca de las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de componentes principales de correo electrónico](/help/versions.md).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Título [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir el texto del título, así como seleccionar el nivel de encabezado.

* **Título**: si está vacío, se utilizará el título de la página
   * Haga clic en el icono de la campaña para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **Tipo / Tamaño**: define el nivel de encabezado del título
* **Vínculo**: define el contenido al que se vinculará el título. Puede ser una ruta a una página de contenido, una URL externa o un anclaje de página.
   * Haga clic en el icono de la campaña para abrir el cuadro de diálogo [Seleccione la variable Adobe Campaign](/help/email/campaign-variables.md) para insertar contenido dinámico desde Adobe Campaign.
* **ID**: esta opción permite controlar el identificador único del componente en HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.

![Cuadro de diálogo de edición del componente Título de correo electrónico](/help/email/assets/email-title-edit.png)

El editor in situ también se puede utilizar para editar el texto del componente de título.

![Edición in situ del componente Título de correo electrónico](/help/email/assets/email-title-edit-inline.png)

### Pestaña Estilos {#styles-tab-edit}

El componente Título de correo electrónico es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

![Pestaña Estilos del cuadro de diálogo de edición del componente Título](/help/email/assets/email-title-edit-styles.png)

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir el nivel de encabezado predeterminado que tendrán los componentes de título cuando los creen los autores de contenido.

### Pestaña Tamaños {#sizes-tab}

![Cuadro de diálogo de diseño del componente Título](/help/email/assets/email-title-design.png)

* **Tipos permitidos/tamaños para autores**: habilita o deshabilita los tipos de encabezados que estarán disponibles para los autores de contenido cuando usen el componente Título de correo electrónico.
* **Tipo/tamaño predeterminado**: define el tipo de encabezado que se asignará automáticamente cuando un autor de contenido añada el componente Título de correo electrónico a una página.
* **Deshabilitar el vínculo**: desactiva la compatibilidad con los vínculos en el componente Título de correo electrónico para impedir que los autores de contenido se vinculen desde títulos.

### Pestaña Estilos {#styles-tab}

El componente Título de correo electrónico es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
