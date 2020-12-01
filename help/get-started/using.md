---
title: Uso de componentes principales
description: '"Para ponerse en marcha con los componentes principales de su propio proyecto, hay que seguir tres pasos: descargar e instalar, crear componentes proxy, cargar los estilos principales y permitir los componentes en las plantillas".'
translation-type: tm+mt
source-git-commit: 78202dc777b90f795f66873921c55e21ef8a239c
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 4%

---


# Uso de componentes principales{#using-core-components}

Para ponerse en marcha con los componentes principales de su propio proyecto, hay cuatro pasos que se detallan individualmente en las secciones siguientes:

1. [Descargar e instalar](#download-and-install)
1. [Creación de componentes proxy](#create-proxy-components)
1. [Carga de los estilos principales](#load-the-core-styles)
1. [Habilitar los componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obtener instrucciones más amplias sobre cómo empezar desde cero con la configuración del proyecto, los componentes principales, las plantillas editables, las bibliotecas de clientes y el desarrollo de componentes, el siguiente tutorial de varias partes puede ser de interés:\
>[Introducción a AEM Sites: Tutorial de WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Descargar e instalar {#download-and-install}

Una de las ideas que impulsan los componentes principales es la flexibilidad. La publicación de nuevas versiones de los componentes principales con más frecuencia permite a Adobe ser más flexible al ofrecer nuevas funciones. A su vez, los desarrolladores pueden ser flexibles en cuanto a los componentes que eligen integrar en sus proyectos y a la frecuencia con la que desean actualizarlos.

Por este motivo, los componentes principales no forman parte del inicio rápido cuando se inician en modo de producción (sin contenido de muestra). Por lo tanto, su primer paso es [descargar el último paquete de contenido publicado de GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalarlo en sus entornos de AEM.

Existen varias formas de automatizar esto, pero la forma más sencilla de instalar rápidamente un paquete de contenido en una instancia es mediante el uso del Administrador de paquetes; consulte [Instalación de paquetes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Además, una vez que tenga una instancia de publicación en ejecución también, deberá replicar ese paquete al editor; consulte [Replicación de paquetes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Crear componentes proxy {#create-proxy-components}

Por motivos explicados en la sección [Patrón de componentes proxy](/help/developing/guidelines.md#proxy-component-pattern), no se debe hacer referencia a los componentes principales directamente desde el contenido. Para evitarlo, todos pertenecen a un grupo de componentes ocultos ( `.core-wcm` o `.core-wcm-form`), lo que impedirá que se muestren directamente en el editor.

En su lugar, se deben crear componentes específicos del sitio, que definan el nombre y el grupo del componente deseado para que se muestren a los autores de la página y remitan cada uno a un componente principal como su supertipo. Estos componentes específicos del sitio a veces se denominan &quot;componentes proxy&quot;, ya que no necesitan contener nada y sirven principalmente para definir la versión de un componente que se va a utilizar en el sitio. Sin embargo, al personalizar los [Componentes principales](/help/developing/customizing.md), estos componentes proxy juegan un papel esencial en el marcado y la personalización lógica.

Por lo tanto, para cada componente principal que desee utilizar en un sitio, debe:

1. Cree un componente proxy correspondiente en la carpeta de componentes del sitio.

   ****
EjemploEn  `/apps/my-site/components` Crear un nodo de título de tipo  `cq:Component`

1. Seleccione la versión correspondiente del componente principal con el supertipo.

   ****
EjemploAgregue la siguiente propiedad:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina el grupo, el título y la descripción opcional del componente. Estos valores son específicos del proyecto y dictan cómo se expone el componente a los autores.

   ****
EjemploAgregue las siguientes propiedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por ejemplo: observe el componente [title del sitio WKND](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), que es un buen ejemplo de un componente proxy que se genera de esa manera.

## Cargue los estilos principales {#load-the-core-styles}

1. Si aún no lo ha hecho, cree una [biblioteca de clientes](https://docs.adobe.com/content/help/es-ES/experience-manager-65/developing/introduction/clientlibs.html) que contenga todos los archivos CSS y JS necesarios para su sitio.
1. En la biblioteca de clientes de su sitio, agregue las dependencias a los componentes principales que podrían ser necesarias. Esto se realiza agregando una propiedad `embed`.

   Por ejemplo, para incluir las bibliotecas de cliente de todos los componentes principales v1, la propiedad que se debe agregar sería:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Asegúrese de que los componentes proxy y las bibliotecas de cliente se han implementado en el entorno de AEM antes de pasar a la siguiente sección.

## Permitir los componentes {#allow-the-components}

Los pasos siguientes se realizan en el [Editor de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. En el Editor de plantillas, seleccione el Contenedor Presentación y abra su política.
1. En la lista de componentes permitidos, seleccione los componentes proxy creados anteriormente, que deben aparecer en el grupo de componentes asignado a ellos. Una vez realizados, aplique los cambios.
1. Opcionalmente, para los componentes que tienen un cuadro de diálogo de diseño, se pueden preconfigurar.

¡Eso es todo! En las páginas creadas a partir de la plantilla editada, ahora debe poder utilizar los componentes recién creados.

**Consulte lo siguiente:**

* [Personalización de componentes](/help/developing/customizing.md)  principales: para aprender a diseñar y personalizar los componentes principales.
* [Directrices](/help/developing/guidelines.md)  de componentes: para conocer los patrones de implementación de los componentes principales.
