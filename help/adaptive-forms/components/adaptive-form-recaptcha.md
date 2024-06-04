---
title: 'Componente principal de Forms adaptable: Google reCAPTCHA'
description: Mejore la seguridad de los formularios con el servicio reCAPTCHA de Google sin esfuerzo con AEM Forms. Explicar las propiedades del formulario adaptable reCaptcha
role: Architect, Developer, Admin, User
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 82%

---


# reCAPTCHA de formulario adaptable {#google-recaptcha}

CAPTCHA (prueba de Turing completamente automática y pública para diferenciar ordenadores de humanos) es un programa que se utiliza comúnmente en transacciones en línea para distinguir entre humanos y programas o bots automatizados. Plantea un desafío y evalúa la respuesta del usuario para determinar si es un humano o un bot que interactúa con el sitio. Evita que el usuario continúe si la prueba falla y ayuda a que las transacciones en línea sean seguras al impedir que los bots publiquen contenido no deseado o con fines malintencionados.

AEM Forms as a Cloud Service es compatible con Google reCAPTCHA v2 en los formularios adaptables. Puede utilizarlo para presentar un desafío de CAPTCHA en el envío de formularios

## Uso {#reasons-to-use-google-recaptcha}


- **Prevención de spam y bots**: una de las principales razones para utilizar reCAPTCHA es evitar que el spam y los bots maliciosos inunden el formulario. Los algoritmos avanzados de reCAPTCHA pueden detectar intentos automatizados de enviar el formulario, garantizando de este modo que solo los usuarios legítimos puedan interactuar con él.

- **Seguridad mejorada**: al implementar reCAPTCHA, añade una capa adicional de seguridad a su formulario adaptable. Esto contribuye a proteger la información confidencial y a evitar que usuarios malintencionados exploten las vulnerabilidades.

- **Experiencia del usuario**: aunque a veces los CAPTCHA se perciben como un inconveniente, el enfoque adaptativo de reCAPTCHA hace que la mayoría de los usuarios disfruten de una experiencia sencilla y fácil de utilizar que requiere una interacción mínima. Esto puede ayudar a mantener una experiencia del usuario positiva. Al mismo tiempo, disuade a los bots.

- **Adaptabilidad**: el mecanismo adaptativo de reCAPTCHA analiza el comportamiento y las interacciones de los usuarios para determinar si son humanos o no. Esto quiere decir que el nivel de desafío presentado al usuario puede variar en función de la probabilidad de que sea un bot. Esta adaptabilidad reduce la complejidad para los usuarios reales y, al mismo tiempo, mantiene un alto nivel de seguridad.

- **Moderación manual reducida**: al reducir significativamente el número de envíos de spam y contenidos generados por bots, reCAPTCHA puede ahorrar tiempo y recursos que, de otro modo, se dedicarían a la moderación y limpieza manuales.

## Versión y compatibilidad {#version-and-compatibility}

El componente principal de reCAPTCHA de Google para formularios adaptables se publicó en agosto de 2023 como parte de la “versión” de los componentes principales. A continuación se muestra una tabla con todas las versiones admitidas, la compatibilidad con AEM y los vínculos a la documentación correspondiente:


| Versión del componente | AEM as a Cloud Service |
|--- |--- |
| Versión 1 | Compatible con la <br>[versión 2.0.4](/help/versions.md) y posteriores | Compatible | Compatible |

Para obtener información sobre las versiones y publicaciones de los componentes principales, consulte el documento [Versiones de los componentes principales](/help/versions.md).

## Detalles técnicos {#technical-details}

