---
title: Componente Segmentación de correo electrónico
description: El componente Segmentación de correo electrónico
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Segmentación de correo electrónico {#email-segmentation-component}

El componente Segmentación de correo electrónico utiliza variables de Adobe Campaign para mostrar y ocultar contenido en función del destinatario.

## Uso {#usage}

El componente Segmentación de correo electrónico permite al autor del contenido ocultarlo y mostrarlo en función de las condiciones que cumplan las variables acerca del destinatario proporcionadas por Adobe Campaign. De este modo, los destinatarios del contenido lo ven en función de su segmentación.

* El autor de la plantilla puede utilizar el [cuadro de diálogo de diseño](#design-dialog) para definir qué componentes se pueden añadir como segmento.
* El autor del contenido puede usar el [cuadro de diálogo de configuración](#configure-dialog) para agregar componentes como segmentos y configurar qué segmentos se muestran en función de las variables de Adobe Campaign.

Como alternativa al cuadro de diálogo de configuración, una vez que el autor de contenido ha añadido el componente Segmentación de correo electrónico a una página de contenido, puede arrastrar y soltar componentes adicionales en los componentes Segmentación de correo electrónico para crear nuevos segmentos.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Segmentación de correo electrónico es la versión 1, que se introdujo con la versión x de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | - | - |

### Detalles técnicos {#technical-details}

La documentación técnica más reciente acerca del componente Teaser de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1_es)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido crear, cambiar el nombre y reorganizar segmentos, así como definir el segmento activo. En el componente Segmentación de correo electrónico, un segmento es simplemente otro componente que se oculta o muestra en función de las condiciones que cumple el destinatario del contenido. Puede compararlo con el [componente Pestaña de los componentes principales,](/help/components/tabs.md) pero, en el componente Segmentación, solo se muestra el contenido de la pestaña cuyas condiciones se cumplen.

### Pestaña Elementos {#items-tab}

![Pestaña de configuración de elementos del diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-items.png)

Utilice el botón **Agregar segmento** para abrir el selector de componentes y elegir qué componente añadir como segmento. Una vez agregado, se suma una entrada a la lista, que contiene los siguientes elementos:

* **Icono**: el icono del tipo de componente del segmento para facilitar la identificación en la lista. Pase el ratón por encima para ver el nombre completo del componente como información sobre herramientas.
* **Condición**: la condición que debe cumplirse para que este segmento se muestre al destinatario del contenido.
   * Las condiciones disponibles se definen en el [diálogo de diseño.](#design-dialog)
   * **Predeterminado**: define el segmento predeterminado para mostrar si no se cumplen otras condiciones
   * **Personalizado**: permite al autor definir una condición
      * Las condiciones se basan en variables de personalización de Adobe Campaign
      * [Consulte aquí los recursos de personalización de Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=es)
      * [Consulte aquí los recursos de personalización de Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html?lang=es)
* **Eliminar**: toque o haga clic para eliminar el segmento del componente Segmentación de correo electrónico.
* **Reorganizar**: toque o haga clic y arrastre para reorganizar los segmentos.

>[!TIP]
>
>Si la ventana móvil del contenido se reduce para que el cuadro de diálogo de edición pase a estar en pantalla completa, el botón **Añadir** se ocultará. Los componentes se pueden añadir al componente Segmentación de correo electrónico [arrastrando desde el explorador de componentes y soltando en el componente Segmentación de correo electrónico del editor de contenido.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=es#inserting-a-component)

### Pestaña Propiedades {#properties-tab}

![Pestaña de configuración de propiedades del diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-properties.png)

* **ID**: esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña de configuración de accesibilidad del diálogo del componente Segmentación de correo electrónico](/help/email/assets/email-segmentation-configure-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: valor de un atributo de etiqueta ARIA para el componente

### Pestaña Estilos {#styles-tab-edit}

El componente Segmentación de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Seleccionar panel {#select-panel}

El autor del contenido puede utilizar la opción **Seleccionar panel** de la barra de herramientas de componentes para cambiar a un segmento diferente y editarlo, así como para reorganizar fácilmente los segmentos.

![Icono Seleccionar panel](/help/email/assets/select-panel-icon.png)

Una vez seleccionada la opción **Seleccionar panel** en la barra de herramientas de componentes, los segmentos configurados se muestran como una lista desplegable.

* La lista se ordena según la disposición asignada de los segmentos y se refleja en la numeración.
* El tipo de componente del segmento se muestra primero, seguido de la descripción del segmento con la fuente más clara.

![Seleccionar la ventana emergente del panel](/help/email/assets/select-panel-popover.png)

* Al tocar o hacer clic en una entrada de la lista desplegable, cambia la vista del editor a ese segmento.
* Los segmentos se pueden reorganizar mediante los controladores de arrastre.

>[!NOTE]
>
>Los segmentos se representan como pestañas dentro del editor de páginas para mostrar que hay varias opciones para el contenido final. El autor no puede seleccionar estas pestañas dentro del editor de páginas. Utilice Seleccionar panel para cambiar entre los segmentos mostrados.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir qué componentes se pueden añadir como segmentos al componente Segmentación de correo electrónico, así como definir qué estilos personalizados están disponibles para el autor del contenido.

### Pestaña Componentes permitidos {#allowed-components-tab}

La pestaña **Componentes permitidos** se utiliza para definir qué componentes puede añadir el autor de contenido como segmentos al componente Segmentación de correo electrónico.

La pestaña **Componentes permitidos** funciona del mismo modo que la del mismo nombre cuando [define la directiva y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es)

### Pestaña Estilos {#styles-tab}

El componente Segmentación de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

### Pestaña Condiciones definidas {#defined-conditions}

Mediante la pestaña **Condiciones definidas**, el editor de la plantilla puede definir qué condiciones podrá seleccionar el autor de contenido al crear segmentos.

![Pestaña Condiciones definidas del cuadro de diálogo de diseño](/help/email/assets/email-segmentation-design-defined-conditions.png)

Toque o haga clic en el botón **Añadir** para crear nuevas condiciones.

* **Nombre de la condición del segmento**: una descripción de la condición
* **Condición del segmento**: la condición que debe cumplirse, en función de las variables de personalización de Adobe Campaign
   * [Consulte aquí los recursos de personalización de Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=es)
   * [Consulte aquí los recursos de personalización de Adobe Campaign Classic.]&#x200B;(https://experienceleague.adobe.com/docs/?lang=es
* **Eliminar**: toque o haga clic para quitar la condición
* **Reorganizar**: toque o haga clic y arrastre para reorganizar el orden de las condiciones
