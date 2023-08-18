---
title: 'Componente principal de formularios adaptables: contenedor de formulario'
description: Agregue un formulario adaptable a una página web.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 8db061f3d6f1041336c379b34f3b6b7f03083560
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 54%

---


# Google reCAPTCHA {#google-recaptcha}

CAPTCHA (prueba de Turing completamente automática y pública para diferenciar ordenadores de humanos) es un programa que se utiliza comúnmente en transacciones en línea para distinguir entre humanos y programas o bots automatizados. Plantea un desafío y evalúa la respuesta del usuario para determinar si es un humano o un bot que interactúa con el sitio. Evita que el usuario continúe si la prueba falla y ayuda a que las transacciones en línea sean seguras al impedir que los bots publiquen contenido no deseado o con fines malintencionados.

AEM Forms as a Cloud Service es compatible con Google reCAPTCHA v2 en Forms adaptable. Puede utilizarlo para presentar un desafío CAPTCHA al enviar el formulario

## Uso {#reasons-to-use-google-recaptcha}


- **Prevención de spam y bots**: una de las principales razones para utilizar reCAPTCHA es evitar que los envíos de correo no deseado y los bots maliciosos inunden el formulario. Los algoritmos avanzados de reCAPTCHA pueden detectar intentos automatizados de enviar el formulario, lo que garantiza que solo los usuarios legítimos puedan interactuar con él.

- **Seguridad mejorada**: Al implementar reCAPTCHA, agrega una capa adicional de seguridad al formulario adaptable. Esto ayuda a proteger la información confidencial y a evitar que los usuarios malintencionados exploten las vulnerabilidades.

- **Experiencia del usuario**: Aunque los CAPTCHA a veces se pueden ver como un inconveniente, el enfoque adaptativo de reCAPTCHA significa que a la mayoría de los usuarios se les presenta una experiencia optimizada y fácil de usar que requiere una interacción mínima. Esto puede ayudar a mantener una experiencia de usuario positiva y, al mismo tiempo, disuadir a los bots.

- **Adaptabilidad**: el mecanismo adaptable de reCAPTCHA analiza el comportamiento y las interacciones del usuario para determinar si son humanas o no. Esto significa que el nivel de desafío presentado al usuario puede variar en función de la probabilidad de que sea un bot. Esta adaptabilidad reduce la fricción para los usuarios genuinos y, al mismo tiempo, mantiene una sólida seguridad.

- **Moderación manual reducida**: Al reducir significativamente el número de envíos de correo no deseado y el contenido generado por bots, reCAPTCHA puede ahorrar tiempo y recursos que, de lo contrario, se gastarían en moderación manual y limpieza.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal reCAPTCHA de Forms Google adaptable se lanzó en agosto de 2023 como parte de la &quot;versión&quot; de los componentes principales. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:

|  |  |
|---|---|
| Versión del componente | AEM as a Cloud Service |
| --- | --- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/versions.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente sobre el componente principal reCAPTCHA de Forms Google adaptable en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente su experiencia de Google reCAPTCHA para los visitantes con el Cuadro de diálogo de configuración. También puede definir las opciones de reCAPTCHA de Google con facilidad para una experiencia de usuario perfecta.

### Pestaña Básicos {#basic-tab}

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Ocultar título**: seleccione la opción para ocultar el título del componente.

- **Configuración** -

- **Tipo** -

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. Los datos del componente deshabilitado no se envían. El usuario puede ver el valor del campo, pero no puede modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Validación {#validation-tab}

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

