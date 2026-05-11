---
title: Habilitar y utilizar patrones de validación de entrada de texto en los formularios adaptables de Adobe Experience Manager
description: Aprenda a configurar políticas de plantilla para exponer patrones de validación como números de teléfono, números de la seguridad social y códigos postales y, a continuación, utilícelos en sus formularios adaptables.
hide: true
exl-id: e4500666-1346-4558-861d-da9541dcef51
source-git-commit: 59064c359aea14af99675709bbddf9a933a959df
workflow-type: ht
source-wordcount: '861'
ht-degree: 100%

---

# Habilitar y utilizar patrones de validación de entrada de texto en los formularios adaptables de Adobe Experience Manager

## Información general

En los formularios de Adobe Experience Manager (Adobe Experience Manager), los formatos de validación específicos (como números de la seguridad social, direcciones de correo electrónico o códigos postales) para los componentes de entrada de texto se controlan a nivel de política de plantilla. Esta guía explica cómo:

1. Acceder al editor de plantillas y configurar la política del componente de entrada de texto para exponer los patrones de validación.
2. Cree un formulario adaptable y aplique esos patrones de validación a un componente de entrada de texto.

## Requisitos previos

- Acceda a una instancia de Adobe Experience Manager con formularios habilitados.
- Permisos para editar plantillas (normalmente, parte del grupo `template-authors`).
- Permisos para crear y editar formularios adaptables.

## Parte 1: Habilitar patrones de validación en la plantilla

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Paso 1: Acceder a la consola Plantillas

1. En la pantalla de inicio de Adobe Experience Manager, haga clic en **Herramientas** (el icono del martillo) en la barra lateral izquierda.
2. Vaya a **General > Plantillas**.
3. Seleccione la carpeta que contiene las plantillas de proyecto (por ejemplo, ejemplos de componentes principales).
4. Busque la plantilla específica que desea modificar (por ejemplo, AF en blanco) y selecciónela.
5. Haga clic en **Editar** (o abra la plantilla directamente).

### Paso 2: Acceder a la estructura del componente

1. Asegúrese de que está en la vista **Estructura** (seleccione “Estructura” en la lista desplegable de modo en la parte superior derecha si es necesario).
2. Busque el **contenedor de diseño** principal o el contenedor específico donde se permite el componente de entrada de texto.
3. Haga clic en el contenedor para mostrar la lista de componentes permitidos.
4. Busque el componente **Cuadro de texto del formulario adaptable** en la lista.
5. Haga clic en el icono **Política** (representado por un símbolo de archivo o cajón) junto al nombre del componente.

### Paso 3: Configurar la política del componente de entrada de texto

1. En el editor de políticas, haga clic en la pestaña **Formatos** en el lado derecho de la ventana.
2. Verá una lista de patrones de validación disponibles. Marque las casillas de los formatos que desee habilitar:
   - Número de teléfono
   - Número de la seguridad social
   - Correo electrónico alfanumérico
   - Código postal

### Paso 4: Definir y guardar la política

1. Vuelva a la pestaña **Política** (o compruebe la configuración izquierda).
2. En el campo **Título de la política**, introduzca un nombre claro (por ejemplo, `new-textinput-default-policy`).
3. Haga clic en el icono (marca de verificación)**Listo** en la esquina superior derecha para guardar los cambios.

## Parte 2: Crear un formulario y utilizar patrones de validación

Ahora que los patrones de validación están habilitados en la plantilla, puede crear un formulario adaptable y aplicarlos a los componentes de entrada de texto.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Paso 3: Crear un formulario adaptable

1. Vaya a la interfaz **Formularios y documentos**.
2. Haga clic en el botón **Crear** en la esquina superior derecha.
3. Seleccione **Formulario adaptable** en las opciones desplegables.
4. Elija la plantilla donde habilitó los patrones de validación (por ejemplo, **En blanco**) y haga clic en **Siguiente**.
5. En la pantalla Añadir propiedades:
   - Escriba un **Título** para su formulario (por ejemplo, “testPolicy”). El campo **Nombre** se rellena automáticamente en función del título.
   - Asegúrese de que está seleccionada la **Biblioteca de cliente de temas** correcta (por ejemplo, `adaptiveform.theme.canvas3`).
6. Haga clic en **Crear**. Aparecerá un mensaje de éxito.
7. Haga clic en **Editar** para abrir el formulario en el editor.

### Paso 2: Añadir un componente de entrada de texto

1. En el editor de formularios, busque el explorador de **Componentes** en la barra lateral izquierda.
2. Utilice la barra de búsqueda para encontrar el componente **Cuadro de texto del formulario adaptable**. Escribir “texto” filtra la lista.
3. Haga clic en el componente **Cuadro de texto del formulario adaptable** y arrástrelo al área del lienzo principal.

### Paso 3: Configurar el formato del componente

1. Haga clic en el componente **Entrada de texto** que acaba de añadir para seleccionarlo.
2. Haga clic en el icono **Configurar** (representado por una llave inglesa) en la barra de herramientas que aparece sobre el componente.
3. En el cuadro de diálogo de propiedades, vaya a la pestaña **Formatos**.
4. Busque el menú desplegable **Tipo** y cambie la selección a **Número de teléfono** (u otro formato habilitado).

### Paso 4: Configurar la validación de datos

1. Mientras sigue en el cuadro de diálogo de la configuración del componente, vaya a la pestaña **Validación**.
2. Busque la sección **Patrón de validación**.
3. Haga clic en el menú desplegable **Tipo**.
4. Seleccione **Número de teléfono** de la lista de patrones de validación. Esto garantiza que el formulario produzca un error si el usuario introduce texto que no coincide con un formato de número de teléfono válido.
5. Haga clic en el icono **Listo** (marca de verificación) en la parte superior derecha del cuadro de diálogo para guardar los cambios.

## de verificación

Para comprobar que los patrones de validación funcionan correctamente:

1. Previsualice el formulario en el editor.
2. Escriba datos de prueba en el componente **Entrada de texto**.
3. Confirme que:
   - Los patrones de validación habilitados aparecen en las pestañas Formatos y Validación del componente.
   - La entrada no válida activa los mensajes de error correspondientes.
   - Se acepta una entrada válida sin errores.

## Solución de problemas

- **Problema:** los patrones de validación no aparecen en el componente del formulario.
   - **Solución:** asegúrese de que la política de plantilla se guardó correctamente y de que está usando la plantilla correcta al crear el formulario.

- **Problema:** no se puede obtener acceso al editor de plantillas.
   - **Solución:** compruebe que dispone de los permisos necesarios para editar plantillas (pertenencia al grupo `template-authors`).

- **Problema:** el componente Entrada de texto no valida la entrada correctamente.
   - **Solución:** vuelva a comprobar la configuración del patrón de validación en la pestaña Validación del componente y asegúrese de que esté seleccionado el patrón correcto.

## Próximos pasos

Después de habilitar y utilizar los patrones de validación de entrada de texto en los formularios adaptables de Adobe Experience Manager:

- Configure patrones de validación adicionales para otros tipos de datos.
- Explore otras políticas de componentes para personalizar el comportamiento del formulario.
- Configure la gestión del envío de formularios y la lógica de procesamiento de datos.
