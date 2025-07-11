---
title: Componente Fragmento de contenido de correo electrónico
description: El componente Fragmento de contenido de correo electrónico permite la visualización de un fragmento de contenido en el contenido.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Fragmento de contenido de correo electrónico {#email-content-fragment-component}

El componente Fragmento de contenido de correo electrónico permite la visualización de un [fragmento de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es) en el contenido.

## Uso {#usage}

El componente Fragmento de contenido de correo electrónico permite la inclusión de un [fragmento de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=es) en el contenido del correo electrónico. Los fragmentos de contenido son contenido estructurado multicanal que se puede crear de forma centralizada y reutilizar fácilmente.

* El fragmento y sus propiedades se pueden seleccionar en el [cuadro de diálogo de configuración.](#configure-dialog)
* Los tipos de recursos para gestionar ciertas imágenes y cuadrículas se pueden definir en el [cuadro de diálogo de diseño.](#design-dialog)
* La opción de edición abre el fragmento seleccionado dentro del [editor de fragmentos de contenido,](#edit-dialog) personalizado para usarse con los componentes principales de correo electrónico.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de contenido de correo electrónico es la versión 1, que se introdujo con la versión X de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| Versión 1 | Compatible | - | - |

Para obtener más información acerca de las versiones y publicaciones de los componentes principales de correo electrónico, consulte el documento [Versiones de los componentes principales de correo electrónico.](/help/email/versions.md)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente acerca del componente Fragmento de contenido de correo electrónico [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Puede encontrar más información acerca del desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales.](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir qué fragmento de contenido y qué elementos de ese fragmento se incluyen.

### Pestaña Propiedades {#properties-tab}

![Componente Fragmento de contenido de correo electrónico](/help/email/assets/email-content-fragment-edit-properties.png)

* **Fragmento de contenido**

   * Ruta al fragmento de contenido deseado
   * Se puede utilizar el **Cuadro de diálogo de selección** para localizar el fragmento

* **Modo de visualización**
   * **Elemento de texto único**: permite la selección de un elemento de texto multilínea y activa las opciones de control de párrafo
* **Variación**: qué variación del fragmento de contenido se va a utilizar (el valor predeterminado es **Principal**)

* **ID**: esta opción permite controlar el identificador único del componente en el HTML.
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando el contenido resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al CSS.

### Pestaña Control de párrafo {#paragraph-control-tab}

![Componente Fragmento de contenido de correo electrónico](/help/assets/content-fragment-edit-paragraph.png)

* **Párrafos**: permite seleccionar todos los párrafos o un intervalo
   * **Todos**: mostrar todos los párrafos
   * **Intervalo**
      * Especifique los intervalos de párrafos que se deben mostrar, separados por punto y coma
      * Por ejemplo, `1;3-5;7;9-*` para incluir los párrafos primero, tercero a quinto, séptimo y noveno a último
* **Gestionar encabezados como sus propios párrafos**

## Cuadro de diálogo de edición {#edit-dialog}

Una vez que haya utilizado el componente Fragmento de contenido de correo electrónico para configurar un fragmento de contenido, al seleccionar el componente en el editor de contenido, se muestra una opción **Editar**.

![Barra de herramientas del componente Fragmento de contenido de correo electrónico](/help/email/assets/email-content-fragment-edit-toolbar.png)

Al tocar o hacer clic en el botón **Editar**, se abre el editor de fragmentos de contenido. El editor de fragmentos de contenido se ha ampliado para incluir botones para que **Seleccionar la variable de Adobe Campaign** inserte variables de Adobe Campaign en los fragmentos de contenido.

![Editor de fragmentos de contenido para correo electrónico](/help/email/assets/email-content-fragment-editor.png)

Para obtener más información acerca de la edición y creación de fragmentos de contenido, consulte el documento [Creación de contenido de fragmentos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html?lang=es)

## Cuadro de diálogo de diseño {#design-dialog}

Cuando se configura un componente Fragmento de contenido de correo electrónico con un fragmento de contenido, al seleccionarlo en el editor de contenido, la barra de herramientas muestra un botón para abrir el editor de fragmentos de contenido.


### Pestaña Principal {#main-tab}

![Cuadro de diálogo de diseño del componente Fragmento de contenido de correo electrónico](/help/email/assets/email-content-fragment-design.png)

* **Cuadrícula interactiva interna**

   * El tipo de recurso de sling que se utiliza para la cuadrícula interactiva interna

### Pestaña Estilos {#styles-tab}

El componente Fragmento de experiencia de correo electrónico es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.
