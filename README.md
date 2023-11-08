# Estadistica
Estudio de estadística 
Comandos de Git

-> CONFIGURACIÓN

git --version
git config --global user.name "andrespuertag" (la configuración que realicemos va ser global y no por proyecto)
git config --global user.mail andrespuertagonzalez@gmail.com
git config --global user.editor "code --wait" (para indicar que VSC es nuestro editor por defecto. wait es para que la terminal se quede esperando a que cerremos el editor de texto)
git config --global -e (abre el archivo de configuración en VSC)
git config --global core.autocrlf input (input es para mac y true es para windows, hace compatibles los saltos de líneas entre sistemas operativos)

-> COMANDOS

git init (inicializado un repositorio)
ls -a (muestra todos los archivos incluyendo los ocultos)
cd .git (entramos al directorio oculto, si se da ls aparecen todos los archivos que gestionan los repositorios, versiones, ramas etc., es un detalle de implementación)
git status (muestra el estado actual de nuestri repositorio)
git add . (agrega absolutamente todo, pero es una mala practica)
git add .txt (todos los archivos terminados en txt que vamos agregar a nuestra etapa de stage)
git commit -m "mensaje que indica que hiciste" (este comando compromete o commit los archivos en su ultima version)

--> eliminación de archivos
rm archivo.txt
git status (muestra los cambios que no han sido agregados a la etapa de stage)
git status -s (muestra los cambios que no han sido agregados a la etapa de stage)
git add (para adicionar el cambio en stage)
git commit -m "eliminando archivo" (se elimina en commit)

git rm archivo.txt (remueve los archivos de commit, que ahorra un paso anterior)

--> recuperar archivo eliminado
git restore archivo.txt

--> como mover o cambiar el nombre de un archivo

mv archivo.txt archivo1.txt
git add archivo.txt archivo1.txt
git commit -m "renombrando el archvio.txt"

git mv archivo.txt archivo1.txt (paso mas corto)
git commit -m "renombrando el archvio.txt"

--> como ignorar archivos para que no se subaa los repositorios de git

crear un archivo .gitignore y se colocan alli los archivos que se quieren ignorar
git add gitignore
git commit -m "agregando archivo .gitignore"

---

git diff (muestra de una manera mas grafica los cambios que se han realizado
git log (permite ver los cambios)
git log --online (permite ver los cambios pero solo muestra los mensajes"

--> Branch and Merge

git branch (nos dice en que rama estamos)
git checkout -b ramab (crea una nueva rama)
git checkout main (se cambia a la rama principal)
git checkout ramab (se cambia a la ramab)

- para hacer merge se tiene que estar en la rama main

git merge ramab 


-- > subir a la nube

git pull origin main --rebase
git push origin main

Si queremos subir la información a otra rama se debe hacer lo siguiente
git checkout -b ramaA
git push -u origin ramaA
git push
