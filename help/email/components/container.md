---
title: Componente Contenedor de correo electrónico
description: El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Contenedor de correo electrónico {#email-container-component}

El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico.

## Uso {#usage}

El componente Contenedor de correo electrónico permite crear un contenedor para varios componentes adicionales en el contenido del correo electrónico y se puede utilizar para agrupar otros componentes y aplicar un estilo o diseño común.

* Las propiedades del contenedor se pueden seleccionar en el [cuadro de diálogo de configuración.](#configure-dialog)
* Los valores predeterminados del componente Contenedor de correo electrónico al agregarlo a una página se pueden definir en el [cuadro de diálogo de diseño.](#design-dialog)

Una vez agregado el componente Contenedor de correo electrónico a una página, un autor de contenido puede arrastrar y soltar componentes adicionales en ella.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor de correo electrónico es la versión 1, que se introdujo con la versión X de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | - | - |

Para obtener más información acerca de las versiones y publicaciones de los componentes principales de correo electrónico, consulte el documento [Versiones de los componentes principales de correo electrónico.](/help/email/versions.md)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1_es)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento contenedor y cómo se comporta y aparece en el contenido.

![Cuadro de diálogo de edición del componente Contenedor de correo electrónico](/help/email/assets/email-container-configure.png)

* **Diseño**: esta opción define el comportamiento o el comportamiento de diseño del componente Contenedor de correo electrónico.
   * **Ancho completo**
   * **mitad|mitad**
   * **un tercio|dos tercios**
   * **dos tercios|un tercio**
   * **tercio|tercio|tercio**
* **Color de fondo**: se puede definir como valores RGB de forma libre o utilizando el selector de color, [según la configuración](#container-settings-tab)
* **Imagen de fondo**: define una imagen de fondo para el contenedor, [según la configuración](#container-settings-tab)
* **ID**: esta opción permite controlar el identificador único del componente en HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.

### Pestaña Estilos {#styles-tab-edit}

El componente Contenedor de correo electrónico es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla defina las opciones disponibles para el autor de contenido que utiliza el componente Contenedor de correo electrónico.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente Contenedor de correo electrónico.

La pestaña **Componentes permitidos** funciona del mismo modo que la del mismo nombre cuando [define la directiva y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Componentes predeterminados {#default-components-tab}

La pestaña **Componentes predeterminados** se utiliza para definir qué componente se añade al componente cuando se coloca un tipo de recurso en particular en el contenedor, de forma similar a [cómo se definen los componentes predeterminados en la plantilla de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Configuración de contenedor {#container-settings-tab}

La pestaña **Configuración de contenedor** define si el autor puede establecer una imagen de fondo o un color.

![La pestaña Configuración de contenedor del cuadro de diálogo de diseño del componente Contenedor de correo electrónico](/help/email/assets/email-container-design-container-settings.png)

* **Imagen de fondo**
   * **Habilitar la imagen de fondo**: seleccione esta opción para permitir que el autor del contenido defina una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Habilitar el color de fondo**: seleccione esta opción para permitir que el autor del contenido defina un color de fondo para el contenedor.
   * **Solo muestras**: seleccione esta opción para permitir que el autor del contenido seleccione únicamente muestras de color predefinidas para el color de fondo del contenedor.
      * Solo está disponible cuando se selecciona **Habilitar el color de fondo**
* **Muestras permitidas**: defina los colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo del contenedor
   * Utilice el botón **Añadir** para añadir una muestra de color predefinida. Una vez añadida, se añade una entrada a la lista, que contiene las siguientes columnas:
   * **Valor**: defina el color manualmente mediante valores RGB.
      * Pulse o haga clic en el selector de color para seleccionar más fácilmente un color ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar**: pulse o haga clic para eliminar una muestra.
   * **Reorganizar**: toque o haga clic y arrastre para reordenar las muestras.

### Pestaña Estilos {#styles-tab}

El componente Contenedor de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
