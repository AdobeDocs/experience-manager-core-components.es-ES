---
title: Componente de fragmento de experiencia
description: El componente Fragmento de experiencia permite al autor del contenido agregar una variación de fragmento de experiencia a una página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 1%

---


# Componente de fragmento de experiencia{#experience-fragment-component}

El componente de fragmento de experiencia de componente principal permite al autor del contenido colocar una variación de fragmento de experiencia en una página mientras se admite una estructura de sitio localizada.

## Uso {#usage}

El componente de fragmento de experiencia de componente principal permite al autor del contenido seleccionar entre las variaciones de fragmento de experiencia existentes y colocar una en la página de contenido. El componente Fragmento de experiencia también admite una estructura de sitio localizada.

* Las propiedades del componente se pueden definir en el cuadro de diálogo [](#configure-dialog)Configurar.
* Los valores predeterminados del componente al agregarlo a una página se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Compatibilidad con la estructura del sitio localizada {#localized-site-structure}

El componente Fragmento de experiencia se adapta a las estructuras del sitio localizadas y procesa el fragmento de experiencia adecuado en función de la localización de la página. Para ello, el fragmento de experiencia debe cumplir las siguientes condiciones.

* El componente Fragmento de experiencia se agrega a una plantilla.
* Esa plantilla se utiliza para crear una nueva página de contenido que forma parte de una estructura localizada a continuación `/content/<site>`.
* El fragmento de experiencia al que se hace referencia en una página de contenido forma parte de una estructura de fragmentos de experiencia localizada a continuación `/content/experience-fragments` que sigue los mismos patrones que el sitio a continuación, `/content/<site>` incluido el uso de los mismos nombres de componentes.

En este caso, el fragmento con la misma localización (idioma, modelo o Live Copy) que la página actual se procesará como parte de la plantilla.

Este comportamiento se limita a los componentes de fragmento de experiencia añadidos a las plantillas. Los componentes de fragmento de experiencia añadidos a páginas de contenido individuales representarán las representaciones exactas de fragmentos de experiencia configuradas dentro del componente.

* Para ver un ejemplo de cómo funcionan las funciones de localización del componente Fragmento de experiencia, consulte [la sección siguiente](#example).
* Para ver un ejemplo de cómo funcionan conjuntamente las funciones de localización de los componentes principales, consulte la página [Características de la](/help/get-started/localization.md)Localización de la páginaComponentes principales.

### Ejemplo {#example}

Supongamos que su contenido tiene este aspecto:

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

Observe que la estructura siguiente `/content/experience-fragments/wknd` refleja la estructura de `/content/wknd`.

En este caso, si el componente Fragmento de experiencia `/content/experience-fragments/wknd/us/en/footerTextXf` se coloca en una plantilla, las páginas localizadas creadas a partir de esa plantilla representarán automáticamente el fragmento de experiencia localizado que corresponde a la página de contenido localizado.

Por lo tanto, si se desplaza a una página de contenido debajo de `/content/wknd/ch/de` la que se utiliza la misma plantilla, `/content/experience-fragments/wknd/ch/de/footerTextXf` se procesará en lugar de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Visitas en el orden previsto {#fallback}

El componente Fragmento de experiencia intentará encontrar un componente localizado correspondiente en el orden siguiente.

1. Primero trata de encontrar una raíz de idioma.
1. Si no se encuentra, intenta encontrar un modelo.
1. Si no se encuentra, intenta encontrar una Live Copy.
1. Si no se encuentra, el valor predeterminado es el fragmento de experiencia configurado en el componente.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Fragmento de experiencia es v1, que se introdujo con la versión 2.6.0 de los componentes principales en septiembre de 2019 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Fragmento de experiencia y ver ejemplos de sus opciones de configuración, así como los resultados HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_xf)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Fragmento de experiencias [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido seleccionar la variación de fragmento de experiencia que se debe representar en la página.

![Cuadro de diálogo de edición del componente Fragmento de experiencia](/help/assets/experience-fragment-edit.png)

Utilice el botón **Abrir cuadro de diálogo** de selección para abrir el selector de componentes y elegir la variación de componente de fragmento de experiencia que desea agregar a la página de contenido.

Si agrega el componente Fragmento de experiencia a una plantilla, tenga en cuenta que se localizará automáticamente siempre que los fragmentos de experiencia estén localizados, por lo que lo que se procese en la página puede variar con respecto al componente que seleccione explícitamente. [Consulte el ejemplo anterior](#example) para obtener más información.

También puede definir un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la capa [](/help/developing/data-layer/overview.md)de datos.

* Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Fragmento de experiencia y los valores predeterminados establecidos al colocar el componente Fragmento de experiencia.

### Ficha Estilos {#styles-tab}

El componente Fragmento de experiencia admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
