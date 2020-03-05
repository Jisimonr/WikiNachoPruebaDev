
[[_TOC_]]


Cuando creamos un proyecto, no se crea un repositorio Wiki de forma predeterminada. Para comenzar a usar una Wiki, primero debemos crear la. Cada Wiki funciona con un repositorio Git en el back-end de Azure Devops, en el que se almacenan las páginas Markdown, imágenes, archivos adjuntos y la secuencia de páginas y subpáginas.

Los repositorios de la wiki tienen asignadas las siguientes etiquetas:

* Repositorio wiki: ProjectName.wiki.
* Rama maestra: wikiMaster.

El repositorio de Wiki contiene los siguientes archivos y carpetas:

* Archivo para cada página de Markdown.
* Archivo con extensión order en la raíz y debajo de cada carpeta.
* Carpeta para cada página que tiene subpáginas.
* Carpeta attachments que almacenar todos los archivos adjuntos de la Wiki.

Para clonar la wiki desplegamos el menú contextual y seleccione Clonar wiki.

![](/.attachments/Imagen1-86e1bb54-e570-409d-8fe0-01b77b89ed1a.png)

Nos aparecerá la siguiente pantalla:

![](/.attachments/Imagen2-cf615762-bc33-4719-ba25-680050ea2245.png)
 
Pinchando en el icono copiar-clonar obtendremos una URL con el siguiente formato:

```
https://dev.azure.com/<AccountName>/<TeamProjectName>/_git/<WikiName>
```

Esta URL nos permite obtener una copia en local de la wiki. Esta copia nos permitirá añadir páginas o hacer cambios sin tener que acceder a nuestra cuenta de Azure Devops.

El repositorio lo podemos clonar en local con la herramienta Sourcetree o con Git y hacer las modificaciones en notepad++.


Podemos clonar el repositorio mediante git, si lo tenemos instalado. En caso contrario podemos descargar el [instalador de Git](https://git-scm.com/download/win "Pinche para bajar la version windows de Git").

Una vez descargado el instalador de git lo ejecutamos y damos a siguiente hasta que se empiece a instalar.
Después, en el explorador de archivos, nos colocamos en la carpeta en la que queremos clonar el proyecto.
Pinchamos en la pantalla, del explorador, con el botón derecho y en el popput que nos aparece pinchamos en Git Bash Here para llamar a la consola de Git:

![](/.attachments/Imagen3-4106388d-ec4a-4fd1-9929-a19dd1d95a1f.png)

En ella escribiremos git clone y la URL copiada anterioemente:

```
git clone https://dev.azure.com/<AccountName>/<TeamProjectName>/_git/<WikiName>
```

Para poder utilizar Notepad++ como editor de la wiki clonada, tenemos que decírselo a git con el siguiente comando en la consola de git bash.

git config --global core.editor "'Ruta_de_Notepad/notepad++.exe'"

Los push y pull los podemos hacer en la consola o en Sourcetree. Para añadir una página, desde la consola de Git, tendremos que utilizar los comandos:

git add Fichero.md
git commit -m 'Mensaje esplicación commit'
git push

Tenemos información de cómo clonar y actualizar el contenido de la wiki sin conexión, en local, en el enlace:

https://docs.microsoft.com/es-es/azure/devops/project/wiki/wiki-update-offline?view=azure-devops.

Es importante conocer los archivos del repositorio de Wiki Git y la estructura de archivos. Esta información se encuentra en el enlace:

https://docs.microsoft.com/es-es/azure/devops/project/wiki/wiki-file-structure?view=azure-devops.

Modifico esto. Otra vez.

Y otra más
