---
title: 'Componente principal de formularios adaptables: componente de revisión'
description: Uso o personalización del componente principal de revisión de formularios adaptables.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: acd230ed-284b-4df2-98e0-a0090cd73611
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 100%

---


# Revisar componente

El componente de revisión de los formularios adaptables permite a los usuarios revisar y comprobar la información que han introducido antes de enviar el formulario. Sirve como página de resumen, proporcionando una vista de solo lectura de todos los campos y sus valores en un formato estructurado y fácil de usar. Esta función garantiza que los usuarios puedan identificar y corregir cualquier error u omisión antes de finalizar su envío, lo que mejora la experiencia general del formulario. Al hacer clic en el icono de edición, pueden modificar la información introducida antes de enviar el formulario.

{{traditional-aem}}

**Ejemplo**

![Componente de revisión](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Uso

Existen varias razones para utilizar el componente de revisión en un formulario adaptable:

- **Precisión de datos mejorada**: el componente de revisión permite a los usuarios revisar todos los datos que han introducido antes del envío. Ayuda a reducir las posibilidades de errores u omisiones, lo que garantiza que los datos enviados sean precisos.
- **Experiencia del usuario mejorada**: los usuarios obtienen un resumen claro y organizado de toda la información que han rellenado, lo que les da confianza de que el formulario esté completo y sea preciso antes del envío final, lo que se traduce en una mejor experiencia general.
- **Detección y corrección de errores**: proporciona la posibilidad de editar información en el panel o en el nivel de campo, lo que permite a los usuarios corregir errores sin volver a navegar por varias pestañas. Si hace clic en el icono **Editar** junto a un panel o campo, es más fácil volver atrás y solucionar los problemas.
- **Mayor confianza del usuario**: los usuarios pueden revisar los datos introducidos, lo que les garantiza que la información que envían sea correcta, lo que se traduce en menos errores de envío y una mayor confianza en la funcionalidad del formulario.
- **Impedir envíos no intencionados**: los usuarios suelen hacer clic en **Enviar** sin revisar todos los detalles. El componente **Revisar** les ofrece la oportunidad final de comprobar sus datos, lo que reduce la probabilidad de que se produzcan envíos no intencionados.


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de revisión de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia para los visitantes con el cuadro de diálogo de configuración para una experiencia de usuario perfecta. 

![Cuadro de diálogo de configuración](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Ocultar título**: seleccione la opción para ocultar el título del componente.
- **Habilitar acciones del modo de edición para**: las opciones de **Habilitar acciones del modo de edición para** permiten a los usuarios modificar la información escrita. Los usuarios pueden editar la información a nivel de campo o de panel.
   - Cuando los usuarios seleccionan la opción **Campo**, pueden editar campos de formulario individuales durante la revisión.
   - Cuando los usuarios seleccionan la opción **Panel**, pueden editar todos los campos de una sección específica (panel).
   - Cuando los usuarios seleccionan la opción **Campo y panel**, pueden hacer clic en el icono de edición que hay junto a un campo para modificar información específica, o bien junto a un panel para editar todos los campos de ese panel.
   - Cuando los usuarios seleccionan la opción **Ninguno**, pueden editar cualquier campo o panel dentro de todo el formulario.

  La opción **Panel** está seleccionada de forma predeterminada.

- **Paneles de vínculo**: la opción **Paneles de vínculo** permite que los usuarios seleccionen los paneles para su revisión. Cuando los paneles están vinculados, los usuarios pueden revisar la información introducida del panel o paneles seleccionados y modificarla antes del envío.

## Caso de uso

Vea un ejemplo de **Formulario de solicitud de préstamo** que consta de cuatro pestañas, donde cada pestaña recopila información específica sobre el usuario:

- **Datos personales**: recopila los datos personales básicos del usuario, como el nombre, la fecha de nacimiento, la información de contacto y la dirección.

- **Detalles del préstamo**: recopila información relacionada con el préstamo, incluido el tipo de préstamo, el importe deseado, el plazo de amortización y los campos calculados automáticamente como el tipo de interés y la cuota mensual (EMI).

- **Documentos adicionales**: permite al usuario cargar los documentos necesarios, como la prueba de ID, la prueba de la dirección y la revisión de ingresos. También incluye una casilla de verificación de declaración para confirmar el acuerdo con los términos.

- **Revisar y enviar formulario**: incluye un componente de revisión que resume todas las entradas de las pestañas anteriores. Los usuarios pueden comprobar y editar sus datos antes de enviar el formulario. Esta pestaña también incluye el botón **Enviar** para enviar la solicitud.

En el siguiente vídeo se muestra cómo configurar el componente **Revisar** para que proporcione al usuario la posibilidad de editar información:

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
