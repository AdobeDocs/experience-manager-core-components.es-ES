---
title: Uso de componentes principales
seo-title: Uso de componentes principales
description: nulo
seo-description: '" Para empezar a utilizarlo con componentes principales en su propio proyecto, siga estos pasos: descargue e instale, cree componentes proxy, cargue los estilos principales y permita los componentes de las plantillas. "'
uuid: a 1 ef 2 acf -8226-4510-838 b-f 5 fae 196 f 9 f 1
contentOwner: Usuario
content-type: referencia
topic-tags: desarrollar
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 1703 a 171-830 c -477 e-a 34 f -99 caba 841 ec 4
disttype: dist5
gnavtheme: claro
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Uso de componentes principales{#using-core-components}

Para ponerse en marcha con [componentes principales](developing.md) en su propio proyecto, hay cuatro pasos, que se detallan individualmente en las secciones siguientes:

1. [Descarga e instalación](#download-and-install)
1. [Crear componentes Proxy](#create-proxy-components)
1. [Cargar los estilos principales](#load-the-core-styles)
1. [Activar componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obtener instrucciones más amplias sobre cómo empezar desde cero con la configuración del proyecto, los componentes principales, las plantillas editables, las bibliotecas cliente y el desarrollo de componentes, puede ser interesante el siguiente tutorial de varias partes:\
>[Introducción a sitios AEM - Tutorial de WKND](wknd-tutorial.md)

## Descarga e instalación {#download-and-install}

Una de las ideas que impulsan los componentes principales es la flexibilidad. Lanzar nuevas versiones de los componentes principales con mayor frecuencia permite a Adobe ser más flexible en la entrega de nuevas funciones. Los desarrolladores pueden ser flexibles en los componentes que elija integrar en sus proyectos y en la frecuencia con que desean actualizarlos.

Por este motivo, los componentes principales no forman parte del inicio rápido al comenzar en modo de producción (sin contenido de muestra). Por lo tanto, su primer paso es [descargar el último paquete de contenido publicado desde github](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalarlo en los entornos de AEM.

Existen varias formas de automatizar esto, pero la manera más sencilla de instalar rápidamente un paquete de contenido en una instancia es mediante el Administrador de paquetes; Consulte [Instalación de paquetes](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). Asimismo, una vez que tenga una instancia de publicación en ejecución, tendrá que replicar dicho paquete en el editor; Consulte [Replicación de paquetes](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Crear componentes Proxy {#create-proxy-components}

Por motivos explicados en la [sección Patrón](guidelines.md#proxy-component-pattern) de componente proxy, los componentes principales no se deben hacer referencia directamente desde el contenido. Para evitar esto, todos pertenecen a un grupo de componentes ocultos ( `.core-wcm` o `.core-wcm-form`), lo que impide que se muestren directamente en el editor.

En su lugar, se deben crear componentes específicos del sitio que definan el nombre y el grupo que desee para mostrar a los autores de páginas, y hacer referencia a cada uno de ellos a un componente principal como supertipo. Estos componentes específicos del sitio se denominan a veces «componentes proxy» porque no necesitan contener nada y sirven principalmente para definir la versión de un componente que se utilizará en el sitio. Sin embargo, al personalizar los componentes [](customizing.md)principales, estos componentes proxy juegan un papel esencial en la personalización y la personalización de la lógica.

Así pues, para cada componente principal que desee utilizar para un sitio, debe:

1. Cree un componente proxy correspondiente en la carpeta de componentes del sitio.

   **Ejemplo**
bajo `/apps/my-site/components` creación de un nodo de título de tipo `cq:Component`

1. Apunte a la versión de componente principal correspondiente con el supertipo.

   **Ejemplo**
Añadir siguiente propiedad:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina el grupo, el título y la descripción del componente. Estos valores son específicos del proyecto y dictan cómo se expone el componente a los autores.

   **Ejemplo**
Agregue las propiedades siguientes:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por ejemplo, observe el [componente de título del sitio de referencia We. Retail](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), que es un buen ejemplo de componente proxy creado de ese modo.

## Cargar los estilos principales {#load-the-core-styles}

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

1. Si aún no lo hace, cree una [biblioteca](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) de cliente que contenga todos los archivos CSS y JS necesarios para su sitio.
1. En la biblioteca de cliente del sitio, agregue las dependencias a los componentes principales que puedan ser necesarios. Esto se realiza agregando `embed` una propiedad.

   Por ejemplo, para incluir las bibliotecas cliente de todos los componentes principales v 1, la propiedad que agregar sería la siguiente:

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

Los pasos siguientes suelen realizarse en el Editor [de plantillas](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html); sin embargo, para las configuraciones existentes, esto puede realizarse en modo Diseño:

1. En el Editor de plantillas (o modo Diseño), seleccione el contenedor de diseño (o parsys) y abra su política (o configuración de diseño).
1. En la lista de componentes permitidos, seleccione los componentes proxy creados anteriormente, que deben aparecer bajo el grupo de componentes asignado a ellos. Una vez realizados, aplique los cambios.
1. Opcionalmente, para los componentes que tienen un cuadro de diálogo de diseño, pueden estar preconfigurados.

Es decir, en las páginas creadas a partir de la plantilla editada, ahora debería poder utilizar los componentes recién creados.

**Siguiente:**

* [Personalización de componentes](customizing.md) principales: para aprender a diseñar y personalizar los componentes principales.
* [Directrices](guidelines.md) de componentes: para conocer los patrones de implementación de los componentes principales.
