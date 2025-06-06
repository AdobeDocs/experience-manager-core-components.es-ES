---
title: 'Componente principal de Forms adaptable: componente de revisión'
description: Usar o personalizar el componente principal de revisión de Forms adaptable.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 14%

---


# Revisar componente

El componente Revisar en Forms adaptable permite a los usuarios revisar y comprobar la información que han introducido antes de enviar el formulario. Sirve como página de resumen, que proporciona una vista de solo lectura de todos los campos y sus valores en un formato estructurado y fácil de usar. Esta función garantiza que los usuarios puedan identificar y corregir cualquier error u omisión antes de finalizar su envío, lo que mejora la experiencia general del formulario. Al hacer clic en el icono de edición, pueden modificar la información introducida antes del envío del formulario.

**Ejemplo**

![Componente de revisión](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Uso

A continuación se indican las razones para utilizar el componente Revisar en un formulario adaptable:

- **Precisión de datos mejorada**: el componente Revisar permite a los usuarios revisar todos los datos que han introducido antes del envío. Ayuda a reducir las posibilidades de errores u omisiones, lo que garantiza que los datos enviados sean precisos.
- **Experiencia del usuario mejorada**: Los usuarios obtienen un resumen claro y organizado de toda la información que han rellenado, lo que les da confianza de que el formulario está completo y es preciso antes del envío final, lo que mejora la experiencia general.
- **Detección y corrección de errores**: Proporciona la capacidad de editar información en el panel o en el nivel de campo, lo que permite a los usuarios corregir errores sin volver a navegar por varias pestañas. Si hace clic en el icono **Editar** junto a un panel o campo, es más fácil volver atrás y solucionar los problemas.
- **Mayor confianza del usuario**: los usuarios pueden revisar los datos introducidos, asegurándoles que la información que envían es correcta, lo que reduce los errores de envío y genera una mayor confianza en la funcionalidad del formulario.
- **Impedir envíos no intencionados**: Los usuarios suelen hacer clic en **Enviar** sin revisar todos los detalles. El componente **Revisar** les ofrece la oportunidad final de comprobar sus datos, lo que reduce la probabilidad de que se produzcan envíos no intencionados.


## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal de revisión de Forms adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Para obtener más información sobre el desarrollo de los componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de los visitantes con el Cuadro de diálogo de configuración para una experiencia de usuario perfecta.

![Cuadro De Diálogo De Configuración](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.
- **Ocultar título**: seleccione la opción para ocultar el título del componente.
- **Habilitar acciones del modo de edición para**: las opciones **Habilitar acciones del modo de edición para** permiten a los usuarios modificar la información escrita. Los usuarios pueden editar la información en el nivel de campo o de panel.
   - Cuando los usuarios seleccionan la opción **Campo**, pueden editar campos de formulario individuales durante la revisión.
   - Cuando los usuarios seleccionan la opción **Panel**, pueden editar todos los campos de una sección específica (panel).
   - Cuando los usuarios seleccionan la opción **Campo y panel**, pueden hacer clic en el icono de edición que hay junto a un campo para modificar información específica, o bien junto a un panel para editar todos los campos de ese panel.
   - Cuando los usuarios seleccionan la opción **Ninguno**, pueden editar cualquier campo o panel dentro de todo el formulario.

  De manera predeterminada, la opción **Panel** está seleccionada.

- **Paneles de vínculo** - La opción **Paneles de vínculo** permite que los usuarios seleccionen los paneles para su revisión. Cuando los paneles están vinculados, los usuarios pueden revisar la información introducida de los paneles seleccionados y modificarla antes del envío.

## Caso de uso

Vea un ejemplo de un **Formulario de solicitud de préstamo** que consta de cuatro fichas, donde cada ficha recopila información específica acerca del usuario:

- **Datos personales**: recopila los datos personales básicos del usuario, como el nombre, la fecha de nacimiento, la información de contacto y la dirección.

- **Detalles del préstamo**: Recopila información relacionada con el préstamo, incluido el tipo de préstamo, el importe deseado, el período de reembolso y los campos calculados automáticamente como tasa de interés y EMI mensual.

- **Documentos adicionales**: permite al usuario cargar los documentos necesarios, como la revisión de ID, la revisión de direcciones y la revisión de ingresos. También incluye una casilla de verificación de declaración para confirmar el acuerdo con los términos.

- **Revisar y enviar formulario**: Incluye un componente Revisar que resume todas las entradas de las pestañas anteriores. Los usuarios pueden comprobar y editar sus datos antes de enviar el formulario. Esta pestaña también incluye el botón **Enviar** para enviar la solicitud.

El siguiente vídeo muestra cómo configurar el componente **Review** para que proporcione al usuario la flexibilidad de editar información:

## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}

