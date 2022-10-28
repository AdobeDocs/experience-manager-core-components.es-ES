---
title: Componente de contenedor de correo electrónico
description: El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 40%

---


# Componente de contenedor de correo electrónico {#email-container-component}

El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico.

## Uso {#usage}

El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico y se puede utilizar para agrupar otros componentes y aplicar un estilo o diseño común.

* Las propiedades del contenedor se pueden seleccionar en el [cuadro de diálogo de configuración.](#configure-dialog)
* Los valores predeterminados del componente Contenedor de correo electrónico al agregarlo a una página se pueden definir en la variable [diálogo de diseño.](#design-dialog)

Una vez agregado el componente Contenedor de correo electrónico a una página, un autor de contenido puede arrastrar y soltar componentes adicionales en ella.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de correo electrónico es v1, que se introdujo con la versión X de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales de correo electrónico, consulte el documento [Versiones de los componentes principales de correo electrónico.](/help/email/versions.md)

## Salida del componente de ejemplo {#sample-component-output}

Para obtener información sobre el componente Contenedor de correo electrónico y ver ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_container)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento contenedor y cómo se comporta y aparece en el contenido.

![Cuadro de diálogo Editar del componente contenedor de correo electrónico](/help/email/assets/email-container-configure.png)

* **Diseño** : esta opción define el comportamiento o el comportamiento de diseño del componente Contenedor de correo electrónico.
   * **ancho completo**
   * **mitad|mitad**
   * **one-third|two-third**
   * **two-third|one-third**
   * **third|third|third**
* **Color de fondo**: se puede definir como valores RGB de forma libre o utilizando el selector de color, [según la configuración](#container-settings-tab)
* **Imagen de fondo** - Define una imagen de fondo para el contenedor, [según la configuración](#container-settings-tab)
* **ID** - Esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se genera automáticamente un ID único y se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar a CSS.

### Pestaña Estilos {#styles-tab-edit}

El componente Contenedor de correo electrónico es compatible con el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en la variable [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Contenedor de correo electrónico .

### Pestaña Componentes permitidos {#allowed-components-tab}

La variable **Componentes permitidos** se utiliza para definir qué componentes puede añadir el autor del contenido como elementos al componente Contenedor de correo electrónico.

La variable **Componentes permitidos** funciona de la misma manera que la pestaña del mismo nombre cuando [definición de la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Componentes predeterminados {#default-components-tab}

La variable **Componentes predeterminados** se utiliza para definir qué componente se añade al componente cuando se coloca un tipo de recurso en particular en el contenedor, de forma similar a [cómo se definen los componentes predeterminados en la plantilla de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Pestaña Configuración de contenedor {#container-settings-tab}

La variable **Configuración de contenedor** define si el autor puede definir una imagen de fondo o un color.

![Ficha Configuración de contenedor del cuadro de diálogo de diseño del componente Contenedor de correo electrónico](/help/email/assets/email-container-design-container-settings.png)

* **Imagen de fondo**
   * **Habilitar imagen de fondo**: seleccione esta opción para permitir que el autor del contenido defina una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Activar color de fondo**: seleccione esta opción para permitir que el autor del contenido defina un color de fondo para el contenedor.
   * **Solo muestras**: seleccione esta opción para permitir que el autor del contenido seleccione únicamente muestras de color predefinidas para el color de fondo del contenedor.
      * Solo está disponible cuando se selecciona **Habilitar color de fondo**
* **Muestras permitidas**: defina los colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo del contenedor
   * Utilice el botón **Añadir** para añadir una muestra de color predefinida. Una vez añadida, se añade una entrada a la lista, que contiene las siguientes columnas:
   * **Valor**: defina el color manualmente mediante valores RGB.
      * Pulse o haga clic en el selector de color para seleccionar más fácilmente un color ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar**: pulse o haga clic para eliminar una muestra.
   * **Reorganizar** - Toque o haga clic y arrastre para reordenar las muestras.

### Pestaña Estilos {#styles-tab}

El componente Contenedor de correo electrónico es compatible con el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)