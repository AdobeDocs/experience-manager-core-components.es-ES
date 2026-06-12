---
title: Variables de campaña
description: Utilice variables de campaña como marcadores de posición para crear contenido de correo electrónico personalizado.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Variables de campaña {#campaign-variables}

Utilice variables de campaña para crear contenido de correo electrónico personalizado. Las variables de campaña actúan como marcadores de posición para valores de Adobe Campaign que puede insertar en el contenido del correo electrónico. Cuando el contenido se envía mediante Adobe Campaign, Campaign reemplaza esas variables con el contenido personalizado del destinatario.

## Uso {#usage}

Los componentes principales de correo electrónico facilitan el acceso a las variables de campaña mediante botones de personalización junto a campos de texto comunes. Cuando se presionan, aparece un cuadro de diálogo desde el que puede seleccionar un campo de personalización.

La lista de campos de personalización disponibles se sincroniza con su instancia de Adobe Campaign. Los campos se administran en Adobe Campaign en el esquema `nms:seedMember`. Todos los campos de `nms:seedMember` también debe estar presentes en la tabla de destinatarios.

## Diálogo Seleccionar la variable de Adobe Campaign {#dialog}

El cuadro de diálogo Seleccionar la variable de Adobe Campaign está disponible en muchos cuadros de diálogo de edición de los componentes principales de correo electrónico. Para usarlo, simplemente haga clic en el icono **Seleccionar la variable de Adobe Campaign** junto al campo correspondiente. Este icono puede adoptar dos formas.

![Botón de Adobe Campaign](/help/email/assets/campaign-button.png)
![Icono Seleccionar la variable de Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Al hacer clic en ambos iconos, se abre el diálogo **Seleccionar la variable de Adobe Campaign**.

![Diálogo Seleccionar la variable de Adobe Campaign](assets/select-campaign-variable-dialog.png)

Utilice la vista de columna para localizar la variable que desea insertar. Al hacer clic en un nodo de una columna, se muestran sus tareas secundarias en una nueva columna a la derecha. De este modo, puede desplazarse por la estructura de contenido variable.

Seleccione la variable que desee insertar y, a continuación, haga clic en la marca de verificación situada en la parte superior derecha del cuadro de diálogo.

![Variable de Adobe Campaign seleccionada](assets/select-campaign-variable-dialog-selected.png)

A continuación, la variable se inserta en el campo del cuadro de diálogo de edición del componente principal de correo electrónico.

![Variable de campaña insertada en el cuadro de diálogo de edición](assets/campaign-variable.png)

Haga clic en la X situada en la parte superior izquierda del cuadro de diálogo en cualquier momento para cancelar y cerrarlo.
