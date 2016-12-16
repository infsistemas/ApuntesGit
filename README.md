# Índice

Ayuda para crear el TOC de forma automática con SublimeText:

https://github.com/naokazuterada/MarkdownTOC

* Clientes de Windows gratuitos
** Pruebas con smartgit
** Pruebas con SourceTree
* Configurar Synology para ser un Servidor Git


# Clientes de Windows gratuitos

* SmartGit
* SourceTree

## Pruebas con smartgit

Pasos que he seguido con SmartGit (una utilidad GUI para windows):

1.- Instalar SmartGit en versión para uso no comercial.

2.- Crear repositorio local desde el menú superior: Repository > Add o Create... y seleccionando una carpeta de nuestro sistema ficheros.

3.- Añadir ficheros de texto de prueba en nuestra carpeta local que ahora es un repositorio Git.

4.- En la parte inferior izda, ventana de Branches, usar "Push to" para conectarnos a nuestro repositorio remoto en GitHub. Dicho repositorio debe crearse también previamente desde la web de GitHub.

5.- Una vez añadido el repositorio remoto, ya podemos hacer commit de los ficheros locales al repositorio remoto en GitHub.

6.- Si añadimos más ficheros en local, y modificamos algunos directamente en GitHub, cuando hagamos commit no podremos porque hay diferencias en el repositorio remoto. Para solucionarlas tendremos que hacer un Pull (un checkout para los que venimos de SVN), o un SYNC (para sincronizar los dos extremos), y finalmente podremos hacer un commit cuando los dos repositorios local y remoto estén iguales.

7.- Al mismo, cada vez que hacemos cambios en local, SmartGit los detecta y nos lo muestra en la ventana Files. Haciendo Commit actualizamos el repositorio local, y haciendo un "Push to" desde la rama "master" los subimos al servidor remoto.

## Pruebas con SourceTree

Con este cliente conseguí conectarme a mi repositorio remoto Synology.

# Configurar Synology para ser un Servidor Git

1.- Instalar Servidor Git

2.- Crear Repositorio desde SSH con el comando:

> mkdir /volumen/git/mirepo

> git init --bare --shared

3.- Para conectarnos al repositorio, la url de este será:

> ssh://username@[ip_synology]/ruta_repositorio

Ejemplo:

> ssh://username@diskstation/volumen/git/mirepo