Obtenga la información más reciente acerca del componente principal reCAPTCHA de Google de formularios adaptables en la documentación técnica de [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Para obtener más información sobre el desarrollo de componentes principales, consulte la [Documentación para desarrolladores de componentes principales](/help/developing/overview.md).

## Cuadro de diálogo de configuración {#configure-dialog}

Puede personalizar fácilmente la experiencia de reCAPTCHA de Google para los visitantes con el cuadro de diálogo de configuración. También puede definir las opciones de reCAPTCHA de Google con facilidad para una experiencia del usuario perfecta.

### Pestaña Básicos {#basic-tab}

![Pestaña Básicos](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Nombre**: puede identificar fácilmente un componente de formulario con su nombre único tanto en el formulario como en el editor de reglas, pero el nombre no debe contener espacios ni caracteres especiales.

- **Título**: con su título, puede identificar fácilmente un componente en un formulario y, de forma predeterminada, el título aparece sobre el componente. Si no agrega un título, se mostrará el nombre del componente en lugar del texto del título.

- **Permitir texto enriquecido en el título**: esta función permite a los usuarios dar formato a los títulos de texto sin formato, incorporando funciones como negrita, cursiva, texto subrayado, varias fuentes, tamaños de fuente, colores y opciones adicionales para mejorar la presentación visual y la personalización. Ofrece una mayor flexibilidad y control creativo para hacer que los títulos destaquen dentro de los documentos, sitios web o aplicaciones.\
  Al seleccionar la casilla de verificación **Permitir texto enriquecido para el título, las opciones de formato se vuelven visibles para aplicar estilo al título del componente. Para acceder a todas las opciones de formato disponibles, puede hacer clic en la pestaña ![Icono de pantalla completa](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Compatibilidad del texto enriquecido](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: seleccione la opción para ocultar el título del componente.
- **Marcar como elemento de formulario independiente**: seleccione la opción para configurar un campo de formulario no vinculado a ningún esquema. Esta opción le permite guardar datos sin actualizar la fuente de datos. También le permite gestionar los datos de forma personalizada, independientemente de la integración de bases de datos estándar.
- **Ajustes de configuración**: seleccione el contenedor de configuración que contiene la configuración de nube que conecta AEM Forms con el servicio reCAPTCHA de Google.

  >[!NOTE]
  >
  > Consulte la [Usar Google AEM reCAPTCHA en un formulario adaptable de forma basado en componentes principales](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) para aprender a crear y configurar Google reCAPTCHA para su entorno.

- **Tipo**: elija esta opción para seleccionar el tamaño de reCAPTCHA.
   - **Normal**: Se refiere a la versión estándar y más grande del widget reCAPTCHA, que puede ser más visible y fácil de interactuar para los usuarios, especialmente en dispositivos con pantallas más grandes.
   - **Compacto**: Se refiere a una versión más pequeña del widget reCAPTCHA. Esta opción es adecuada para situaciones en las que el espacio es limitado, como en dispositivos móviles o en diseños ajustados en páginas web.

- **Ocultar componente**: seleccione la opción para ocultar el componente del formulario. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas. Esto resulta útil cuando necesita almacenar información que el usuario no necesita ver o cambiar directamente.

- **Deshabilitar componente**: seleccione la opción para desactivar el componente. El componente desactivado no está activo ni puede editarlo el usuario final. Los datos del componente desactivado no se envían. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

- **Solo lectura**: seleccione la opción para que el componente no se pueda editar. El usuario puede ver el valor del campo, pero no modificarlo. El componente permanece accesible para otros fines, como utilizarlo para los cálculos en el Editor de reglas.

### Pestaña Validación {#validation-tab}

![Pestaña Validación](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Mensaje de error**: esta opción le permite introducir un mensaje que se muestra si la casilla de verificación **Obligatorio** está activada y el campo de formulario se deja en blanco.

- **Mensaje de validación de secuencia de comandos**: esta opción le permite introducir un mensaje que se mostrará si la validación de la secuencia de comandos falla.

## Cuadro de diálogo de diseño {#design-dialog}

Cuadro de diálogo de diseño se utiliza para definir y administrar estilos CSS para el componente reCAPTCHA.

### Pestaña Estilos {#styles-design-tab}

El componente principal de reCAPTCHA de Forms AEM adaptable es compatible con la función de [Sistema de estilos](/help/get-started/authoring.md#component-styling).

![Cuadro de diálogo de diseño](/help/adaptive-forms/assets/checkbox-style.png)

- **Clases CSS predeterminadas**: puede proporcionar una clase CSS predeterminada para el componente principal reCAPTCHA de Forms adaptable.

- **Estilos permitidos**: puede definir estilos proporcionando un nombre y la clase CSS que representa el estilo. Por ejemplo, puede crear un estilo llamado “texto en negrita” y proporcionar la clase de CSS “grosor de fuente: negrita”. Puede utilizar o aplicar estos estilos a un formulario adaptable en el editor de formularios adaptable. Para aplicar un estilo, en el editor de Formularios adaptables, seleccione el componente al que desee aplicar el estilo, vaya al cuadro de diálogo de propiedades y seleccione el estilo que desee en la lista desplegable **Estilos**. Si necesita actualizar o modificar los estilos, simplemente vuelva al cuadro de diálogo Diseño, actualice los estilos en la pestaña Estilos y guarde los cambios.

### Propiedades personalizadas

![Cuadro de diálogo Propiedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

Las propiedades personalizadas le permiten asociar atributos personalizados (pares clave-valor) a un componente principal del formulario adaptable mediante la plantilla de un formulario. Las propiedades personalizadas se reflejan en la sección de propiedades de la representación sin encabezado del componente. Permite crear un comportamiento de formulario dinámico que se adapta en función de los valores de atributos personalizados. Por ejemplo, los desarrolladores pueden diseñar varias representaciones de un componente Forms sin encabezado para plataformas móviles, de escritorio o web, lo que mejora significativamente la experiencia del usuario en una amplia gama de dispositivos.
- **Nombre de grupo**: puede proporcionar un nombre para identificar el grupo de propiedades personalizadas. Puede agregar, eliminar o reorganizar varios grupos de propiedades personalizadas. Después de añadir el grupo de propiedades personalizadas, podrá ver las siguientes opciones:

   - **Pares de clave-valor**: puede agregar varios nombres de propiedades personalizadas y valores de propiedades personalizadas haciendo clic en el botón **Añadir** para cada grupo de propiedades personalizadas.

   - **Eliminar**: toque o haga clic para eliminar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.

   - **Reorganizar**: toque o haga clic y arrastre para reorganizar el nombre de la propiedad personalizada y el valor de la propiedad personalizada.


## Artículos relacionados {#related-articles}

{{more-like-this}}

## Consulte también {#see-also}

{{see-also}}
