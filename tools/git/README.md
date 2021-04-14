# Git Cheat Sheet

### Configuración

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git config --list`      | Enlista la configuración de git       |
| `git config --list --show-origin`      | Enlista donde esta ubicado la configuración de git       |
| `git config --global user.name "[firstname lastname]"`      | Establecer un nombre que sea identificable en el historial de versiones       |
| `git config --global user.mail "[valid-email]"`      | Establecer una dirección de correo electrónico que se asociará con cada marcador del historial       |

### Inicializar

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git init`      | Inicializar       |

### Repositorio remoto

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git remote add origin <URL>`      | Agrega un origen remoto de nuestros archivos       |
| `git remote`      | Muestra el origen remoto que se tiene       |
| `git remote -v`      | Muestra el origen remoto de manera verbal       |
| `git clone <URL>`      | Descarga la version del proyecto del sitio remoto       |
| `git pull`      | Traerse todo los archivos del sitio remoto       |
| `git push origin <BranchName>`      | Publicar una la rama al sitio remoto       |
| `git remote add upstream <URL>`      | Crea una nueva rama o fuente de datos remotos       |

### Stage y Snapshot

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git status`      | Muestra las modificaciones y cosas que aún no están preparadas        |
| `git add <file>`      | Agrega el archivo a git       |
| `git add .`      | Agrega todos los archivos que hayan cambiado en la carpeta que estoy posicionado       |
| `git commit -m "<descriptive message>"`      | Manda los ultimos cambios a la BD del control de cambios. El -m "Mensaje" Coloca un mensaje sobre el cambio       |

### Inspeccionar y Comparar

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git status`      | Muestra las modificaciones y cosas que aún no están preparadas        |
| `git diff <branchA> <branchB>`      | Ver la diferencia entre una versión y otra       |
| `git diff <oldID newID>`      | Mostrar cambios entre commits, commit y working tree       |
| `git log`      | Mostrar los logs de los commits       |
| `git log --stat`      | Revisa los cambios especificos en cada archivo a apartir del primer commit       |
| `git log --all --graph --decorate --oneline`      | Enlista los cambios pero de forma mas grafica como en ramas de todos los cambios       |
| `git log --online`      | Coloca los cambios como tipo enlistado       |
| `git show <IDcommit>`      | Muestra uno o más objetos (blobs, trees, tags and commits)       |
| `git tag -l`      | Muestra todos los tags       |

### Deshacer commits

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git reset <IDcommit> --hard`      | Reestablecer al ultimo commit        |
| `git revert <BranchName>`      | Reestablecer al ultimo commit        |
| `git checkout <IDcommit> <file>`      | Vuelve a cualquier version anterior de un archivo en especifico o incluso del proyecto entero        |
| `git rebase <BranchName>`      | Aplicar las confirmaciones de la rama actual antes de la especificada         |
| `git commit --amend`      | Primero hay que añadir los cambios con el commit add, luego ejecutar el comando y con esto lo que hace es fusionar los cambios que se hicieron primero con lo ultimo y no genera otro commit. Esto se hace si nos equivocamos al mandar un commit         |

### Branches

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git branch`      | Listar ramas existentes        |
| `git branch -a`      | Listar branches locales y remotas        |
| `git branch -r`      | Listar las ramas existentes remotas        |
| `git branch <BranchName>`      | Crea una rama        |
| `git branch -b <BranchName>`      | Crea una rama y cambiar a la rama        |
| `git checkout <BranchName>`      | Cambiar de rama        |
| `git checkout -m <BranchName>`      | Renombrar una rama        |
| `git branch -D <BranchName>`      | Elimina una rama        |
| `git branch origin :<BranchName>`      | Elimina una rama remota        |
| `git merge <branch>`      | Fusiona las ramas        |
| `git push origin <BranchName>`      | Publicar una la rama al sitio remoto       |

### Tags

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git tag`      | Listar los tags de nuestro repositorio local        |
| `git tag -a <TagName> - m "<Message>" <IDCommit>`      | Crear un nuevo tag y asignarlo a un commit        |
| `git tag -d <TagName>`      | Borrar un tag en el repositorio local        |
| `git checkout <TagName>`      | Cambiar a un tag existente        |
| `git push origin --tags`      | Publicar un tag en el repositorio remoto        |
| `git pull --tags`      | Traer tags remotas        |

### Commits Temporales

| Comando| Uso                    |
| ------------- | ------------------------------ |
| `git stash`      | Guarda en memoria los cambios y vuelve a estado anterior        |
| `git stash list`      | Enlista los stash que se tienen en memoria        |
| `git stash pop`      | Coloca los cambios guardados previamente en memoria        |
| `git stash branch <BranchName>`      | Crea una rama y coloca los cambios guardados previamente en memoria en la rama nueva        |
| `git stash drop`      | Elimina el stash guardado en memoria        |

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)