---
title: Componente de contenedor
seo-title: Componente de contenedor
description: nulo
seo-description: El componente Contenedor de componentes principales permite la creación de un contenedor para varios componentes adicionales en una página.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: Usuario
content-type: referencia
topic-tags: creación
products: SG_EXPERIENCEMANAGER/CORECOMPONENTES-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# Componente de contenedor{#container-component}

El componente Contenedor de componentes principales permite la creación de un contenedor para varios componentes adicionales en una página.

## Uso {#usage}

El componente Contenedor de componentes principales permite la creación de un contenedor para varios componentes adicionales en una página y se puede utilizar para agrupar otros componentes y aplicar un estilo o diseño común.

* Las propiedades del contenedor se pueden seleccionar en el cuadro de diálogo [](#configure-dialog)configurar.
* Los valores predeterminados del componente Contenedor al agregarlo a una página se pueden definir en el cuadro de diálogo [de](#design-dialog)diseño.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Contenedor es v1, que se introdujo con la versión 2.5.0 de los componentes principales en junio de 2019, y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatible | Compatible | Compatible |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento Versiones [de componentes](versions.md)principales.

## Ejemplo de salida de componente {#sample-component-output}

Para experimentar el componente Contenedor y ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/container.html)componentes.

## Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Contenedor [puede encontrarse en GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](developing.md)principales.

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el elemento de contenedor y cómo se comportará y aparecerá para un visitante de la página.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **Diseño** : esta opción define el comportamiento o el comportamiento de diseño del componente contenedor.
   * **Simple** : define un contenedor como una simple colección de componentes
   * **Cuadrícula** adaptable: define un contenedor como una cuadrícula adaptable a [AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** : utilice esta opción para definir el atributo de ID HTML que se aplicará al componente.
* **Color** de fondo: se puede definir como valores RGB de forma libre o mediante el selector de color, [según la configuración](#background-tab)
* **Imagen** de fondo: define un color de fondo para el contenedor, [según la configuración](#background-tab)

## Cuadro de diálogo Diseño {#design-dialog}

El cuadro de diálogo de diseño permite al autor de la plantilla definir las opciones disponibles para el autor del contenido que utiliza el componente Contenedor.

### Ficha Componentes permitidos {#allowed-components-tab}

La ficha Componentes **** permitidos se utiliza para definir qué componentes puede agregar el autor del contenido como elementos al componente contenedor.

La ficha Componentes permitidos funciona del mismo modo que la ficha del mismo nombre al [definir la política y las propiedades de un contenedor de diseño en el Editor de plantillas.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Ficha Componentes predeterminados {#default-components-tab}

La ficha Componentes predeterminados se utiliza para definir qué componente se agrega al componente cuando se coloca un tipo de recurso determinado en el contenedor, de forma similar a [cómo se definen los componentes predeterminados en la plantilla](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors)de página.

### Ficha Configuración adaptable {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **Columnas** : define el número de columnas en la cuadrícula del contenedor resultante.

### Ficha Fondo {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **Imagen de fondo**
   * **Activar imagen** de fondo: seleccione esta opción para permitir que el autor del contenido defina una imagen de fondo para el contenedor.
* **Color de fondo**
   * **Activar color** de fondo: seleccione esta opción para permitir que el autor del contenido defina un color de fondo para el contenedor.
   * **Solo** muestras: seleccione esta opción para permitir que el autor del contenido seleccione solo muestras de color predefinidas para el color de fondo del contenedor.
      * Solo está disponible cuando se selecciona **Activar color** de fondo
* **Muestras** permitidas: defina los colores predefinidos desde los que el autor del contenido puede seleccionar el color de fondo del contenedor
   * Utilice el botón **Agregar** para agregar una muestra de color predefinida. Una vez agregada, se agrega una entrada a la lista, que contiene las siguientes columnas:
   * **Valor** : defina el color manualmente mediante valores RGB
      * Toque o haga clic en el selector de color para seleccionar un color más fácilmente ajustando valores RGB individuales o definiendo un valor hexadecimal.
   * **Eliminar** : toque o haga clic para eliminar una muestra.
   * **Reorganizar** : toque o haga clic y arrastre para reorganizar el orden de las muestras.

### Ficha Estilos {#styles-tab}

El componente Contenedor es compatible con el sistema [de](authoring.md#component-styling)estilo AEM.
