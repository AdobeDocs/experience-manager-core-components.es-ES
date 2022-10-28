---
title: Componente de fragmento de experiencia de correo electrónico
description: El componente Fragmento de experiencia de correo electrónico permite al autor del contenido colocar una variación de fragmento de experiencia en su contenido, al mismo tiempo que admite una estructura de contenido localizada.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 27%

---


# Componente de fragmento de experiencia de correo electrónico {#email-experience-fragment-component}

El componente Fragmento de experiencia de correo electrónico permite al autor del contenido colocar una variación de fragmento de experiencia en su contenido, al mismo tiempo que admite una estructura de contenido localizada.

## Uso {#usage}

El componente Fragmento de experiencia de correo electrónico permite al autor del contenido seleccionar entre las variaciones de fragmento de experiencia existentes y colocar una dentro del contenido. Un fragmento de experiencia es un grupo de contenido que incluye contenido y diseño y que se puede reutilizar en todos los canales.

* Las propiedades del componente se pueden definir en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente al agregarlo al contenido se pueden definir en la variable [cuadro de diálogo de diseño](#design-dialog).

El componente Fragmento de experiencia de correo electrónico admite una estructura de sitio localizada.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de experiencia de correo electrónico es v1, que se introdujo con la versión X de los componentes principales de correo electrónico en octubre de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones del componente principal de correo electrónico, consulte el documento [Versiones de los componentes principales de correo electrónico.](/help/email/versions.md)

## Compatibilidad con la estructura del sitio localizada {#localized-site-structure}

El componente Fragmento de experiencia de correo electrónico se adapta a las estructuras de contenido localizadas y representa el fragmento de experiencia adecuado en función de la localización del contenido. Para ello, el fragmento de experiencia debe cumplir las siguientes condiciones.

* El componente Fragmento de experiencia de correo electrónico se agrega a una [plantilla de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* Esa plantilla se utiliza para crear una nueva página de contenido que forma parte de una estructura localizada debajo de `/content/<site>`.
* El fragmento de experiencia al que se hace referencia en una página de contenido forma parte de una estructura de fragmento de experiencia localizada a continuación `/content/experience-fragments` que sigue los mismos patrones que el sitio de abajo `/content/<site>` incluido el uso de los mismos nombres de componentes.

En este caso, el fragmento con la misma localización ([idioma, modelo o Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)), ya que la página actual se representará como parte de la plantilla.

Este comportamiento se limita a los componentes de fragmento de experiencia de correo electrónico que se agregan a las plantillas. Los componentes de fragmento de experiencia añadidos a páginas de contenido individuales representarán las representaciones exactas del fragmento de experiencia configuradas dentro del componente.

* Para ver un ejemplo del funcionamiento de las funciones de localización del componente Fragmento de experiencia, consulte [la siguiente sección](#example).
* Para ver un ejemplo de cómo funcionan juntas las funciones de localización de los componentes principales, consulte la [página Funciones de localización de los componentes principales](/help/get-started/localization.md).

### Ejemplo {#example}

Digamos que el contenido tiene este aspecto:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Verá que la estructura siguiente `/content/experience-fragments/wknd` refleja la estructura de `/content/wknd`.

En este caso, si el componente Fragmento de experiencia de correo electrónico `/content/experience-fragments/wknd/us/en/footerTextXf` se coloca en una plantilla, las páginas localizadas creadas en función de esa plantilla renderizarán automáticamente el fragmento de experiencia localizado que corresponda a la página de contenido localizada.

Por lo tanto, si se desplaza a una página de contenido en `/content/wknd/ch/de` que utiliza la misma plantilla, se procesará `/content/experience-fragments/wknd/ch/de/footerTextXf` en lugar de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Abandono {#fallback}

El componente Fragmento de experiencia de correo electrónico intentará encontrar un componente localizado correspondiente en el siguiente orden.

1. Primero intenta encontrar una raíz de idioma.
1. Si no se encuentra, intenta encontrar un modelo.
1. Si no se encuentra, intenta encontrar una versión activa.
1. Si no se encuentra, el valor predeterminado es el fragmento de experiencia configurado en el componente.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Fragmento de experiencia de correo electrónico, así como ver ejemplos de sus opciones de configuración, así como los resultados de HTML y JSON, visite [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_xf)

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de experiencia [se encuentra en GitHub.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

Encontrará más información sobre el desarrollo de los componentes principales en la [Documentación para desarrolladores de componentes principales .](/help/developing/overview.md)

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido seleccionar la variación del fragmento de experiencia que se debe representar en el contenido.

![Cuadro de diálogo de edición del componente de fragmento de experiencia de correo electrónico](/help/email/assets/email-experience-fragment-edit.png)

Utilice la variable **Abrir cuadro de diálogo de selección** para abrir el selector de componentes y elegir qué variación de componente de fragmento de experiencia se agregará a la página de contenido.

Si agrega el componente Fragmento de experiencia de correo electrónico a una plantilla, se localizará automáticamente siempre que los fragmentos de experiencias estén localizados, por lo que lo que se procese en la página puede variar del componente que seleccione explícitamente. [Consulte el ejemplo anterior](#example) para obtener más información.

También puede definir un **ID**. Esta opción permite controlar el identificador único del componente en el HTML.

* Si se deja en blanco, se genera automáticamente un ID único y se puede encontrar inspeccionando el contenido resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar a CSS.

### Pestaña Estilos {#styles-tab-edit}

El componente Fragmento de experiencia de correo electrónico admite el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en la variable [cuadro de diálogo de diseño](#design-dialog) para que la pestaña esté disponible.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor de contenido que utiliza el componente Fragmento de experiencia de correo electrónico y los valores predeterminados establecidos al colocar el componente Fragmento de experiencia de correo electrónico.

### Pestaña Estilos {#styles-tab}

El componente Fragmento de experiencia de correo electrónico admite el AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)
