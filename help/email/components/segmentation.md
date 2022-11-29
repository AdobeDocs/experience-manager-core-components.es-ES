---
title: Componente de segmentación por correo electrónico
description: El componente Segmentación por correo electrónico
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 16%

---


# Componente de segmentación por correo electrónico {#email-segmentation-component}

El componente Segmentación de correo electrónico utiliza variables de Adobe Campaign para mostrar y ocultar contenido en función del destinatario del contenido.

## Uso {#usage}

El componente Segmentación de correo electrónico permite al autor del contenido ocultar y mostrar contenido en función de las condiciones que cumplan las variables sobre el destinatario que proporciona Adobe Campaign. De este modo, los destinatarios del contenido ven el contenido en función de su segmentación.

* El autor de la plantilla puede utilizar la variable [cuadro de diálogo de diseño](#design-dialog) para definir qué componentes se pueden añadir como segmento.
* El autor de contenido puede usar la variable [cuadro de diálogo configurar](#configure-dialog) para agregar componentes como segmentos y configurar qué segmentos se muestran en función de las variables de Adobe Campaign.

Como alternativa al cuadro de diálogo de configuración, una vez que el autor de contenido ha añadido el componente de segmentación de correo electrónico a una página de contenido, el autor de contenido puede arrastrar y soltar componentes adicionales en los componentes de segmentación de correo electrónico para crear nuevos segmentos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de segmentación por correo electrónico es v1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente de segmentación de correo electrónico, así como ver ejemplos de sus opciones de configuración, así como la salida de HTML y JSON, visite [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente teaser de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo configurar permite al autor del contenido crear, cambiar el nombre y reorganizar segmentos, así como definir el segmento activo. En el componente Segmentación por correo electrónico, un segmento es simplemente otro componente que se oculta o muestra en función de las condiciones que cumple el destinatario del contenido. Puede compararlo con el [Componente de la ficha Componentes principales ,](/help/components/tabs.md) pero en el componente de segmentación solo se muestra el contenido de la pestaña cuyas condiciones se cumplen.

### Pestaña Elementos {#items-tab}

![Pestaña Configurar elementos de diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-items.png)

Utilice la variable **Añadir segmento** para abrir el selector de componentes y elegir qué componente añadir como segmento. Una vez añadida, se añade una entrada a la lista, que contiene los siguientes elementos:

* **Icono** - El icono del tipo de componente del segmento para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Condición** - La condición que debe cumplirse para que este segmento se muestre al destinatario del contenido.
   * Las condiciones disponibles se definen en la variable [diálogo de diseño.](#design-dialog)
   * **Predeterminado** - Define el segmento predeterminado para mostrar si no se cumplen otras condiciones
   * **Personalizado** - Permite al autor definir una condición
      * Las condiciones se basan en variables de personalización de Adobe Campaign
      * [Consulte aquí los recursos de personalización de Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Consulte aquí los recursos de personalización de Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Eliminar** - Toque o haga clic para eliminar el segmento del componente Segmentación de correo electrónico.
* **Reorganizar** - Toque o haga clic y arrastre para reorganizar los segmentos.

>[!TIP]
>
>Si la ventanilla del contenido se reduce para que el cuadro de diálogo de edición se convierta en pantalla completa, la función **Agregar** se ocultará. Los componentes se pueden añadir al componente de segmentación de correo electrónico mediante [arrastrando desde el navegador de componentes y soltando el componente Segmentación de correo electrónico en el editor de contenido.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#inserting-a-component)

### Pestaña Propiedades {#properties-tab}

![Pestaña Configurar propiedades del cuadro de diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se genera automáticamente un ID único y se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar a CSS.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña Configuración de accesibilidad del cuadro de diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: valor de un atributo de etiqueta ARIA para el componente

### Pestaña Estilos {#styles-tab-edit}

El componente Segmentación de correo electrónico es compatible con el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en la variable [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Seleccionar panel {#select-panel}

El autor de contenido puede usar la variable **Seleccionar panel** en la barra de herramientas de componentes para cambiar a otro segmento para editarlo y reorganizar fácilmente los segmentos.

![Icono Seleccionar panel](/help/email/assets/select-panel-icon.png)

Una vez seleccionada la **Seleccionar panel** en la barra de herramientas de componentes, los segmentos configurados se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de los segmentos y se refleja en la numeración.
* El tipo de componente del segmento se muestra primero, seguido de la descripción del segmento en una fuente más ligera.

![Seleccionar la ventana emergente del panel](/help/email/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a ese segmento.
* Los segmentos se pueden reorganizar en su lugar utilizando los controles de arrastre.

>[!NOTE]
>
>Los segmentos se representan como pestañas dentro del editor de páginas para mostrar que hay varias opciones para el contenido final. El autor no puede seleccionar estas pestañas dentro del editor de páginas. Utilice el panel de selección para cambiar entre los segmentos mostrados.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como segmentos al componente de segmentación de correo electrónico, así como definir qué estilos personalizados están disponibles para el autor del contenido.

### Pestaña Componentes permitidos {#allowed-components-tab}

La variable **Componentes permitidos** se utiliza para definir qué componentes puede añadir el autor del contenido como segmentos al componente de segmentación de correo electrónico.

La variable **Componentes permitidos** funciona de la misma manera que la pestaña del mismo nombre cuando [definición de la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Estilos {#styles-tab}

El componente Segmentación de correo electrónico es compatible con el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

### Pestaña Condiciones definidas {#defined-conditions}

Al usar la variable **Condiciones definidas** , el editor de plantillas puede definir qué condiciones están disponibles para que el autor de contenido seleccione al crear segmentos.

![Cuadro de diálogo Diseño ficha Condiciones definidas](/help/email/assets/email-segmentation-design-defined-conditions.png)

Toque o haga clic en el botón **Agregar** para crear nuevas condiciones.

* **Nombre de la condición del segmento** - Una descripción de la condición
* **Condición del segmento** - La condición real que debe cumplirse, en función de las variables de personalización de Adobe Campaign
   * [Consulte aquí los recursos de personalización de Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Consulte aquí los recursos de personalización de Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/)
* **Eliminar** - Toque para hacer clic en para quitar la condición
* **Reorganizar** - Toque o haga clic y arrastre para reorganizar el orden de las condiciones
