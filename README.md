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

