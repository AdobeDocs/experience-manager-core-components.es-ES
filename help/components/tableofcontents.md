---
title: Componente Tabla de contenido
description: El componente Tabla de contenido crea una TDC basada en los títulos del contenido de la página, lo que permite a los lectores navegar rápidamente por ella.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 394a8b968d7bcde7e766ed719c5914ec5cb60744
workflow-type: ht
source-wordcount: '759'
ht-degree: 100%

---

# Componente Tabla de contenido {#table-of-contents-component}

El componente Tabla de contenido crea una TDC basada en los títulos del contenido de la página, lo que permite a los lectores navegar rápidamente por ella.

## Uso {#usage}

El componente Tabla de contenido ofrece a los visitantes del sitio la capacidad de navegar rápidamente por el contenido de la página a través de una TDC generada de forma eficiente en función de los títulos del contenido de las páginas.

* La TDC se genera en el servidor.
* Dispatcher la almacena completamente en caché para una entrega rápida.
* Funciona con todos los componentes de la página, no solo con los componentes principales.

El [cuadro de diálogo de edición](#edit-dialog) permite al autor del contenido definir los intervalos de títulos que se usan en la TDC. Al usar el [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede establecer el valor predeterminado para los títulos cuando un autor de contenido añade un componente Tabla de contenido a una página, así como restringir los títulos incluidos en la TDC en función de los nombres de clase.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Tabla de contenido es la 1, que se introdujo con la versión 2.20.0 de los componentes principales en mayo de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para descubrir el componente Tabla de contenido, así como ver ejemplos de sus opciones de configuración, además de la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente acerca del componente Tabla de contenido [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir los intervalos de niveles de título que el componente Tabla de contenido debe representar como una TDC.

![Cuadro de diálogo de edición del componente Tabla de contenido](/help/assets/tableofcontents-edit.png)

**Tipo de lista**: esta opción define si la lista debe ser una lista con viñetas o numerada.
* **Nivel inicial del título**: esta opción define el nivel más alto de títulos que debe representar el componente Tabla de contenido.
* **Nivel de detención de título**: esta opción define el nivel más bajo de títulos que debe representar el componente Tabla de contenido.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el rango de título del componente Tabla de contenido, así como restringir los títulos incluidos en la TDC en función de los nombres de clase.

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente Búsqueda rápida](/help/assets/tableofcontents-design.png)

* **Restringir tipo de lista**: esta opción define el tipo de lista que generará el componente. Al seleccionar esta opción, se restringe la capacidad del autor de contenido para elegir un tipo de lista diferente.
* **Restringir el nivel de inicio**: esta opción define el nivel de título más alto que el autor de contenido puede seleccionar para definir la TDC.
* **Restringir el nivel de detención**: esta opción define el nivel de título más bajo que el autor de contenido puede seleccionar para definir la TDC.
* **Incluir nombres de clase**: si esta opción está definida, el componente Tabla de contenido solo considerará los títulos con los nombres de clase especificados o contenidos dentro de elementos de los nombres de clase especificados.
   * Toque o haga clic en el icono **Añadir** para añadir uno o más nombres de clase.
   * Toque o haga clic en el botón **Eliminar** junto al nombre de una clase para eliminarla.
* **Omitir nombres de clase**: si se define esta opción, el componente Tabla de contenido ignorará los títulos con los nombres de clase especificados o contenidos dentro de elementos de los nombres de clase especificados.
   * Toque o haga clic en el botón **Añadir** para añadir uno o más nombres de clase.
   * Toque o haga clic en el botón **Eliminar** junto al nombre de una clase para eliminarla.

### Pestaña Estilos {#styles-tab}

El componente Tabla de contenido es compatible con el [Sistema de estilos](/help/get-started/authoring.md#component-styling) de AEM.

## Capa de datos del cliente de Adobe {#data-layer}

El componente Tabla de contenido es compatible con la [Capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
