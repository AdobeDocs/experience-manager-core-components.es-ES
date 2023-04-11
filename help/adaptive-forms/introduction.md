---
title: Introducción a los componentes principales de formularios adaptables de AEM
description: Cree experiencias de inscripción atractivas (formularios) con la flexibilidad de los componentes principales de formularios adaptables y suministre dicha flexibilidad con la potencia de Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 0dec0b1e1d5303a8351d16f748f064a49128cbb3
workflow-type: ht
source-wordcount: '1028'
ht-degree: 100%

---

# Introducción a los componentes principales de formularios adaptables {#adaptive-forms-core-components-introduction}

Con los componentes principales de formularios adaptables en Adobe Experience Manager, puede crear atractivas experiencias de inscripción utilizando las opciones de flexibilidad y personalización disponibles.

## Componentes principales   {#overview}

En Adobe Experience Manager (AEM), los componentes son los elementos básicos que se utilizan para crear páginas y formularios. Proporcionan una forma sencilla y potente para que los autores creen y gestionen el contenido, a la vez que proporcionan a los desarrolladores la flexibilidad y la capacidad de ampliación necesaria para crear componentes personalizados. Están diseñadas para acelerar el tiempo de desarrollo y reducir los costes de mantenimiento de sitios web y formularios, ser flexibles y se pueden personalizar fácilmente para adaptarse a las necesidades específicas de un sitio web y un formulario.

Los componentes principales también están diseñados para ser adaptables y admiten una amplia gama de dispositivos, incluidos ordenadores de sobremesa, tabletas y teléfonos inteligentes. También cumplen con los últimos estándares web y prácticas recomendadas, convirtiéndolos en una solución firme y fiable para crear contenido web.

En general, los componentes principales son una herramienta esencial para crear y administrar el contenido web en AEM, lo que proporciona una solución potente y flexible que puede ayudar a reducir el tiempo de desarrollo y los costes de mantenimiento, al tiempo que proporciona una buena experiencia de usuario a los visitantes del sitio web.

## Componentes principales de formularios adaptables

Los componentes principales de formularios adaptables son un conjunto de 24 componentes de código abierto compatibles con BEM que se basan en los componentes principales de la gestión de contenidos web de Adobe Experience Manager. Están diseñadas específicamente para utilizarse en la creación de formularios adaptables, que son formularios que se adaptan al dispositivo, navegador y tamaño de pantalla del usuario.

Estos componentes se pueden utilizar para crear experiencias de inscripción y captura de datos excepcionales, proporcionando una amplia gama de opciones de campo de formulario, incluidos campos de texto, casillas de verificación, menús desplegables y mucho más. También incluyen funciones como validación, lógica condicional y diseño interactivo, que pueden utilizarse para crear formularios de fácil manejo y sencillos de usar.

Además, como estos componentes son de código abierto, los desarrolladores pueden personalizar y ampliar fácilmente los componentes para adaptarlos a las necesidades específicas de su organización. Además, estos componentes se basan en la metodología de BEM, que garantiza que sean escalables y mantenibles.

![](assets/sample-adaptive-form.png)

## Características {#features}

|  |  |
|---|---|
| Listo para la producción | Los componentes principales de formularios adaptables son 24 componentes WCM sólidos. |
| Preparado para la nube | Disponible para [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=es). |
| Versátil | Los componentes representan conceptos genéricos con los que los autores de formularios pueden montar casi cualquier diseño. |
| Configurable | Las [políticas de contenido](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=es#content-policies) con respecto a la plantilla definen qué características pueden utilizar o no los autores de la página. |
| Accesible | Proporcionan etiquetas ARIA, admiten la navegación mediante el teclado ([problemas conocidos](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) y texto para tecnologías de asistencia, como lectores de pantalla. |
| Tema capaz | Los componentes implementan el [Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=es) y el marcado sigue la [nomenclatura de BEM CSS](https://getbem.com/). |
| Personalizable | Varios patrones permiten una fácil personalización, desde ajustar el HTML a una reutilización de funcionalidades avanzadas. |
| Versiones | La [directiva de versiones](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) garantiza que los componentes principales no romperán el sitio al mejorar las cosas que puedan afectarle. |
| Abrir Con origen en | Si algo no funciona como debería, contribuya a su mejora. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Ventajas {#benefits}

Las experiencias de captura de datos son cruciales para la generación de posibles clientes y la inscripción, y los componentes principales de formularios adaptables proporcionan una solución potente para la creación de formularios optimizados para la captura de datos. Algunas de las razones para utilizar los componentes principales para crear estas experiencias sobre los componentes básicos son las siguientes:

* **Disponibilidad en GitHub y documentación completa**: los componentes principales de formularios adaptables de AEM son de código abierto y están disponibles en GitHub, además de una documentación exhaustiva. Esto facilita a los desarrolladores la comprensión de los componentes y de cómo funcionan, así como la contribución a su desarrollo. El sitio web [aemcomponents.dev](https://www.aemcomponents.dev/) también es un recurso valioso, donde los desarrolladores pueden ver los componentes en acción y acceder a la documentación detallada.

* **Modelo BEM para estilo**: los componentes principales siguen el modelo de estilo de BEM (Modificador de elementos de bloque), que es una metodología establecida y ampliamente utilizada para organizar CSS. Esto facilita a los desarrolladores comprender cómo se organizan los estilos y cómo modificarlos para adaptarlos a sus necesidades específicas.

* **Sin depender de bibliotecas de terceros**: una de las ventajas de los componentes principales es que no dependen de las bibliotecas JavaScript de terceros, incluidas JQuery y Underscore. Esto hace que los componentes sean más rápidos y livianos, así como más fáciles de integrar en una implementación de AEM existente.

* **Centrarse en el rendimiento y la accesibilidad**: los componentes principales se crean teniendo en cuenta el rendimiento y la accesibilidad, lo que se refleja en sus altas puntuaciones de Google Lighthouse y Web Vitals. Esto facilita a los desarrolladores la creación de páginas web accesibles y de alto rendimiento, que es cada vez más importante en el panorama digital actual.

* **Componentes de formulario en plantillas y temas de Sites 30**: los componentes principales son compatibles con los componentes de formulario de la plantilla y los temas de Sites 30, lo que facilita a los desarrolladores la creación y personalización de formularios dentro de AEM.

* **Facilidad al aplicar un estilo**: los componentes principales son más fáciles de diseñar que sus equivalentes de componentes básicos. El proceso de creación del tema es similar al de Sites, con la capacidad de heredar el mismo tema/CSS de la página principal de Sites. Además, el modelo BEM para aplicar estilo facilita la comprensión y modificación de los estilos.

* **Accesibilidad**: los componentes principales de formularios adaptables admiten normas y directrices de accesibilidad para garantizar que las personas con discapacidades puedan utilizar los formularios, incluidos los que utilizan tecnologías de asistencia como lectores de pantalla.


<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



## Requisitos  {#requirements}

Los componentes principales de formularios adaptables tienen los siguientes requisitos:

| AEM | Complementos para AEM Forms | Componentes principales |
|---|---|---|
| AEM as a Cloud Service | Forms: inscripción digital | [Versión 2.20.8](/help/versions.md)+ |


## Componentes principales de formularios adaptables {#components}

Puede utilizar el [Editor de formularios adaptables](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=es) para crear formularios adaptables basados en los componentes principales. La versión actual de los componentes principales de formularios adaptables contiene los siguientes componentes:

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
