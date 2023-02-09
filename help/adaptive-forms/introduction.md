---
title: Introducción a los componentes principales AEM adaptables de Forms
description: Cree experiencias de inscripción atractivas (formularios) con la flexibilidad de los componentes principales de Forms adaptables y suministre dicha flexibilidad con la potencia de Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: 781cf351ef52cbb56ff33c2674c8af591c81a30e
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 13%

---


# Introducción a los componentes principales de Forms adaptable {#adaptive-forms-core-components-introduction}

Con los componentes principales de Forms adaptable en Adobe Experience Manager, puede crear atractivas experiencias de inscripción utilizando las opciones de flexibilidad y personalización disponibles.

## Componentes principales   {#overview}

En Adobe Experience Manager (AEM), los componentes son los componentes básicos que se utilizan para crear páginas y formularios. Proporcionan una forma sencilla y potente para que los autores creen y gestionen el contenido, a la vez que proporcionan a los desarrolladores la flexibilidad y la extensibilidad necesarias para crear componentes personalizados.

Los componentes principales son un conjunto de componentes WCM estandarizados y pregenerados diseñados para acelerar el tiempo de desarrollo y reducir los costes de mantenimiento de los sitios web. Estos componentes incluyen campos de texto, imágenes, vídeos, etc. Están diseñadas para ser flexibles y pueden personalizarse fácilmente según las necesidades específicas de un sitio web.

Los componentes principales también están diseñados para ser interactivos y admiten una amplia gama de dispositivos, incluidos escritorios, tabletas y teléfonos inteligentes. También se adhieren a los últimos estándares web y prácticas recomendadas, convirtiéndolos en una solución sólida y fiable para crear contenido web.

Además, los componentes principales están diseñados para funcionar sin problemas con otras partes de AEM, lo que permite a los autores y desarrolladores crear formularios más interactivos y atractivos con menos esfuerzo y menos tiempo.

En general, los componentes principales son una herramienta esencial para crear y administrar el contenido web en AEM, lo que proporciona una solución potente y flexible que puede ayudar a reducir el tiempo de desarrollo y los costes de mantenimiento, al tiempo que proporciona una buena experiencia de usuario a los visitantes del sitio web.

En Adobe Experience Manager, los componentes son los elementos estructurales que constituyen el contenido de las páginas y los formularios que se crean. Los componentes siempre han sido un elemento fundamental de la experiencia AEM, lo que hace que la creación de páginas y formularios sea sencilla pero eficaz para el autor y el desarrollo de componentes sea flexible y extensible para el desarrollador. Los componentes principales son un conjunto de componentes estandarizados de Administración de contenido web (WCM) para acelerar el tiempo de desarrollo y reducir el coste de mantenimiento de los sitios web.

## Componentes principales adaptables de Forms

Los componentes principales de Forms adaptable son un conjunto de 24 componentes de código abierto compatibles con BEM que se basan en los componentes principales de WCM de Adobe Experience Manager. Están diseñadas específicamente para utilizarse en la creación de Forms adaptable, que son formularios que se adaptan al dispositivo, navegador y tamaño de pantalla del usuario.

Estos componentes se pueden utilizar para crear experiencias de inscripción y captura de datos excepcionales proporcionando una amplia gama de opciones de campo de formulario, incluidos campos de texto, casillas de verificación, menús desplegables y mucho más. También incluyen funciones como validación, lógica condicional y diseño interactivo, que pueden utilizarse para crear formularios fáciles de usar y fáciles de usar.

Además, como estos componentes son de código abierto, los desarrolladores pueden personalizar y ampliar fácilmente los componentes para adaptarlos a las necesidades específicas de su organización. Además, estos componentes se basan en la metodología de BEM, que garantiza que sean escalables y mantenibles.

![](assets/sample-adaptive-form.png)

## Características {#features}

