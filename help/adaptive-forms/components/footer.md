---
title: 'Componente principal adaptable de Forms: pie de página'
description: Uso o personalización del componente principal del pie de página adaptable de Forms.
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 19%

---


# Pie de página {#footer-adaptive-forms-core-component}

Un componente de pie de página de un formulario adaptable es un área que suele aparecer en la parte inferior del formulario y que contiene información como un aviso de copyright, vínculos a recursos relacionados o información de contacto. Un pie de página puede proporcionar información adicional, como la fecha de la última actualización, que puede ser beneficiosa para los usuarios con necesidades de accesibilidad.

**Ejemplo**

![](/help/adaptive-forms/assets/footer.png)

## Uso {#reasons-to-use-footer}

Existen varias razones por las que resulta beneficioso incluir un componente de pie de página en un formulario, entre ellas:

* **Requisitos legales**: Es posible que se requieran algunos formularios para incluir una renuncia de responsabilidad, un aviso de copyright u otra información legal. Un pie de página es un lugar conveniente para incluir esta información.

* **Navegación**: Un pie de página puede proporcionar vínculos a otras páginas importantes del sitio web, como una política de privacidad, los términos de servicio o la página de contacto.

* **Marcas**: Se puede utilizar un pie de página para incluir un logotipo u otros elementos de marca, lo que ayuda a reforzar la identidad de la organización o sitio web.

* **Coherencia**: Un pie de página proporciona coherencia en el diseño y la presentación del formulario, lo que facilita su navegación e intuición.

* **Contexto adicional**: Un pie de página puede proporcionar contexto adicional al formulario, como un texto que describa el formulario o un vínculo a recursos relacionados, lo que hace que el formulario sea más informativo y fácil de usar.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal del pie de página de Forms adaptable se publicó en febrero de 2023 como parte de los componentes principales 2.0.4. A continuación se muestra una tabla con todas las versiones compatibles, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con<br>[versión 2.0.4](/help/versions.md) y posterior | Compatible | Compatible |

Para obtener información sobre las versiones y versiones de los componentes principales, consulte la [Versiones de componentes principales](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal del pie de página adaptable de Forms en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).


## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del pie de página para los visitantes con el cuadro de diálogo Configurar . También puede definir las opciones de pie de página con facilidad para una experiencia de usuario perfecta.

![Pestaña Propiedades](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Cuadro de diálogo Editar**
El cuadro de diálogo de edición proporciona herramientas de formato de texto enriquecido estándar que permiten al usuario crear texto para el pie de página.

* **Negrita** - Esta opción aplica formato de negrita al texto seleccionado o formato negrita al texto introducido después del cursor. `Ctrl+B` es un atajo de teclado.

* **Cursiva** - Esta opción aplica formato en cursiva al texto seleccionado o texto en cursiva introducido después del cursor. `Ctrl+I` es un atajo de teclado.

![Opciones de viñeta](/help/adaptive-forms/assets/footer_bullet.png)


* **Viñeta**

   * **Icono de viñeta** - Formatea el texto seleccionado como una lista con viñetas o comienza la inserción de una lista con viñetas después del cursor. Para finalizar una lista con viñetas, toque o haga clic en el botón Viñeta de nuevo o introduzca dos retornos de carro.

   * **Icono de lista numerada** - Da formato al texto seleccionado como una lista numerada o comienza la inserción de una lista numerada después del cursor. Para finalizar una lista numerada, toque o haga clic en el botón Numeración de nuevo o introduzca dos retornos de carro.

   * **Icono de anular la selección** - Reduce el nivel de sangría del texto o texto seleccionado tras el cursor. Solo se activará si el texto o la posición seleccionados del cursor ya tienen sangría.

   * **Icono de sangría** - Aumenta el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

![Opciones de hipervínculo](/help/adaptive-forms/assets/footer_link.png)

* **Hipervínculo**

   * **Ruta** - Introduzca la ruta
      1. Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM.
      1. Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta.
      1. Las rutas no absolutas se interpretan como relativas a AEM.
   * **Texto alternativo** - Introduzca un texto descriptivo alternativo para el vínculo.

   * **Target** - Seleccione el comportamiento del vínculo
      * Destino
      * Misma pestaña
      * Nueva pestaña
      * Marco principal
      * Marco superior
   * **Icono Desvincular** - Esta opción elimina un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa si el vínculo ya está seleccionado.

   * **Icono de formato de párrafo** - Esta opción le permite aplicar formato de párrafo al texto seleccionado. También le ayuda a dar formato al texto insertado después del cursor. Define el nivel de encabezado del título.



* **ID**: Esta opción permite controlar el identificador único del componente en el HTML y en la capa de datos.

   * Si se deja en blanco, se genera automáticamente un ID único * y se puede encontrar inspeccionando la página resultante.
   * Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   * Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.


