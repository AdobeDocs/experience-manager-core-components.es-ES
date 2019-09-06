---
title: Componente de navegación
seo-title: Componente de navegación
description: nulo
seo-description: El componente de navegación permite a los usuarios navegar fácilmente por una estructura globalizada del sitio.
uuid: 616 c 03 fb -39 b 3-402 a-b 990-f 56 c 87 bc 6 df 4
content-type: referencia
topic-tags: creación
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: da 8 d 67 d 7-b 65 e -4041-bc 0 e-e 998 f 24 a 68 f 9
disttype: dist5
gnavtheme: claro
groupsectionnavitems: nº
hidemerchandisingbar: heredar
hidepromocomponent: heredar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 48d23edbcdf4c4ed70d590cf6c6e4ac1db14f852

---


# Componente de navegación{#navigation-component}

El componente de navegación permite a los usuarios navegar fácilmente por una estructura globalizada del sitio.

## Uso {#usage}

En las listas de componentes de navegación, aparece una lista con un árbol de páginas para que los usuarios de un sitio puedan navegar fácilmente por la estructura del sitio.

El componente de navegación puede detectar automáticamente la estructura del sitio globalizado del sitio y [adaptarse automáticamente a una página localizada.](#localized-site-strucutre) Además, puede admitir cualquier estructura de sitio arbitraria utilizando [las páginas de redirección de sombra](#shadow-structure) para representar otra estructura distinta a la estructura de contenido principal.

El cuadro de diálogo [de edición](#edit-dialog) permite al autor de contenido definir la página raíz de navegación junto con la profundidad de navegación. El cuadro de diálogo [de diseño](#design-dialog) permite que el autor de la plantilla defina los valores predeterminados para la raíz y profundidad de navegación.

## Compatibilidad con estructura de sitio localizada {#localized-site-structure}

Los sitios Web generalmente se proporcionan en varios idiomas para distintas regiones. Generalmente, cada página localizada contendrá un elemento de navega que se incluye como parte de la plantilla de página. El componente de navegación permite colocarlo una vez en una plantilla para todas las páginas del sitio y luego se adaptará automáticamente para las páginas localizadas individuales en función de la estructura globalizada del sitio.

### Ejemplo {#example-localization}

Supongamos que su contenido tiene un aspecto similar al siguiente:

```
/content
+-- we-retail
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

Para el sitio We. Retail, probablemente desee colocar el componente de navegación en una plantilla de página como parte del encabezado. Una vez parte de la plantilla, puede definir la raíz **de navegación** del componente como `/content/we-retail/language-masters/en` desde donde comienza el contenido principal para dicho sitio. Quizás también desee configurar la profundidad de la estructura **de navegación** para que sea `2` porque probablemente no desee que el componente muestre todo el árbol de contenido, sino los dos primeros niveles para que actúe como información general.

Con el valor **Raíz** de navegación, el componente de navegación sabe que después `/content/we-retail/language-masters/en` de que comienza la navegación y puede generar opciones de navegación repitiendo la estructura del sitio dos niveles hacia abajo (tal como se define en el valor **Profundidad** de la estructura de navegación).

Independientemente de la página localizada que esté viendo un usuario, el componente Navegación puede encontrar la página localizada correspondiente conociendo la ubicación de la página actual, avanzando hacia atrás hasta la raíz y luego avanza a la página correspondiente.

Por lo tanto, si un visitante está viendo `/content/ch/de/experience/arctic-surfing-in-lofoten`, el componente sabe generar la estructura de navegación basada `/content/we-retail/language-masters/de`en. Del mismo modo, si el visitante está viendo `/content/us/en/experience/arctic-surfing-in-lofoten`, el componente sabe generar la estructura de navegación basada `/content/we-retail/language-masters/en`en.

## Compatibilidad con estructura del sitio de sombra {#shadow-structure}

A veces es necesario crear un menú de navegación para el visitante diferente de la estructura real del sitio. Tal vez una promoción debe resaltar cierto contenido del menú reorganizando la lista de contenido. Al utilizar páginas de sombra, que simplemente redireccionan a otras páginas de contenido, el componente de navegación puede generar cualquier estructura de navegación arbitraria necesaria.

Para ello necesitará:

1. Cree páginas de sombra como páginas emigry que representen la estructura del sitio que desee. Esto suele conocerse como una estructura de sitio sombreada.
1. Establezca los valores **de Redireccionamiento** en la página divididas en estas páginas para que apunten a las páginas de contenido reales.
1. Establezca **la opción Ocultar en navegación** en las propiedades de página de las páginas de sombra.
1. Defina **el valor Raíz** de navegación del componente de navegación para que apunte a la raíz de la nueva estructura de sitio de sombra.

A continuación, el componente de navegación procesará el menú en función de la estructura del sitio de sombra. Los vínculos representados por el componente son las páginas de contenido real a las que redirecciona las páginas de sombra y no las páginas de sombra. Además, el componente muestra los nombres de las páginas reales y resalta correctamente la página activa, incluso cuando la navegación se basa en páginas de sombra. El componente de navegación hace que las páginas de sombra sean totalmente transparentes para el visitante.

>[!NOTE]
>Las páginas de sombra hacen que las opciones de navegación sean mucho más flexibles, pero tenga en cuenta que la persistencia de esta estructura es por completo manual. Si reorganiza el contenido real del sitio o agrega o elimina contenido, deberá actualizar manualmente la estructura de sombra según sea necesario.

>[!NOTE]
>Cuando se representa una estructura de sitio sombreada, la lógica de navegación sólo recurre a las páginas de sombra. La lógica no recurre a la estructura de los destinos de redirección.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente de navegación es v 1, introducida con la versión 2.0.0 de los componentes principales en enero de 2018, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre versiones y versiones de componentes principales, consulte las [versiones del documento Versiones principales](versions.md).

## Salida de componente de muestra {#sample-component-output}

Para experimentar el componente de navegación, así como ver ejemplos de opciones de configuración, así como HTML y JSON, visite la Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente de navegación [se encuentra en github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Encontrará más información sobre el desarrollo de componentes principales en la documentación del desarrollador de componentes [principales](developing.md).

>[!NOTE]
>
>Desde la versión de componentes principales 2.1.0, el componente de navegación admite [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

En el cuadro de diálogo de edición, el autor de contenido puede definir la página raíz para la navegación y la profundidad de la estructura de navegación.

### Ficha Propiedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.23.45.png)

* **Raíz
de navegación** La página raíz, que se utilizará para generar el árbol de navegación.
* **Excluir raíz
de navegación** Excluir la raíz de navegación en el árbol resultante, incluir solo a sus descendientes.
* **Recopilación de todas las páginas**
secundarias Recopile todas las páginas que sean descendientes de la raíz de navegación.
* **Profundidad
de estructura de navegación** Define cuántos niveles en el árbol de navegación se deben mostrar en relación con la raíz de navegación (solo disponible cuando **no se selecciona la opción Recopilación de todas las páginas** secundarias).

### Ficha Accesibilidad {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.23.53.png)

En la ficha **Accesibilidad** , los valores se pueden definir para [las etiquetas de accesibilidad](https://www.w3.org/WAI/standards-guidelines/aria/) de ARIA para el componente.

* **Etiqueta** : valor de un atributo de etiqueta ARIA para el componente

## Cuadro de diálogo de diseño {#design-dialog}

El cuadro de diálogo de diseño permite que el autor de la plantilla establezca los valores predeterminados para la página raíz de navegación y la profundidad de navegación que se presentan a los autores de contenido.

### Ficha Propiedades {#properties-tab-design}

![](assets/screen_shot_2018-04-03at112357.png)

* **Raíz de navegación El**
valor predeterminado de la página raíz de la estructura de navegación, que se utilizará para generar el árbol de navegación y predeterminado cuando el autor de contenido agrega el componente a la página.
* **Excluir raíz
de navegación** El valor predeterminado de la opción para excluir la raíz de navegación en el árbol resultante.
* **Recopilación de todas las páginas**
secundarias El valor predeterminado de la opción para recopilar todas las páginas que sean descendientes de la raíz de navegación.
* **Profundidad de la estructura de navegación El**
valor predeterminado de la profundidad de la estructura de navegación.

### Ficha Estilos {#styles-tab}

El componente de navegación admite el sistema [de estilos AEM](authoring.md#component-styling).
