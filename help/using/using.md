---
title: Uso de componentes principales
description: '"Para ponerse en marcha con los componentes principales de su propio proyecto, hay que seguir tres pasos: descargar e instalar, crear componentes proxy, cargar los estilos principales y permitir los componentes en las plantillas".'
translation-type: tm+mt
source-git-commit: 945381996db443c227aa31f0aacb963071165681

---


# Uso de componentes principales{#using-core-components}

Para ponerse en marcha con los componentes [](developing.md) principales en su propio proyecto, hay cuatro pasos que se detallan individualmente en las secciones siguientes:

1. [Descargar e instalar](#download-and-install)
1. [Creación de componentes proxy](#create-proxy-components)
1. [Carga de los estilos principales](#load-the-core-styles)
1. [Habilitar los componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obtener instrucciones más amplias sobre cómo empezar desde cero con la configuración del proyecto, los componentes principales, las plantillas editables, las bibliotecas de clientes y el desarrollo de componentes, el siguiente tutorial de varias partes puede ser de interés:\
>[Introducción a los sitios de AEM: Tutorial de WKND](wknd-tutorial.md)

## Descargar e instalar {#download-and-install}

Una de las ideas que impulsan los componentes principales es la flexibilidad. La publicación de nuevas versiones de los componentes principales permite a Adobe ser más flexible a la hora de ofrecer nuevas funciones. A su vez, los desarrolladores pueden ser flexibles en cuanto a los componentes que eligen integrar en sus proyectos y a la frecuencia con la que desean actualizarlos.

Por este motivo, los componentes principales no forman parte del inicio rápido cuando se inician en modo de producción (sin contenido de muestra). Por lo tanto, el primer paso es [descargar el último paquete de contenido publicado de GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalarlo en sus entornos AEM.

Existen varias formas de automatizar esto, pero la forma más sencilla de instalar rápidamente un paquete de contenido en una instancia es mediante el uso del Administrador de paquetes; consulte [Instalación de paquetes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Además, una vez que tenga una instancia de publicación en ejecución también, deberá replicar ese paquete al editor; consulte [Replicar paquetes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Creación de componentes proxy {#create-proxy-components}

Por motivos explicados en la sección Patrón [de componentes](guidelines.md#proxy-component-pattern) proxy, no se debe hacer referencia a los componentes principales directamente desde el contenido. Para evitarlo, todos pertenecen a un grupo de componentes ocultos ( `.core-wcm` o `.core-wcm-form`), lo que impedirá que se muestren directamente en el editor.

En su lugar, se deben crear componentes específicos del sitio, que definan el nombre y el grupo del componente que se desea mostrar a los autores de la página y hacen referencia a cada uno de ellos a un componente principal como supertipo. Estos componentes específicos del sitio a veces se denominan &quot;componentes proxy&quot;, ya que no necesitan contener nada y sirven principalmente para definir la versión de un componente que se va a utilizar en el sitio. Sin embargo, al personalizar los componentes [principales](customizing.md), estos componentes proxy desempeñan un papel esencial en el marcado y la personalización lógica.

Por lo tanto, para cada componente principal que desee utilizar en un sitio, debe:

1. Cree un componente proxy correspondiente en la carpeta de componentes del sitio.

   **Ejemplo** En `/apps/my-site/components` Crear un nodo de título de tipo `cq:Component`

1. Seleccione la versión correspondiente del componente principal con el supertipo.

   **Ejemplo** Agregar la siguiente propiedad:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina el grupo, el título y la descripción opcional del componente. Estos valores son específicos del proyecto y dictan cómo se expone el componente a los autores.

   **Ejemplo** Agregar las siguientes propiedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por ejemplo: observe el componente de [título del sitio](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml)de referencia We.Retail, que es un buen ejemplo de un componente proxy creado de esa manera.

## Carga de los estilos principales {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. Si aún no lo ha hecho, cree una biblioteca [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) clientes que contenga todos los archivos CSS y JS necesarios para su sitio.
1. En la biblioteca de clientes de su sitio, agregue las dependencias a los componentes principales que podrían ser necesarias. Esto se realiza agregando una `embed` propiedad.

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

Los pasos siguientes se realizan en el Editor [de plantillas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. En el Editor de plantillas, seleccione el contenedor de diseño y abra su política.
1. En la lista de componentes permitidos, seleccione los componentes proxy creados anteriormente, que deben aparecer en el grupo de componentes asignado a ellos. Una vez realizados, aplique los cambios.
1. Opcionalmente, para los componentes que tienen un cuadro de diálogo de diseño, se pueden preconfigurar.

¡Eso es todo! En las páginas creadas a partir de la plantilla editada, ahora debe poder utilizar los componentes recién creados.

**Consulte lo siguiente:**

* [Personalización de componentes](customizing.md) principales: para aprender a diseñar y personalizar los componentes principales.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
