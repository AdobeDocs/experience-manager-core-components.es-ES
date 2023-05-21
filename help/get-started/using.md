---
title: Uso de componentes principales
description: '"Para poner en marcha los componentes principales en su propio proyecto, hay que seguir tres pasos: descargar e instalar, crear componentes proxy, cargar los estilos principales y permitir los componentes de las plantillas".'
role: Architect, Developer, Admin, User
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 100%

---

# Uso de componentes principales{#using-core-components}

Para ponerse en marcha con los componentes principales de su propio proyecto, hay cuatro pasos que se detallan individualmente en las siguientes secciones:

1. [Descargar e instalar](#download-and-install)
1. [Crear componentes proxy](#create-proxy-components)
1. [Cargar los estilos principales](#load-the-core-styles)
1. [Habilitar los componentes](#allow-the-components)

>[!TIP]
>
>Para obtener instrucciones más amplias sobre cómo empezar desde cero con la configuración del proyecto, los componentes principales, las plantillas editables, las bibliotecas de clientes y el desarrollo de componentes, el siguiente tutorial de varias partes puede ser de interés:\
>[Introducción a AEM Sites: Tutorial de WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=es)

>[!TIP]
>
>Si utiliza el [tipo de archivo del proyecto de AEM,](/help/developing/archetype/overview.md) los componentes principales se incluyen automáticamente en el proyecto en función de las recomendaciones de prácticas recomendadas de Adobe.

## Descargar e instalar {#download-and-install}

Una de las ideas que impulsan los componentes principales es la flexibilidad. La publicación de nuevas versiones de los componentes principales con más frecuencia permite que Adobe sea más flexible a la hora de ofrecer nuevas funciones. A su vez, los desarrolladores pueden ser flexibles en qué componentes eligen integrar en sus proyectos y con qué frecuencia desean actualizarlos. Esto resulta en un proceso de versión independiente tanto para los componentes principales como para los de AEM.

Por lo tanto, tanto si está ejecutando AEM Cloud Service como local, determinará los pasos de instalación.

### AEM as a Cloud Service {#aemaacs}

¡No hay paso uno! AEM Cloud Service viene automáticamente con la última versión de los componentes principales. Al igual que AEMaaCS le ofrece las últimas funciones de AEM, AEMaaCS le mantiene actualizado automáticamente con la última versión de los componentes principales.

Algunos puntos que se deben tener en cuenta al utilizar los componentes principales en AEMaaCS:

* Los componentes principales se incluyen en `/libs`.
* La canalización de la generación de proyectos generará advertencias en el registro si vuelve a incluir los componentes principales como parte de `/apps` e ignorará la versión incrustada como parte del proyecto.
   * En una próxima versión, volver a incluir los componentes principales producirá un error en la compilación de la canalización.
* Si el proyecto anteriormente incluía los componentes principales en `/apps`, [es posible que tenga que ajustar el proyecto.](/help/developing/overview.md#via-aemaacs)
* Aunque los componentes principales se encuentran ahora en `/libs`, no se recomienda crear ninguna superposición de la misma ruta en `/apps`. En lugar de eso, se debe utilizar el [patrón de componentes proxy](/help/developing/guidelines.md#proxy-component-pattern) si fuera necesario personalizar cualquier aspecto de los componentes.
* Para que el [Componente Tabla de contenido](/help/components/tableofcontents.md) procese su contenido, es necesario configurar un filtro en OSGi.
   * [Consulte la documentación de GitHub del componente](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) para más información.

### AEM 6.5 y anteriores {#aem-65}

Los componentes principales no forman parte del inicio rápido al iniciarse en el modo de producción (sin contenido de ejemplo). Por lo tanto, el primer paso es [descargar el último paquete de contenido publicado desde GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalarlo en sus entornos de AEM.

Existen varias formas de automatizar esto, pero la forma más sencilla de instalar rápidamente un paquete de contenido en una instancia es mediante el uso del Administrador de paquetes; consulte [Instalar paquetes](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=es#installing-packages). Además, una vez que también tenga una instancia de publicación en ejecución, deberá replicar ese paquete al editor; consulte [Duplicación de paquetes](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=es#replicating-packages).

## Crear componentes proxy {#create-proxy-components}

Por los motivos explicados en la sección [Patrón de componentes proxy](/help/developing/guidelines.md#proxy-component-pattern), no se debe hacer referencia directamente a los componentes principales desde el contenido. Para evitarlo, todos pertenecen a un grupo de componentes ocultos (`.core-wcm` o `.core-wcm-form`), lo que impide que se muestren directamente en el editor.

En lugar de eso, se deben crear componentes específicos del sitio, que definan el nombre y el grupo del componente deseado para mostrarlos a los autores de la página y hacen referencia cada uno a un componente principal como su supertipo. Estos componentes específicos del sitio a veces se denominan &quot;componentes proxy&quot;, ya que no necesitan contener nada y sirven principalmente para definir la versión de un componente que se utilizará para el sitio. Sin embargo, al personalizar los [Componentes principales](/help/developing/customizing.md), estos componentes proxy desempeñan un papel esencial para el marcado y la personalización lógica.

Por lo tanto, para cada componente principal que se desee utilizar en un sitio, debe:

1. Crear un componente proxy correspondiente en la carpeta de componentes del sitio.

   **Ejemplo**
En `/apps/my-site/components` crear un nodo de título de tipo `cq:Component`

1. Seleccionar la versión del componente principal correspondiente con el supertipo.

   **Ejemplo**
Agregar la siguiente propiedad:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina el grupo, el título y, opcionalmente, la descripción del componente. Estos valores son específicos del proyecto y dictan cómo se expone el componente a los autores.

   **Ejemplo**
Añadir las siguientes propiedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por ejemplo, observe el [componente titular del sitio WKND](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), que es un buen ejemplo de un componente proxy generado de esa manera.

## Cargar los estilos principales {#load-the-core-styles}

1. Si aún no lo ha hecho, cree una [Biblioteca de clientes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=es) que contenga todos los archivos CSS y JS necesarios para su sitio.
1. En la biblioteca de clientes de su sitio, agregue las dependencias para los componentes principales que puedan ser necesarias. Esto se hace añadiendo una propiedad `embed`.

   Por ejemplo, para incluir las bibliotecas de clientes de todos los componentes principales de la versión 1, la propiedad que se agregaría sería:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Asegúrese de que los componentes proxy y las bibliotecas de clientes se hayan implementado en el entorno de AEM antes de pasar a la siguiente sección.

## Permitir los componentes {#allow-the-components}

Los siguientes pasos se realizan en el [Editor de plantillas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=es).

1. En el Editor de plantillas, seleccione el contenedor de diseño y abra su directiva.
1. En la lista de componentes permitidos, seleccione los componentes proxy creados anteriormente, que deberían aparecer en el grupo de componentes asignado a ellos. Una vez finalizado, aplique los cambios.
1. De forma opcional, los componentes que tienen un cuadro de diálogo de diseño, se pueden preconfigurar.

¡Eso es todo! En las páginas creadas a partir de la plantilla editada, ahora debería poder utilizar los componentes recién creados.

**Consulte lo siguiente:**

* [Personalizar componentes principales](/help/developing/customizing.md): para aprender a aplicar estilos y personalizar los componentes principales.
* [Directrices de componentes](/help/developing/guidelines.md): para conocer los patrones de implementación de los componentes principales.
