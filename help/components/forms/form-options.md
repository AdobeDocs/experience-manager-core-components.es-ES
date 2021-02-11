---
title: Componente Opciones de formulario
description: El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 3%

---


# Componente de opciones de formulario {#form-options-component}

El componente Opciones de formulario de componentes principales permite seleccionar opciones predefinidas en diversos formatos.

## Uso {#usage}

El componente Opciones de formulario de componente principal permite enviar diferentes tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el [componente de Contenedor de formulario](form-container.md).

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Opciones de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-options-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte el documento [Versiones de componentes principales](/help/versions.md).

## Salida de componente de muestra {#sample-component-output}

Para obtener información sobre el componente Opciones de formulario y ver ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_options).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la [documentación para desarrolladores de los componentes principales](/help/developing/overview.md).

## Configurar cuadro de diálogo {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![Opciones de formulario Cuadro de diálogo de edición del componente](/help/assets/form-options-edit.png)

* **Tipos** : cómo se presentarán las opciones
   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**
* **Título** : el título que se mostrará como la etiqueta de las opciones
* **Nombre** : el nombre del campo enviado con los datos del formulario
* **Origen** : donde se definen las opciones
   * **Local** : definido dentro del componente
      * Toque o haga clic en el botón **Añadir** para agregar un valor, **Eliminar** para eliminar un valor
         * **Valor** : el valor guardado cuando se selecciona esa opción al enviar el formulario
         * **Texto** : la etiqueta de la opción que se muestra en el formulario
         * **Activo** : la opción se marca como seleccionada cuando se carga el formulario
         * **Deshabilitada** : la opción no se puede seleccionar pero se muestra
   * **Lista** : para las opciones se utiliza una lista estática definida en otra parte de AEM
      * **Lista** : la ruta de la lista estática en AEM
         * Utilice el botón Examinar para localizar el recurso de lista
   * **Fuente**  de datos: se utiliza una fuente de datos para las opciones
      * **Fuente**  de datos: tipo de recurso de la fuente de datos
* **Mensaje**  de ayuda: una sugerencia para el usuario sobre lo que se puede introducir en el campo
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [ de ](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Diálogo de diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Opciones de formulario admite el sistema de estilo AEM [](/help/get-started/authoring.md#component-styling).
