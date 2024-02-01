---
title: Diseño interactivo de los componentes principales
description: Obtenga información acerca del diseño interactivo de los componentes principales y cómo puede afectar a su proyecto.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Diseño interactivo de los componentes principales {#responsive-design}

Todos los componentes principales están diseñados para responder completamente, lo que garantiza una experiencia sin problemas en todos los dispositivos. Es importante tener en cuenta que algunos componentes avanzados, como por ejemplo el [Carrusel,](/help/components/carousel.md) [Fichas,](/help/components/tabs.md) y [Componentes de acordeón,](/help/components/accordion.md) puede requerir una consideración específica en el contexto del proyecto de ejecución a fin de mantener la capacidad de respuesta en todas las condiciones.

Dada la diversidad de formas en que estos componentes pueden mostrar un comportamiento interactivo, y en el compromiso de Adobe de mantener los componentes principales ligeros listos para usar, la responsabilidad de implementar los componentes interactivos detallados se deja intencionalmente en manos del proyecto.

Por ejemplo, en pantallas estrechas, el componente Pestañas puede adaptarse dividiendo pestañas anchas en nuevas líneas, permitiendo el desplazamiento vertical, transformando pestañas en desplegables o adoptando un estilo de acordeón. Debido al impacto potencial en el rendimiento que causaría la implementación de todos estos comportamientos, la variable [clientlibs](/help/developing/including-clientlibs.md#provided) se han diseñado como punto de partida para los implementadores, en lugar de como una solución exhaustiva.
