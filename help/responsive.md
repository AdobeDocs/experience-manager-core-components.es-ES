---
title: Diseño interactivo de los componentes principales
description: Conozca el diseño interactivo de los componentes principales y cómo puede afectar su proyecto.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 178
ht-degree: 100%

---

# Diseño interactivo de los componentes principales {#responsive-design}

Todos los componentes principales están diseñados para responder completamente, lo que garantiza una experiencia sin problemas en todos los dispositivos. Es importante tener en cuenta que algunos componentes avanzados, como por ejemplo el [Carrusel,](/help/components/carousel.md) [Pestañas,](/help/components/tabs.md) y [Componentes de acordeón,](/help/components/accordion.md) pueden requerir una consideración específica dentro del contexto del proyecto de implementación para mantener la capacidad de respuesta en todas las condiciones.

Dadas las diversas formas en que estos componentes pueden exhibir un comportamiento interactivo, y en el compromiso de Adobe de mantener los componentes principales livianos y listos para usar, la responsabilidad de implementar aspectos interactivos detallados se deja intencionalmente al proyecto.

Por ejemplo, en pantallas estrechas, el componente Pestañas puede adaptarse dividiendo pestañas anchas en nuevas líneas, permitiendo el desplazamiento vertical, transformando pestañas en menús desplegables o adoptando un estilo de acordeón. Debido al impacto potencial en el desempeño que causaría la implementación de todos esos comportamientos, las [clientlibs](/help/developing/including-clientlibs.md#provided) pretenden ser un punto de partida para los implementadores más que una solución exhaustiva.
