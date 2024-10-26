![repo size](https://img.shields.io/github/repo-size/E7OY/GIT)

# GIT CHEAT SHEET

![LogoGit.](https://git-scm.com/images/logos/downloads/Git-Logo-2Color.svg)


## Índice

* [Áreas de trabajo de Git](#areas-de-trabajo-de-git)
* [Crear repos](#crear-repos)
* [Cambios Repos](#cambios-repos)
* [Mover y Reubicar Archivos](#mover-y-reubicar-archivos)
* [Guardar cambios](#guardar-cambios)
* [Historial commits](#historial-commits)
* [Rehacer commits](#rehacer-commits)
* [Sincronizar cambios](#sincronizar-cambios)


##  ÁREAS DE TRABAJO DE GIT

> | **Area** | **Descripción** |
> | --- | --- |
> | Directorio de trabajo (Working directory) | Carpeta donde se encuentran los archivos de tu proyecto. Aquí es dónde traabajas activamente con los archivos, modificándolos, eliminándolos o añadiendo nuevos. |
 >| Área de preparación (Staging area) | Conocida como índice, área intermedia dónde se colocan los cambios que deseas incluir en el próximo commit, cuando se usa `git add`, se están moviendo los cambios desde el directorio de trabajo a esta área. Los archivos en el índice están listos para ser confirmados (comitted). |
> | Repositorio (Repository) |  Dónde se almacena el historial de todos los commits del proyecto. Cuando se hace un `git commit` se mueven los cambios desde el área de preparación al repositorio. |




## **CREAR REPOS**

| **Comando** | **Descripción** |
| --- | --- |
| `git init [nombreRepo]` | Crea un repositorio local con el nombre especificado, con todos los archivos necesarios para el seguimiento de versiones. |
| `git clone [urlRepo]` | Crea una copia local de un repositorio remoto de Git con la URL especificada. |

---

## **CAMBIOS REPOS**

| **Comando** | **Descripción** |
| --- | --- |
| `git status`  | Muestra el estado del directorio de trabajo.|
| `git diff`  | Muestra las diferencias entre los cambios del directorio de trabajo y el área de preparación.  |
| `git diff --staged` | Muestra las diferencias entre los archivos en el área de preparación y la última versión del archivo. |
| `git add [fileName]`  | Añade un archivo específico al área de preparación. |
| `git add .`   | Añade todos los cambios y archivos en el directorio de trabajo al área de preparación. :warning: Úsalo con precaución ya que puede incluir archivos no deseados. |
| `git reset [fileName]`   | Deshace los cambios en el área de preparación para el archivo especificado, devolviéndolo al estado del último commit. |
| `git commit -m [commitMessage]`  | Confirma los cambios del área de preparación con un mensaje de confirmación. |

---

## RAMAS

| **Comando** | **Descripción** |
| --- | --- |
| `git branch`  | Enumera todas las ramas del repositorio actual. |
| `git branch [nombreRama]`  | Crea una nueva rama con el nombre especificado. |
| `git checkout [nombreRama]`  | Cambia a la rama especificada. |
| `git merge [nombreRama]`  | Fusiona los cambios de la rama especificada con la rama actual. |
| `git branch -d [nombreRama]`  | Borra la rama especificada. |

---

## MOVER Y REUBICAR ARCHIVOS

| **Comando** | **Descripción** |
| --- | --- |
| `git rm [nombreArchivo]` | Borra el archivo especificado del sistema de archivos y del índice de Git. |
| `git rm --cached [nombreArchivo]` | Retira el archivo especificado del control de versiones, pero lo preserva a nivel local. |
| `git mv [nombreArchivo] [nuevoNombreArchivo]` | Cambia el nombre del archivo especificado. |

---

### GUARDAR CAMBIOS

| **Comando** | **Descripción** |
| --- | --- |
| `git stash` | Almacena temporalmente los cambios no confirmados en una pila stash limpiando el área de trabajo sin necesidad de hacer un commit. |
| `git stash pop` | Restaura los archivos guardados del último stash. |
| `git stash list` | Enumera todos los stashes guardados con un identificador único. |
| `git stash drop [stash@{n}]` | Elimina stash de cambios especificado en el índice n. |

---

## HISTORIAL COMMITS

| **Comando** | **Descripción** |
| --- | --- |
| `git log` | Enumera el historial de commits de la rama actual. |
| `git log --oneline` | Muestra el historial en una sola línea por commit, mostrando solo el hash corto y el mensaje del commit. |
| `git log -n x` | Muestra solo los últimos x commits. |
| `git log --grep = [palabraCommit]` | Muestra solo los commits que contienen la palabra "palabraCommit" en el mensaje del commit. |
| `git log --author = [nombreAutor]` | Muestra solo los commits hechos por un autor específico. |
| `git log --follow [nombreArchivo]` | Muestra el historial de commits de un archivo específico incluyendo los cambios de nombre de este. |
| `git diff [primeraRama]...[segundaRama]` | Muestra las diferencias de contenido entre dos ramas. |
| `git show [commit]` | Muestra la información detallada sobre un commit específico pasándole como parámetro el hash o identificador del commit. |

---

## REHACER COMMITS

| **Comando** | **Descripción** |
| --- | --- |
| `git reset [commit]` | Deshace todos los commits después del commit especificado, preservando los cambios localmente. |
| `git reset --hard [commit]` | Reestablece completamente todo el repo al estado exacto del commit especificado, eliminando cualquier cambio posterior. |
| `git log -n x` | Muestra solo los últimos x commits. |

---

## SINCRONIZAR CAMBIOS

| **Comando** | **Descripción** |
| --- | --- |
| `git fetch [nombreRepo]` | Descarga los cambios del repo remoto especificado, sin integrarlos en la rama actual, permitiendo inspeccionar los cambios entes de unirlos al área de trabajo. |
| `git merge [nombreRama]` | Combina los cambios de la rama actual con la rama especificada. |
| `git push [nombreRepoRemoto] [nombreRamaRemota]` | Envía los commits locales a un repositorio remoto. |
| `git pull` | Actualiza el repo local con los cambios del repo remoto. Combina los comandos git fetch(descarga cambios del repo remoto) y git merge(combina los cambios a la rama actual) |

