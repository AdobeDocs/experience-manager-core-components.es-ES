---
title: Componente Navegación de idioma
description: El componente Navegación de idioma proporciona un idioma o navegación por país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---


# Componente Navegación de idioma{#language-navigation-component}

El componente Navegación de idioma proporciona un idioma o navegación por país para un sitio, de modo que los visitantes pueden navegar a la misma página en una configuración regional diferente.

{{traditional-aem}}

## Uso {#usage}

Los sitios web a menudo se ofrecen en varios idiomas para diferentes regiones. El componente Navegación de idioma permite que un visitante vea la misma página en diferentes idiomas o configuraciones regionales. De esta forma, si el usuario es un lector de la versión en alemán suizo del sitio web, puede fácilmente cambiar a la versión en inglés de EE. UU. de la misma página. El componente Navegación de idioma controla la comprensión de la estructura de idioma del sitio y encuentra la página correspondiente automáticamente.

* Para ver un ejemplo del funcionamiento de la función de localización del componente Navegación de idioma, consulte [la siguiente sección](#example).
* Para ver un ejemplo del funcionamiento conjunto de las funciones de localización de los demás componentes principales, consulte la página [Funciones de localización de Componentes principales](/help/get-started/localization.md).

El [cuadro de diálogo de edición](#edit-dialog) permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación. Con el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede establecer los valores predeterminados para las mismas opciones.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Navegación de idioma es la versión 2, que se introdujo con la versión 2.18.0 de los componentes principales en febrero de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| Versión 2 | - | Compatible | Compatible | Compatible |
| [Versión 1](v1/language-navigation.md) | Compatible | Compatible | - | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Navegación de idioma, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_langnav_es).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Navegación de idioma [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite definir la raíz de navegación del sitio global, así como la profundidad en la estructura que debe ir la navegación.

Normalmente, estas configuraciones solo deben realizarse en el nivel de plantilla de página. Sin embargo, se pueden cambiar a nivel de página mediante el [cuadro de diálogo de edición](#edit-dialog).

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente Navegación de idioma](/help/assets/language-navigation-design.png)

* **Raíz de navegación**
   * Aquí es donde debería comenzar la navegación por el idioma del sitio.
   * La estructura de idioma del sitio comienza en el siguiente nivel debajo de esta raíz.
* **Profundidad de la estructura de idiomas**
   * Así es como muchos niveles del árbol de contenido debajo de **Raíz de navegación** representan la estructura de idioma del sitio. Ejemplos:
      * `1` normalmente significa que solo tiene la opción de idioma.
      * `2` normalmente significa que tiene una elección de idioma y país.
      * `3` normalmente significa que tiene una opción de idioma, país y región.

#### Ejemplo {#example}

Digamos que el contenido tiene este aspecto:

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para el sitio WKND, es probable que desee colocar el componente Navegación de idioma en una plantilla de página como parte del encabezado. Una vez que forme parte de la plantilla, puede establecer la **Raíz de navegación** del componente en `/content/wknd`, ya que allí es donde comienza el contenido localizado para ese sitio. También deberá configurar la **Profundidad de la estructura de idioma** para que sea `2`, ya que la estructura es de dos niveles (país e idioma).

Con el valor **Raíz de navegación**, el componente Idioma sabe que después de `/content/wknd` comienza la navegación y puede generar opciones de navegación reconociendo los dos niveles siguientes del árbol de contenido como la estructura de navegación de idioma del sitio (tal como se define en el valor **Profundidad de la estructura de idioma**).

Independientemente de la página que esté viendo un usuario, el componente Navegación de idioma puede encontrar la página correspondiente en otro idioma, conociendo la ubicación de la página actual y trabajando hacia atrás hasta la raíz, y luego reenviando a la página correspondiente.

### Pestaña Estilos {#styles-tab}

El componente Navegación de idioma es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).

## Cuadro de diálogo de edición {#edit-dialog}

### Pestaña Propiedades {#properties-tab-edit}

Normalmente, el componente Navegación de idioma solo necesita agregarse y configurarse en las plantillas de página de un sitio. Sin embargo, si es necesario añadir el componente Navegación de idioma a una página de contenido individual, el cuadro de diálogo de edición permite a un autor de contenido configurar los mismos valores que se describen en el [cuadro de diálogo de diseño](#design-dialog)

Además, puede establecer un **ID**. Esta opción permite controlar el identificador único del componente en el HTML y en la [capa de datos](/help/developing/data-layer/overview.md).

* Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
* Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
* Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

![Cuadro de diálogo de edición del componente Navegación de idioma](/help/assets/language-navigation-edit.png)

### Pestaña Accesibilidad {#accessibility-tab}

* **Etiqueta**: esta opción debe definirse si hay más de un idioma de navegación en la página para establecer el atributo de etiqueta aria del componente.

![Pestaña Accesibilidad de navegación por idiomas](/help/assets/language-navigation-edit-accessibility.png)

### Pestaña Estilos {#styles-tab-edit}

El componente Navegación de idioma es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

Utilice la lista desplegable para seleccionar los estilos que desea aplicar al componente. Las selecciones realizadas en el cuadro de diálogo de edición tienen el mismo efecto que las seleccionadas en la barra de herramientas de componentes.

Los estilos deben configurarse para este componente en el [cuadro de diálogo de diseño](#design-dialog) para que el menú desplegable esté disponible.

![Pestaña Estilos del cuadro de diálogo de edición del componente de navegación de idioma](/help/assets/language-navigation-edit-styles.png)

## Capa de datos del cliente de Adobe {#data-layer}

El componente Navegación de idioma es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