|  |  |
|---|---|
| Listo para la producción | Los componentes principales de Forms adaptable son 24 componentes WCM sólidos. |
| Preparado para la nube | Disponible para  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Versátil | Los componentes representan conceptos genéricos con los que los autores de Forms pueden ensamblar casi cualquier diseño. |
| Configurable | Nivel de plantilla [políticas de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=es#content-policies) defina qué funciones se pueden utilizar o no. |
| Accesible | Cumplen con [WCAG 2.1 estándar](https://www.w3.org/TR/WCAG21/), proporcione etiquetas ARIA, admita la navegación mediante el teclado ([problemas conocidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) y texto para tecnologías de asistencia, como lectores de pantalla. |
| Configurable | Los componentes implementan el [Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=es) y el marcado sigue la [nomenclatura de BEM CSS](http://getbem.com/). |
| Personalizable | Varios patrones permiten una fácil personalización, desde ajustar el HTML a una reutilización avanzada de la funcionalidad. |
| Versiones | La [directiva de versiones](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiza que los componentes principales no romperán el sitio al mejorar las cosas que puedan afectarle. |
| Abrir origen | Si algo no es como debería, contribuya con su mejora. |

## Ventajas {#benefits}

Las experiencias de captura de datos son cruciales para la generación de posibles clientes y la inscripción, y los componentes principales de Forms adaptables proporcionan una solución potente para la creación de formularios optimizados para la captura de datos. Algunas de las razones para utilizar los componentes principales para crear estas experiencias son:

* **Personalización**: Los componentes principales de Forms adaptables permiten a los desarrolladores personalizar fácilmente el aspecto y el comportamiento de los componentes del formulario, como los campos de texto, las casillas de verificación y los menús desplegables, para satisfacer los requisitos específicos.

* **Accesibilidad**: Los componentes principales de Forms adaptables admiten normas y directrices de accesibilidad, como  [WCAG 2.1 estándar](https://www.w3.org/TR/WCAG21/), para garantizar que las personas con discapacidades puedan utilizar los formularios, incluidos los que utilizan tecnologías de asistencia, como lectores de pantalla.

* **Formularios coherentes**: Mediante los componentes principales de Forms adaptable, los desarrolladores pueden crear formularios con un aspecto y una presentación coherentes, lo que facilita a los usuarios la comprensión y la finalización de los formularios, lo que aumenta la participación y mejora la experiencia del usuario.

* **Editor WYSIWYG**: AEM Forms proporciona una interfaz fácil de usar y facilita el uso del editor WYSIWYG para utilizar estos componentes para crear un formulario adaptable. Permite a los autores de formularios crear y editar formularios sin necesidad de saber cómo codificarlos. También incluye un editor de reglas visual que le ayuda a crear acciones basadas en reglas fácilmente e implementar lógica compleja para automatizar el comportamiento del formulario sin tener que escribir código.

* **Lógica condicional**: Los componentes principales de Forms adaptables admiten el uso de la lógica condicional, lo que significa que el aspecto o el comportamiento de los componentes del formulario se pueden cambiar en función de los valores introducidos por el usuario. Por ejemplo, ciertos campos pueden ocultarse o hacerse obligatorios en función de la selección realizada en otros campos.

* **Validación de datos**: Los componentes principales de Forms adaptables proporcionan capacidades de validación de datos integradas, lo que permite a los desarrolladores garantizar que los datos introducidos por el usuario cumplen criterios específicos, como longitudes mínimas y máximas, valores requeridos y formatos específicos.

## Requisitos  {#requirements}

Los componentes principales de Forms adaptable tienen los siguientes requisitos:

| AEM | Complemento de AEM Forms | Componentes principales |
|---|---|---|
| AEM as a Cloud Service | Forms: inscripción digital | [Versión 2.20.8](/help/versions.md)+ |


## Componentes principales adaptables de Forms {#components}

La versión actual de los componentes principales de Forms adaptable incluye los siguientes componentes.

* Acordeón
* Botón
* Casilla de verificación Grupo
* Selector de fecha
* Lista desplegable
* Entrada de correo electrónico
* Contenedor del formulario
* Archivo adjunto
* Pie de página
* Encabezado
* Pestañas horizontales
* Imagen
* Entrada de número
* Contenedor de panel
* Botón de opción
* Botón Restablecer
* Botón Enviar
* Entrada de teléfono
* Entrada de texto
* Texto
* Título
* Asistente

