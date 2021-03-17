# Notas GIT

## Instalar en ubuntu
'''sudo apt install git'''

##   Instalar en debian, redhat, centOS
sudo yum install git

## Instalar en windows`
Descargar de http://git-scm.com/

### MarkDown (.md)


## Crear respositorio GIT
Ejecutar comando dentro de la carpeta RAIZ
```git init```


## Dentro de GIT
Tenemos la carpeta con nuestro código /home/ubuntu/environment/curso
Hay una carpeta con el respositorio /home/ubuntu/environment/curso/.git

- Que hay en mi carpeta de mi codigo?
El codigo fuente de mi aplicación, en su última versión en la rama en la que me encuentre

- Que hay en mi repositorio?
El codigo fuente de mi aplicación, en todas sus vresiones en todas las ramas
Los fichreos los llevaremos de nuestra carpeta al repo, o al reves
La carpeta de mi codigo es lo que en git se denomina WORKSPACE

En GIT hay una cosa más en medio.. AREA DE STAGING

WORKSPACE               AREA DE STAGING                         REPO (carpeta .git)
----------------->>>>>>>----------------------------------->>>>>------------
fichreros 
en directorios                                                  Commits (paquetes de código sellado)

## Almacenar credenciales remotas en GIT
- Ejecutar $ git config credential.helper store
- Ejecutar $ git config --global credential.helper store
- Realizar un push o pull para que se almacenen automaticamente las credenciales



## Comandos GIT
### - git init
Crea un repositorio

### - git status
Nos da el estado del workspace

### - git add
Marcar un archivo / directorio para seguimiento.
Por defecto trabaja de forma recursiva

- git add NOMBRE_FICHERO
- git add NOMBRE_CARPETA
- git add *
- git add . (añade archivos / carpetas ocultas)

### - git rm --cached
Saca un fichero del STAGING 
Hace que los ficheros deje de estar controlado por el SCM

### - git rm 
Elimina el fichero:
- De mi carpeta local: WORKSPACE
- Del área de STAGING
- Del REPOSITORIO en la versión actual

### - git commit -m "mensaje confirmacion"
Indica al SCM que guarde el paquete de cambios en el REPOSITORIO

### - git commit ammedn --reset-autor
Hace un commit reescribiendo los comentarios

### - git commit --all -m "mensaje"
Añade al stating y hace el comit directamente pero solo de los archivos que estan ya en el reposittorio


### - git config --global user.name "Iván Díaz"
Cambie el nombre del usuario

### - git config --global user.email i.diaz@ibermatica.com
Email del usuario

### - git reset --hard 
Restaura el WORKSPACE completamente (ojo se pueden perder cambios locales en workspace)

### - git branch 
Obtiene informacion de la rama actual

### - git branch NOMBRE_RAMA
Crea una rama nueva

### - git checkout NOMBRE_RAMA
Cambia el workspace a la rama indicada

### - git checkout -b NOMBRE_RAMA
Crea la rama y cambia el workspace a la rama indicada
Reemplaza todos los ficheros

### - git ls-files
Lista los archivos en el repositorio GIT


### - git merge "rama a traer"
Trae los datos de una rama a la rama en la que stamos actualmente

### - git stash save "aqui me he quedado"
Guarda en el stash "diretorio temporal" el estdo actual de la rama en la que estamos
Solo los archivos controlados por SCM

### - git stash list
Lista los stash que tenemos en la rama

### - git stash pop
Saca el ultimo stash y lo pone en la rama actual

### - git stash branch 
Crea una nueva rama desde la rama actual añadiendo los cambios que hay en el stash

### - git remote
Lista los recursos remotos existentes

### - git remote add github https://github.com/diazalmazan/cursoGIT_proyecto1.git
Añade un repositorio externo

### - git push github
Envia los cambios en el repostiorio (commit) al repositorio remotos

### - git fetch
Sincroniza el repositorio local con el repositorio remotos

### - git pull 
Obtiene los datos del repositorio y actualiza el repositorio local y el workspace

