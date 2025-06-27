---
title: 'Componente principal de formularios adaptables: pie de página'
description: Uso o personalización del componente principal de pie de página de formularios adaptables.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '767'
ht-degree: 100%

---


# Pie de página {#footer-adaptive-forms-core-component}

Un componente de pie de página de un formulario adaptable es un área que suele aparecer en la parte inferior del formulario y que contiene información como un aviso de copyright, vínculos a recursos relacionados o información de contacto. Un pie de página puede proporcionar información adicional, como la fecha de la última actualización, que puede ser beneficiosa para los usuarios con necesidades de accesibilidad.

{{traditional-aem}}

**Ejemplo**

![ejemplo](/help/adaptive-forms/assets/footer.png)

## Uso {#reasons-to-use-footer}

Existen varias razones por las que resulta beneficioso incluir un componente de pie de página en un formulario, entre ellas, las siguientes:

- **Requisitos legales**: es posible que se requieran algunos formularios para incluir una exención de responsabilidad, un aviso de copyright u otra información legal. Un pie de página es el lugar idóneo para incluir esta información.

- **Navegación**: un pie de página puede proporcionar vínculos a otras páginas importantes del sitio web, como una política de privacidad, los términos de servicio o la página de contacto.

- **Personalización de marca**: se puede utilizar un pie de página para incluir un logotipo u otros elementos de personalización de marca, lo que ayuda a reforzar la identidad de la organización o del sitio web.

- **Coherencia**: un pie de página proporciona coherencia en el diseño y la presentación del formulario, lo que lo hace más intuitivo y fácil de navegar para los usuarios.

- **Contexto adicional**: un pie de página puede proporcionar contexto adicional al formulario, como un texto que describe el formulario o un vínculo a recursos relacionados, lo que hace que el formulario sea más informativo y fácil de usar.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal Pie de página de los formularios adaptables se publicó en febrero de 2023 como parte de los componentes principales, versión 2.0.4 para Cloud Service y los componentes principales, versión 1.1.12 para AEM 6.5.16.0 Forms o versiones posteriores. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

| Versión del componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms o versiones posteriores |
|---|---|---|
| v1 | Compatible con la <br>[versión 2.0.4](/help/adaptive-forms/version.md) y posteriores | Compatible con la<br>[versión 1.1.12](/help/adaptive-forms/version.md) y posteriores, pero inferiores a 2.0.0. |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de pie de página de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).


## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia del pie de página para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de pie de página con facilidad para que la experiencia del usuario sea óptima.

![Pestaña Propiedades](/help/adaptive-forms/assets/footer_propertiestab.png)

- **Cuadro de diálogo Editar**
El cuadro de diálogo de edición proporciona herramientas de formato de texto enriquecido estándar que permiten al usuario crear texto para el pie de página.

- **Negrita**: se utiliza para aplicar formato de negrita al texto seleccionado o para dar formato negrita al texto introducido después del cursor. `Ctrl+B` es un método abreviado del teclado.

- **Cursiva**: esta opción aplica formato en cursiva al texto seleccionado o texto en cursiva introducido después del cursor. `Ctrl+I` es un método abreviado del teclado.

![Opciones de viñeta](/help/adaptive-forms/assets/footer_bullet.png)


- **Viñeta**

   - **Icono de viñeta**: se utiliza para dar formato al texto seleccionado como una lista con viñetas o comenzar la inserción de una lista con viñetas después del cursor. Para finalizar una lista con viñetas, toque o haga clic en el botón Viñeta de nuevo o introduzca dos retornos de carro.

   - **Icono de lista numerada**: se utiliza para dar formato al texto seleccionado como una lista numerada o comenzar la inserción de una lista numerada después del cursor. Para finalizar una lista numerada, toque o haga clic en el botón Numeración de nuevo o introduzca dos retornos de carro.

   - **Icono de anular selección**: reduce el nivel de sangría del texto o texto seleccionado tras el cursor. Solo se activará si el texto o la posición seleccionados del cursor ya tienen sangría.

   - **Icono de sangría**: aumenta el nivel de sangría del texto seleccionado o del texto introducido después del cursor.

![Opciones de hipervínculo](/help/adaptive-forms/assets/footer_link.png)

- **Hipervínculo**

   - **Ruta**: introduzca la ruta
      1. Utilice el cuadro de diálogo Abrir selección para elegir una ruta en AEM.
      1. Si el vínculo no está dentro de AEM, introduzca la dirección URL absoluta.
      1. Las rutas no absolutas se interpretan como relativas a AEM.

   - **Texto alternativo**: escriba un texto descriptivo alternativo para el vínculo.

   - **Público objettivo**: seleccione el comportamiento del vínculo
      - Destino
      - Misma pestaña
      - Nueva pestaña
      - Marco principal
      - Marco superior

   - **Icono Desvincular**: esta opción elimina un vínculo ya aplicado al texto seleccionado. Esta opción solo está activa cuando ya se ha seleccionado el vínculo.

   - **Icono de formato de párrafo**: esta opción le permite aplicar formato de párrafo al texto seleccionado. También le ayuda a dar formato al texto insertado después del cursor. Define el nivel de encabezado del título.

- **ID**: esta opción permite controlar el identificador único del componente en el HTML y en la capa de datos.

   - Si se deja en blanco, se generará automáticamente un ID único que se puede encontrar examinando la página resultante.
   - Si se especifica un ID, es responsabilidad del autor asegurarse de que sea único.
   - Cambiar el ID puede afectar al seguimiento de CSS, JS y de la capa de datos.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
