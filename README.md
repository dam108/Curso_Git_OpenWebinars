# Curso_Git_OpenWebinars
repositorio para el curso online Git de la plataforma OpenWebinars

# areas
working directory - area de trabajo
staging - area de preparación 
commit - area de salvado

# Comandos basicos de inicializacion

git init - crear el repositorio en local

git status - visualizamos el area en el que estan los ficheros

git add <archivo> - añadir los ficheros al area de preparacion

git commit [-m "mensaje de la revision"] - nos permite hacer un commit ( hacer una instantanea del archivo y mandarlo al area de salvado).

git log --oneline - nos el registro de los guardados en una columna con su identificador ( hash ID )

## Comandos de manipulacion
git rm <fichero> - borrar un fichero y lo agrega al area de preparacion
  
git mv <fichero> - renombrar un fichero y lo agrega al area de preparacion

## Comandos de comparacion 
git diff - nos muestra la diferencia entre un archivo que estaba en el area de trabajo con el area de preparacion.

git diff --staged - compara la diferencia entre el area de preparacion y el area de salvado

git difftool - nos abre la herramienta grafica de comparacion de diferencias

git show <hashID> - nos muestra lo que habia justo en esa revision

### git log
git log --oneline - nos el registro de los guardados en una columna con su identificador ( hash ID )

git log --pretty=[format]:"%h %an %ar - %s" - nos muestra hashID, autor, tevision y tiempo de la revision

## Comandos de configuracion personal 
git config --global user.email "tu@emai.com"

git config --global user.name "tu nombre"

## Comandos para aprobar cambios
git add . - nos incluye todos los ficheros que esten el el area de trabajo al area de preparacion

git reset HEAD <archivo> - saca el fichero del area de revision

# Ficheros
.gitignore - fichero para crear una mascara en donde se indican los ficheros que se añaden en un salvado o no

# Comandos para trabajo en remoto 
git remote add origin <url> - para vincularse con un respositorio (la etiqueta origin se utiliza por convencion para referirse a algo remoto
  
git fetch origin - recuperar lo que hay en origen ( en el repositorio anteriormente añadido)

git branch -v -a - Nos dice las ramas disponibles en origin

git pull origin master - nos descargamos el repositorio

git clone <url> - nos inicializa en el directorio donde estamos el repositorio local y clona el repositorio que esta en remoto
  
git clone <url> . - es lo mismo que el anterior pero coje los archivos y los copia en el path actual
  
git push origin master - con este comando despues de introducir las credenciales del repositorio y lo sube al repositorio remoto

# Comandos de manipulacion de revisiones
## para recuperar desde el working directory lo que hay en el area de commit 8

git checkou master - para traer de la rama master la revision 

git checkout -- master - para traer el archivo master la revision 

git checkout -- . - para traer un grupo de archivos de la revision 

git checout [HEAD] <fichero> - para traer algo de una revision concreta (si utilizamos HEAD estamos referenciando el hash de la ultima revision)

## para recuperar desde el working directory lo que hay en el area de staging (preparacion)

git reset HEAD <archivo> - para recuperar un archivo que esta en el area de preparacion
  
## para recuperar lo que hay en el area de commit pero borrando lo que hay en el area de preparacion

git reset --hard HEAD~1 - este comando recupera el ultimo ante penultimo commit ( HEAD~1 ) y borra lo que hay en el area de preparacion (TENER CUIDADO CON EL )

## Comando para revertir los cambios de una revision

git revert <hashID> - con este comando revertimos los cambios commiteados a una revision con ese hash ID
  
git revert HEAD...HEAD~2 --no-edit - revertimos todos los cambios en una franja de revisiones( con el no-edit no se nos pregunta el porque , se revierte y punto )

  



