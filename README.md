# cheatSheets

## GIT CHEAT-SHEET

![LogoGit.](https://git-scm.com/images/logos/downloads/Git-Icon-1788C.svg)

### CREAR REPOS

`git init [nombreRepo]`  
Crea un repositorio local con el nombre especificado

`git clone [urlRepo]`  
Descarga un proyecto remoto a local y toda su historia de versión
 
---

### CAMBIOS REPOS

`git status`  
Muestra el estado del directorio de trabajo.

`git diff`  
Muestra las diferencias entre los cambios del directorio de trabajo y el área de preparación. 

`git diff --staged`  
Muestra las diferencias entre los archivos en el área de preparación y la última versión del archivo.

`git add [fileName]`  
Añade un archivo específico al área de preparación.

`git add .`  
Añade todos los cambios en el directorio de trabajo al área de preparación.  
:warning: Úsalo con precaución ya que puede incluir archivos no deseados.

`git reset [fileName]`
Deshace los cambios en el área de preparación para el archivo especificado, devolviéndolo al estado del último commit.

`git commit -m [commitMessage]`  
Confirma los cambios del área de preparación con un mensaje de confirmación.

---

### CAMBIOS GRUPALES

`git branch`
Enumera todas las ramas del repositorio actual.

`git branch [nombreRama]`  
Crea una nueva rama con el nombre especificado.

`git checkout [nombreRama]`  
Cambia a la rama especificada y actualiza el directorio activo.

`git merge [nombreRama]`  
Fusiona la rama especificada con la rama actual.

`git branch -d [nombreRama]`  
Borra la rama especificada.


---

### MOVER Y REUBICAR ARCHIVOS
