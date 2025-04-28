---
title: Componente Botón de correo electrónico
description: El componente Botón de correo electrónico permite la configuración y visualización de un elemento de botón en el contenido.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 100%

---


# Componente Botón de correo electrónico {#email-button-component}

El componente Botón de correo electrónico permite la configuración y visualización de un elemento de botón en el contenido.

## Uso {#usage}

El componente Botón de correo electrónico permite incluir un botón en el contenido, en el que se puede hacer clic, y que enlaza a recursos adicionales.

* Las propiedades del botón se pueden seleccionar en el [cuadro de diálogo de configuración.](#configure-dialog)
* Los estilos del componente Botón de correo electrónico se pueden definir en el [cuadro de diálogo de diseño.](#design-dialog)

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Botón de correo electrónico es la versión 1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | - | - |

Para obtener más información acerca de las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales de correo electrónico.](/help/email/versions.md)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente acerca del componente Botón de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite que el autor del contenido defina el botón y cómo se comporta y aparece para un lector.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente Botón](/help/email/assets/email-button-edit-properties.png)

* **Texto**: Texto que se muestra en el botón
   * Haga clic en el icono de Campaign para abrir el diálogo [Seleccionar la variable de Adobe Campaign](/help/email/campaign-variables.md) e insertar contenido dinámico desde Adobe Campaign.
* **Vínculo**: vínculo a una página de contenido dentro de AEM, un recurso externo o un anclaje
   * Utilice el **Cuadro de diálogo de selección** para elegir una ruta dentro de AEM.
   * Haga clic en el icono de Campaign para abrir el diálogo [Seleccionar la variable de Adobe Campaign](/help/email/campaign-variables.md) e insertar contenido dinámico desde Adobe Campaign.
* **Icono**: identificador de iconos para mostrar un icono en el botón
* **ID**: esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.
* **Abrir en ficha nueva**: si se selecciona, el vínculo se abre en una nueva pestaña del explorador.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Accesibilidad del cuadro de diálogo de edición del componente Botón](/help/email/assets/email-button-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: valor de un atributo de etiqueta ARIA para el componente

### Pestaña Estilos {#styles-tab-edit}

El componente Botón de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Botón de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
