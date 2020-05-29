---
title: Componente Opciones de formulario
description: El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 4%

---


# Componente Opciones de formulario {#form-options-component}

El componente de opciones de formulario de componente principal permite seleccionar opciones predefinidas en diversos formatos.

## Uso {#usage}

El componente Opciones de formulario de componente principal permite enviar distintos tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el componente [Contenedor de](form-container.md)formulario.

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el cuadro de diálogo [de](#configure-dialog)configuración.

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Opciones de formulario es v2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

En la tabla siguiente se detallan todas las versiones compatibles del componente, las versiones de AEM con las que las versiones del componente son compatibles y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.3 | AEM 6.4   | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatible | Compatible | Compatible |
| [v1](/help/components/v1/form-options-v1.md) | Compatible | Compatible | Compatible | - |

Para obtener más información sobre las versiones y versiones de los componentes principales, consulte las Versiones [de los componentes](/help/versions.md)principales de documento.

## Ejemplo de salida de componente {#sample-component-output}

Para obtener información sobre el componente Opciones de formulario, así como ejemplos de sus opciones de configuración, así como sobre la salida HTML y JSON, visite la biblioteca [de](https://adobe.com/go/aem_cmp_library_form_options)componentes.

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [puede encontrarse en GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Encontrará más detalles sobre el desarrollo de los componentes principales en la documentación [para desarrolladores de los componentes](/help/developing/overview.md)principales.

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
      * Toque o haga clic en el botón **Añadir** para agregar un valor, **Eliminar** para eliminarlo
         * **Valor** : el valor guardado cuando se selecciona esa opción al enviar el formulario
         * **Texto** : la etiqueta de la opción que se muestra en el formulario
         * **Activo** : la opción se marca como seleccionada cuando se carga el formulario
         * **Deshabilitada** : la opción no se puede seleccionar pero se muestra
   * **Lista** : se utiliza una lista estática definida en otra parte de AEM para las opciones
      * **Lista** : la ruta de la lista estática en AEM
         * Utilice el botón Examinar para localizar el recurso de lista
   * **Fuente** de datos: se utiliza una fuente de datos para las opciones
      * **Fuente** de datos: tipo de recurso de la fuente de datos
* **Mensaje** de ayuda: una sugerencia para el usuario sobre lo que se puede introducir en el campo
* **ID** : Esta opción permite controlar el identificador único del componente en el HTML y en la capa [de](/help/developing/data-layer/overview.md)datos.
   * Si se deja en blanco, se genera automáticamente una ID única para usted y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede tener un impacto en el seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo Diseño {#design-dialog}

### Ficha Estilos {#styles-tab}

El componente Opciones de formulario admite el sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
