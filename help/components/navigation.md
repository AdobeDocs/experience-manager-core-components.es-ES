---
title: Componente de navegación
description: El componente de navegación permite a los usuarios navegar fácilmente por una estructura de sitio globalizada.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 1%

---


# Componente de navegación{#navigation-component}

El componente de navegación permite a los usuarios navegar fácilmente por una estructura de sitio globalizada.

## Uso {#usage}

El componente de navegación lista una lista de un árbol de páginas para que los usuarios de un sitio puedan navegar fácilmente por la estructura del sitio.

El componente de navegación puede detectar automáticamente la estructura globalizada del sitio y [adaptarse automáticamente a una página localizada.](#localized-site-structure) Además, puede admitir cualquier estructura de sitio arbitraria mediante el uso de  [páginas de redireccionamiento de ](#shadow-structure) sombra para representar otra estructura distinta a la estructura de contenido principal.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor del contenido definir la página raíz de navegación junto con la profundidad de navegación. El [cuadro de diálogo de diseño](#design-dialog) permite al autor de la plantilla definir los valores predeterminados para la raíz y la profundidad de navegación.

## Compatibilidad con la estructura del sitio localizada {#localized-site-structure}

Los sitios web se proporcionan a menudo en varios idiomas en diferentes regiones. Normalmente, cada página localizada contendrá un elemento de navegación que se incluye como parte de la plantilla de página. El componente de navegación le permite colocarlo una vez en una plantilla para todas las páginas del sitio y luego se adaptará automáticamente para las páginas localizadas individuales en función de la estructura del sitio globalizado.

* Para ver un ejemplo de cómo funciona la función de localización del componente de navegación, consulte [la sección siguiente](#example-localization).
* Para ver un ejemplo de cómo funcionan juntas las funciones de localización de los componentes principales, consulte las [Características de Localización de la página Componentes principales](/help/get-started/localization.md).

### Ejemplo {#example-localization}

Supongamos que su contenido tiene este aspecto:

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para el WKND del sitio, probablemente desee colocar el componente de navegación en una plantilla de página como parte del encabezado. Una vez que forme parte de la plantilla, puede establecer la **Raíz de navegación** del componente en `/content/wknd/language-masters/en`, ya que es ahí donde comienza el contenido maestro de ese sitio. Quizás también desee configurar la **Profundidad de la estructura de navegación** para que sea `2`, ya que probablemente no desee que el componente muestre todo el árbol de contenido, sino los dos primeros niveles para que sirva de información general.

Con el valor **Raíz de navegación**, el componente de navegación sabe que después de `/content/wknd/language-masters/en` que comienza la navegación y puede generar opciones de navegación recurriendo a la estructura del sitio dos niveles hacia abajo (como se define en el valor **Profundidad de estructura de navegación**).

Independientemente de la página localizada que esté viendo un usuario, el componente Navegación puede encontrar la página localizada correspondiente si conoce la ubicación de la página actual, retrocede a la raíz y luego reenvía a la página correspondiente.

Por lo tanto, si un visitante está viendo `/content/ch/de/experience/arctic-surfing-in-lofoten`, el componente sabe generar la estructura de navegación basada en `/content/wknd/language-masters/de`. Del mismo modo, si el visitante está viendo `/content/us/en/experience/arctic-surfing-in-lofoten`, el componente sabe generar la estructura de navegación basada en `/content/wknd/language-masters/en`.

## Compatibilidad con la estructura del sitio de sombra {#shadow-structure}

A veces es necesario crear un menú de navegación para el visitante que sea diferente de la estructura real del sitio. Quizás una promoción debería resaltar cierto contenido en el menú reorganizando la lista de contenido. Mediante el uso de páginas en la sombra, que simplemente se redirigen a otras páginas de contenido, el componente de navegación puede generar cualquier estructura de navegación arbitraria necesaria.

Para ello deberá:

1. Cree páginas de sombra como páginas vacías que representen la estructura del sitio deseada. Esto generalmente se denomina estructura de sitio de sombra.
1. Configure los valores **Redireccionar** en las propiedades de página de estas páginas para que apunten a las páginas de contenido real.
1. Establezca la opción **Ocultar en navegación** en las propiedades de página de las páginas de sombra.
1. Establezca el valor **Raíz de navegación** del componente de navegación para que apunte a la raíz de la nueva estructura del sitio de sombra.

A continuación, el componente de navegación procesará el menú basado en la estructura del sitio de sombra. Los vínculos procesados por el componente son a las páginas de contenido real a las que las páginas de sombra se redirigen y no a las propias páginas de sombra. Además, el componente muestra los nombres de las páginas reales y resalta correctamente la página activa, incluso cuando la navegación se basa en páginas en la sombra. El componente de navegación hace que las páginas de sombra sean totalmente transparentes para el visitante.

>[!NOTE]
>Las páginas de sombra hacen que las opciones de navegación sean mucho más flexibles, pero tenga en cuenta que el mantenimiento de esta estructura es completamente manual. Si reorganiza el contenido real del sitio o agrega o elimina contenido, deberá actualizar manualmente la estructura de sombra según sea necesario.

>[!NOTE]
>Al procesar una estructura de sitio de sombra, la lógica de navegación solo recurre a las páginas de sombra. La lógica no repite la estructura de los destinos de redireccionamiento.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación es v1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de navegación y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_navigation).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente de navegación admite [microdatos de esquema.org](https://schema.org).

## Editar cuadro de diálogo {#edit-dialog}

En el cuadro de diálogo de edición, el autor del contenido puede definir la página raíz para la navegación y la profundidad de la estructura de navegación.

### Ficha Propiedades {#properties-tab}

![Ficha Propiedades del cuadro de diálogo de edición del componente de navegación](/help/assets/navigation-edit-properties.png)

* **Raíz**  de navegación: página raíz que se utilizará para generar el árbol de navegación.
* **Excluir niveles**  raíz: a menudo, la raíz no se debe incluir en la navegación. Esta opción le permite especificar cuántos niveles superiores de la raíz desea excluir. Por ejemplo:
   * 0 = muestra el nivel de raíz
   * 1 = excluir el nivel raíz
   * 2 = excluir la raíz y 1 nivel más arriba
   * etc.
* **Recopilar todas las páginas**  secundarias: recopile todas las páginas que sean descendientes de la raíz de navegación.
* **Profundidad**  de la estructura de navegación: define cuántos niveles del árbol de navegación debe mostrar el componente en relación con la raíz de navegación (solo disponible cuando no se ha seleccionado  **Recopilar todas las** páginas secundarias).
* **Deshabilitar sombreado** : si la página en la jerarquía es una redirección, se mostrará el nombre de la página de redirección en lugar del destinatario. Consulte la [Compatibilidad con la estructura del sitio de sombra](#shadow-structure) para obtener más información.
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

### Ficha Accesibilidad {#accessibility-tab}

![Ficha de accesibilidad del cuadro de diálogo de edición del componente de navegación](/help/assets/navigation-edit-accessibility.png)

En la ficha **Accesibilidad**, se pueden definir valores para las etiquetas [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla establecer los valores predeterminados para la página raíz de navegación y la profundidad de navegación que se presentan a los autores de contenido.

### Ficha Propiedades {#properties-tab-design}

![Cuadro de diálogo de diseño del componente de navegación](/help/assets/navigation-design.png)

* **Raíz**  de navegación: valor predeterminado de la página raíz de la estructura de navegación, que se utilizará para generar el árbol de navegación y se utilizará de forma predeterminada cuando el autor del contenido agregue el componente a la página.
* **Excluir niveles**  raíz: a menudo, la raíz no se debe incluir en la navegación. Esta opción le permite especificar el valor predeterminado de cuántos niveles superiores de la raíz desea excluir. Por ejemplo:
   * 0 = muestra el nivel de raíz
   * 1 = excluir el nivel raíz
   * 2 = excluir la raíz y 1 nivel más arriba
   * etc.
* **Recopilar todas las páginas**  secundarias: el valor predeterminado de la opción para recopilar todas las páginas que sean descendientes de la raíz de navegación.
* **Profundidad**  de la estructura de navegación: el valor predeterminado de la profundidad de la estructura de navegación.
* **Deshabilitar sombreado** : el valor predeterminado de si se debe desactivar la visualización al agregar un componente de navegación

### Ficha Estilos {#styles-tab}

El componente de navegación admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente de navegación admite la capa de datos del cliente de Adobe [](/help/developing/data-layer/overview.md).
