---
title: Componente Opciones de formulario
description: El componente principal Opciones de formulario permite seleccionar entre las opciones predefinidas en distintos formatos.
role: Architect, Developer, Admin, User
exl-id: 8a74bd37-9b12-4fa6-bff2-53e337b16251
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '545'
ht-degree: 100%

---

# Componente Opciones de formulario {#form-options-component}

El componente principal Opciones de formulario permite seleccionar entre las opciones predefinidas en distintos formatos.

## Uso {#usage}

El componente principal Opciones de formulario permite enviar diferentes tipos de opciones presentadas de diferentes maneras y está diseñado para utilizarse junto con el [componente Contenedor de formulario](form-container.md).

El editor de contenido puede definir la presentación de las opciones, etiquetas y opciones individuales en el [cuadro de diálogo de configuración](#configure-dialog).

## Versión y compatibilidad {#version-and-compatibility}

La versión actual del componente Opciones de formulario es la versión 2, que se introdujo con la versión 2.0.0 de los componentes principales en enero de 2018 y se describe en este documento.

La siguiente tabla detalla todas las versiones compatibles del componente, las versiones de AEM con las que son compatibles las versiones del componente y los vínculos a la documentación de versiones anteriores.

| Versión del componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| Versión 2 | Compatible | Compatible | Compatible |
| [Versión 1](/help/components/v1/form-options-v1.md) | Compatible | Compatible | - |

Para obtener más información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Salida del componente de ejemplo {#sample-component-output}

Para experimentar el componente Opciones de formulario, así como ver ejemplos de sus opciones de configuración, así como la salida HTML y JSON, visite la [biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_options_es).

### Detalles técnicos {#technical-details}

La documentación técnica más reciente sobre el componente Opciones de formulario [se encuentra en GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2_es).

Puede encontrar más información sobre el desarrollo de componentes principales en la [documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

El cuadro de diálogo de configuración permite al autor del contenido definir el tipo de opciones que se deben presentar, las etiquetas y las opciones disponibles.

![Cuadro de diálogo de edición del componente Opciones de formulario](/help/assets/form-options-edit.png)

* **Tipos**: presentación de las opciones
   * **Casillas de verificación**
   * **Botones de radio**
   * **Lista desplegable**
   * **Lista desplegable de selección múltiple**
* **Título**: el título que se mostrará como etiqueta para las opciones
* **Nombre**: el nombre del campo, que se envía con los datos del formulario
* **Origen**: donde se definen las opciones
   * **Local**: se define dentro del componente
      * Pulse o haga clic en el botón **Añadir** para añadir un valor y en **Eliminar** para eliminarlo
         * **Valor**: el valor guardado cuando se selecciona esa opción cuando se envía el formulario
         * **Texto**: etiqueta de la opción que se muestra en el formulario.
         * **Activo**: la opción se marca como seleccionada cuando se carga el formulario
         * **Desactivado**: la opción no se puede seleccionar pero se sigue mostrando
   * **Lista**: se utiliza una lista estática definida en otra parte de AEM para las opciones
      * **Lista**: la ruta de la lista estática de AEM
         * Utilice el botón Examinar para localizar el recurso de la lista
   * **Fuente de datos**: se utiliza una fuente de datos para las opciones
      * **Fuente de datos**: tipo de recurso de la fuente de datos
* **Mensaje de ayuda**: una sugerencia al usuario sobre lo que se puede introducir en el campo
* **ID**: esta opción permite controlar el identificador único del componente del HTML y de la [capa de datos](/help/developing/data-layer/overview.md).
   * Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

## Cuadro de diálogo de diseño {#design-dialog}

### Pestaña Estilos {#styles-tab}

El componente Opciones de formulario es compatible con el sistema de estilos de [AEM](/help/get-started/authoring.md#component-styling).
