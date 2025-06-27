---
title: Componente Fragmento de experiencia (v1)
description: El componente Fragmento de experiencia permite al autor del contenido añadir una variación de fragmento de experiencia a una página.
role: Architect, Developer, Admin, User
exl-id: 42230a7b-6feb-4535-baf9-b8fc06978d98
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '770'
ht-degree: 100%

---


# Componente Fragmento de experiencia (v1) {#experience-fragment-component}

El componente principal Fragmento de experiencia permite al autor del contenido colocar una variación de fragmento de experiencia en una página mientras admite una estructura de sitio localizada.

## Uso {#usage}

El componente principal Fragmento de experiencia permite al autor del contenido seleccionar entre las variaciones de fragmento de experiencia existentes y colocar uno en la página de contenido. El componente Fragmento de experiencia también admite una estructura de sitio localizada.

* Las propiedades del componente se pueden definir en el [cuadro de diálogo de configuración](#configure-dialog).
* Los valores predeterminados del componente se pueden definir en el [cuadro de diálogo de diseño](#design-dialog) al agregarlo a una página.

## Versión y compatibilidad {#version-and-compatibility}

Este documento describe la versión 1 del componente Fragmento de experiencia, que se introdujo con la versión 2.6.0 de los componentes principales en septiembre de 2019.

>[!CAUTION]
>
>Este documento describe la versión 1 del componente Fragmento de experiencia.
>
>Para obtener más información sobre la versión actual del componente Fragmento de experiencia, consulte el documento [Componente Fragmento de experiencia](/help/components/experience-fragment.md).

## Compatibilidad con la estructura del sitio localizada {#localized-site-structure}

El componente Fragmento de experiencia se adapta a las estructuras de sitio localizadas y representa el fragmento de experiencia adecuado en función de la localización de la página. Para ello, el fragmento de experiencia debe cumplir las siguientes condiciones.

* El componente Fragmento de experiencia se agrega a una plantilla.
* Esa plantilla se utiliza para crear una nueva página de contenido que forma parte de una estructura localizada debajo de `/content/<site>`.
* El fragmento de experiencia al que se hace referencia en una página de contenido forma parte de una estructura de fragmento de experiencia localizada debajo de `/content/experience-fragments` que sigue los mismos patrones que el sitio debajo de `/content/<site>`, incluido el uso de los mismos nombres de componentes.

En este caso, el fragmento con la misma localización (idioma, modelo o versión activa) que la página actual se procesa como parte de la plantilla.

Este comportamiento se limita a los componentes de fragmento de experiencia añadidos a las plantillas. Los componentes Fragmento de experiencia añadidos a páginas de contenido individuales serán las representaciones exactas de los fragmentos de experiencia configurados dentro del componente.

* Para ver cómo trabajan las funciones de localización del componente Fragmento de experiencia, consulte [la sección siguiente](#example).
* Para ver un ejemplo de cómo funcionan juntas las funciones de localización de los componentes principales, consulte la página [Funciones de localización de los componentes principales](/help/get-started/localization.md).

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

En este caso, si el componente Fragmento de experiencia `/content/experience-fragments/wknd/us/en/footerTextXf` se coloca en una plantilla, las páginas localizadas creadas en función de esa plantilla renderizarán automáticamente el fragmento de experiencia localizado que corresponda a la página de contenido localizada.

Por lo tanto, si se desplaza a una página de contenido en `/content/wknd/ch/de` que utiliza la misma plantilla, se procesará `/content/experience-fragments/wknd/ch/de/footerTextXf` en lugar de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Abandono {#fallback}

El componente Fragmento de experiencia intentará encontrar un componente localizado correspondiente en el siguiente orden.

1. Primero intenta encontrar una raíz de idioma.
1. Si no se encuentra, intenta encontrar un modelo.
1. Si no se encuentra, intenta encontrar una versión activa.
1. Si no se encuentra, el valor predeterminado será el fragmento de experiencia configurado en el componente.

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Fragmento de experiencia, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_xf).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de experiencia [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido seleccionar la variación del fragmento de experiencia que se debe representar en la página.

![Cuadro de diálogo de edición del componente Fragmento de experiencia](/help/assets/experience-fragment-edit.png)

Utilice el botón **Abrir cuadro de diálogo de selección** para abrir el selector de componentes y elegir qué variación del componente Fragmento de experiencia se agregará a la página de contenido.

Si agrega el componente Fragmento de experiencia a una plantilla, tenga en cuenta que se localizará automáticamente siempre que los fragmentos de experiencias estén localizados, por lo que lo que se procese en la página puede variar del componente que seleccione explícitamente. [Consulte el ejemplo anterior](#example) para obtener más información.

También puede definir un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor de contenido que utiliza el componente Fragmento de experiencia y los valores predeterminados establecidos al colocar el componente Fragmento de experiencia.

### Pestaña Estilos {#styles-tab}

El componente Fragmento de experiencia es compatible con el sistema de estilos [AEM](/help/get-started/authoring.md#component-styling).
