---
title: Componente Navegación
description: El componente Navegación permite a los usuarios navegar fácilmente por una estructura de sitio globalizada.
role: Architect, Developer, Admin, User
exl-id: 9154f2a3-3d1e-4865-a413-298748fa66d3
source-git-commit: eea159ad494150c3f132166d48f624605eb92e64
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 94%

---

# Componente Navegación{#navigation-component}

El componente Navegación permite a los usuarios navegar fácilmente por una estructura de sitio globalizada.

## Uso {#usage}

El componente de navegación enumera un árbol de páginas para que los usuarios de un sitio puedan navegar fácilmente por su estructura.

El componente de navegación puede detectar automáticamente la estructura globalizada del sitio y [adaptarse automáticamente a una página localizada.](#localized-site-structure) Además, puede admitir cualquier estructura de sitio arbitraria utilizando [páginas de redireccionamiento de sombras](#shadow-structure) para representar una estructura distinta a la del contenido principal.

El [cuadro de diálogo de edición](#edit-dialog) permite que el autor del contenido defina la página raíz de navegación junto con la profundidad de navegación. El [cuadro de diálogo de diseño](#design-dialog) permite que el autor de la plantilla defina los valores predeterminados para la raíz y profundidad de navegación.

## Compatibilidad con la estructura del sitio localizada {#localized-site-structure}

Los sitios web a menudo se ofrecen en varios idiomas para diferentes regiones. Normalmente, cada página localizada contiene un elemento de navegación que se incluye como parte de la plantilla de página. El componente de navegación le permite colocarlo una vez en una plantilla para todas las páginas del sitio y, a continuación, se adaptará automáticamente para cada página localizada en función de la estructura del sitio globalizada.

* Para ver un ejemplo del funcionamiento de la función de localización del componente de navegación, consulte [la siguiente sección](#example-localization).
* Para ver un ejemplo de cómo funcionan juntas las funciones de localización de los componentes principales, consulte la [página Funciones de localización de los componentes principales](/help/get-started/localization.md).

### Ejemplo {#example-localization}

Digamos que el contenido tiene este aspecto:

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

Para el WKND del sitio, probablemente quiera colocar el componente de navegación en una plantilla de página como parte del encabezado. Una vez que forme parte de la plantilla, puede establecer la **Raíz de navegación** del componente en `/content/wknd/language-masters/en`, ya que ahí es donde comienza el contenido maestro para ese sitio. Tal vez también quiera configurar la **Profundidad de la estructura de navegación** para que sea `2`, ya que probablemente no quiera que el componente muestre todo el árbol de contenido, sino los dos primeros niveles, de modo que sirva como descripción general.

Con el valor **Raíz de navegación**, el componente de navegación sabe que después de `/content/wknd/language-masters/en` comienza la navegación y puede generar opciones de navegación recurriendo a la estructura del sitio en dos niveles hacia abajo (según se defina en el valor **Profundidad de la estructura de navegación**).

Independientemente de la página localizada que esté viendo un usuario, el componente Navegación puede encontrar la página localizada correspondiente conociendo la ubicación de la página actual, trabajando hacia atrás hasta la raíz y luego reenviando a la página correspondiente.

Por lo tanto, si un visitante está viendo `/content/ch/de/experience/arctic-surfing-in-lofoten`, el componente sabe que genera la estructura de navegación basada en `/content/wknd/language-masters/de`. Del mismo modo, si el visitante está viendo `/content/us/en/experience/arctic-surfing-in-lofoten`, el componente sabe generar la estructura de navegación basada en `/content/wknd/language-masters/en`.

## Compatibilidad con la estructura del sitio en la sombra {#shadow-structure}

A veces es necesario crear un menú de navegación para el visitante que sea diferente a la estructura real del sitio. Una promoción debería resaltar cierto contenido del menú reorganizando la lista de contenido. Con las páginas en la sombra, que simplemente se redirigen a otras páginas de contenido, el componente de navegación puede generar cualquier estructura de navegación arbitraria necesaria.

Para ello, deberá:

1. Crear páginas en la sombra como páginas vacías que representen la estructura del sitio deseada. A menudo, esto se denomina estructura de sitio en la sombra.
1. Configure los valores **Redirigir** en las propiedades de página de estas páginas para que apunten a las páginas de contenido real.
1. Establezca la opción **Ocultar en navegación** en las propiedades de página de las páginas en la sombra.
1. Establezca el valor **Raíz de navegación** del componente de navegación para que apunte a la raíz de la nueva estructura del sitio en la sombra.

A continuación, el componente de navegación procesará el menú basado en la estructura del sitio en la sombra. Los vínculos que representa el componente son a las páginas de contenido real a las que las páginas en la sombra se redirigen y no a las propias páginas en la sombra. Además, el componente muestra los nombres de las páginas reales y resalta correctamente la página activa, incluso cuando la navegación se basa en páginas en la sombra. El componente de navegación hace que las páginas en la sombra sean totalmente transparentes para el visitante.

>[!NOTE]
>Las páginas en la sombra hacen que sus opciones de navegación sean mucho más flexibles, pero tenga en cuenta que el mantenimiento de esta estructura es completamente manual. Si reorganiza el contenido real del sitio o añade o elimina contenido, deberá actualizar manualmente la estructura en la sombra según sea necesario.

>[!NOTE]
>Al procesar una estructura de sitio en la sombra, la lógica de navegación solo recurre a las páginas en la sombra. La lógica no repite la estructura de los destinos de redireccionamiento.

## Redirecciones en navegación {#redirects}

Cuando una página tiene un objetivo de redirección (independientemente de si apunta a una dirección URL externa o a otra página AEM), un componente de navegación que contiene vínculos a ese punto directamente a la dirección URL del destino de redirección.

### Ejemplo {#redirect-example}

* Cree una página A que redirija a la página B.
* Cree una página C que redirija a `https://aemcomponents.dev`
* En una página D, inserte un componente de navegación o que contenga las páginas A y C
* Los vínculos respectivos que se generan luego apuntan directamente a la página B y `https://aemcomponents.dev`


## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación es la versión 1, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| Versión 1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente de navegación, ver ejemplos de sus opciones de configuración y la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_navigation).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

>[!NOTE]
>
>A partir de la versión 2.1.0 de los componentes principales, el componente de navegación admite [microdatos de schema.org](https://schema.org).

## Cuadro de diálogo de edición {#edit-dialog}

En el cuadro de diálogo de edición, el autor del contenido puede definir la página raíz para la navegación y la profundidad de la estructura de navegación.

### Pestaña Propiedades {#properties-tab}

![Pestaña Propiedades del cuadro de diálogo de edición del componente de navegación](/help/assets/navigation-edit-properties.png)

* **Raíz de navegación**: página raíz que se utilizará para generar el árbol de navegación.
* **Excluir niveles de la raíz**: a menudo, la raíz no se debe incluir en la navegación. Esta opción le permite especificar cuántos niveles superiores de la raíz desea excluir. Por ejemplo:
   * 0 = mostrar el nivel raíz
   * 1 = excluir el nivel raíz
   * 2 = excluir la raíz y 1 nivel más arriba
   * etc.
* **Recopilar todas las páginas secundarias**: recopile todas las páginas que sean descendientes de la raíz de navegación.
* **Profundidad de la estructura de navegación**: define cuántos niveles hay en el árbol de navegación que el componente debe mostrar en relación con la raíz de navegación (solo disponible cuando no se ha seleccionado **Recopilar todas las páginas secundarias**).
* **Deshabilitar sombreado**: si la página en la jerarquía es una redirección, se mostrará el nombre de la página de redirección en lugar del destino. Consulte [Compatibilidad con la estructura del sitio en la sombra](#shadow-structure) para obtener más información.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

### Pestaña Accesibilidad {#accessibility-tab}

![Pestaña de accesibilidad del cuadro de diálogo de edición del componente de navegación](/help/assets/navigation-edit-accessibility.png)

En la pestaña **Accesibilidad**, se pueden configurar valores para las etiquetas de [accesibilidad ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) del componente.

* **Etiqueta**: Valor de un atributo de etiqueta ARIA para el componente

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla establecer los valores predeterminados para la página raíz de navegación y la profundidad de navegación que se presentan a los autores de contenido.

### Pestaña Propiedades {#properties-tab-design}

![Cuadro de diálogo de diseño del componente de navegación](/help/assets/navigation-design.png)

* **Raíz de navegación**: el valor predeterminado de la página raíz de la estructura de navegación, que se utilizará para generar el árbol de navegación y tendrá un valor predeterminado cuando el autor de contenido añada el componente a la página.
* **Excluir niveles de la raíz**: a menudo, la raíz no se debe incluir en la navegación. Esta opción le permite especificar el valor predeterminado de cuántos niveles superiores de la raíz desea excluir. Por ejemplo:
   * 0 = mostrar el nivel raíz
   * 1 = excluir el nivel raíz
   * 2 = excluir la raíz y 1 nivel más arriba
   * etc.
* **Recopilar todas las páginas secundarias**: el valor predeterminado de la opción para recopilar todas las páginas que descendienden de la raíz de navegación.
* **Profundidad de la estructura de navegación**: el valor predeterminado de la profundidad de la estructura de navegación.
* **Deshabilitar en la sombra**: el valor predeterminado de si se debe deshabilitar las páginas en la sombra al añadir un componente de navegación

### Pestaña Estilos {#styles-tab}

El componente de navegación es compatible con el [sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente de navegación es compatible con la [capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
