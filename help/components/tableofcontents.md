---
title: Componente Tabla de contenido
description: El componente Tabla de contenido crea un ToC basado en los títulos del contenido de la página, lo que permite a los lectores navegar rápidamente por la página.
role: Architect, Developer, Admin, User
source-git-commit: 52c63ecb014e5d4fda4d166d92e8efb3163633ba
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 23%

---

# Componente Tabla de contenido {#table-of-contents-component}

El componente Tabla de contenido crea un ToC basado en los títulos del contenido de la página, lo que permite a los lectores navegar rápidamente por la página.

## Uso {#usage}

El componente Tabla de contenido ofrece a los visitantes del sitio la capacidad de navegar rápidamente por el contenido de la página a través de una tabla de contenido generada en función de los títulos del contenido de las páginas.

La variable [cuadro de diálogo editar](#edit-dialog) permite al autor del contenido definir el rango de títulos que se van a utilizar en el ToC. Al usar la variable [cuadro de diálogo de diseño](#design-dialog), el autor de la plantilla puede establecer el valor predeterminado para los títulos cuando un autor de contenido agrega un componente de tabla de contenido a una página, así como restringir los títulos incluidos en el objeto ToC en función de los nombres de clase.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Tabla de contenido es v1, que se introdujo con la versión 2.20.0 de los componentes principales en mayo de 2022 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| Versión 1 | Compatible | Compatible |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Tabla de contenido, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_tableofcontents).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Tabla de contenido [se puede encontrar en GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de edición {#edit-dialog}

El cuadro de diálogo de edición permite al autor del contenido definir los intervalos de niveles de título que el componente Tabla de contenido debe representar como un ToC.

![Cuadro de diálogo de edición del componente Tabla de contenido](/help/assets/tableofcontents-edit.png)

**Tipo de lista** - Esta opción define si la lista debe ser una lista con viñetas o una lista numerada.
* **Nivel inicial del título** - Esta opción define el nivel más alto de títulos que debe representar el componente Tabla de contenido.
* **Nivel de parada del título** - Esta opción define el nivel más bajo de títulos que debe representar el componente Tabla de contenido.
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

Con el cuadro de diálogo de diseño, el autor de la plantilla puede establecer el valor predeterminado para el rango de título del componente Tabla de contenido, así como restringir los títulos incluidos en el objeto AC en función de los nombres de clase.

### Pestaña Propiedades {#properties-tab}

![Cuadro de diálogo de diseño del componente Búsqueda rápida](/help/assets/tableofcontents-design.png)

* **Restringir tipo de lista** - Esta opción define el tipo de lista que generará el componente. Al seleccionar esta opción, se restringe la capacidad del autor de contenido para elegir un tipo de lista diferente.
* **Restringir el nivel inicial** - Esta opción define el nivel de título más alto que el autor de contenido puede seleccionar para definir el ToC.
* **Restricción del nivel de detención** - Esta opción define el nivel de título más bajo que el autor de contenido puede seleccionar para definir el ToC.
* **Incluir nombres de clase** - Si esta opción está establecida, el componente Tabla de contenido solo considerará los títulos con los nombres de clase especificados o contenidos dentro de elementos de los nombres de clase especificados.
   * Toque o haga clic en el botón **Agregar** para agregar uno o más nombres de clase.
   * Toque o haga clic en el botón **Eliminar** junto al nombre de una clase para eliminarla.
* **Ignorar nombres de clase** - Si se establece esta opción, el componente Tabla de contenido ignorará los títulos con los nombres de clase especificados o contenidos dentro de elementos de los nombres de clase especificados.
   * Toque o haga clic en el botón **Agregar** para agregar uno o más nombres de clase.
   * Toque o haga clic en el botón **Eliminar** junto al nombre de una clase para eliminarla.

### Pestaña Estilos {#styles-tab}

El componente Tabla de contenido es compatible con la AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Capa de datos del cliente de Adobe {#data-layer}

El componente Tabla de contenido es compatible con la variable [Capa de datos del cliente de Adobe.](/help/developing/data-layer/overview.md)
