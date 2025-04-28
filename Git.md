# Comandos Git

## configuración de globales

```bash
git config --global user.name "username"
git config --global user.email "email@dot.com"
```

cuando al hacer `git init` se crea la rama Master, hay que cambiarse a la rama main
`git branch -M main`

|              Comando               | Descripción                                                     |
| :--------------------------------: | :-------------------------------------------------------------- |
|            `git status`            | Muestra el estado de trazabilidad los ficheros                  |
|   `git add <file>` o `git add .`   | Agrega el archivo al grupo que se enviaran a git                |
|     `git commit -m "message"`      | Realizamos el encapsulado de ficheros que se guardaran en stage |
|   `git log` o `git log --graph`    | Muestra los registros de los commit realizados por los usuarios |
| `git log --graph --pretty=oneline` | Muestra los commits en una sola linea                           |
|       `git push origin main`       | Guardamos la version en git                                     |
|         `git clone <url>`          | Clona un repositorio                                            |
|     `git clone <url> carpeta`      | Clona en una carpeta específica                                 |
| `git clone --branch <rama> <url>`  | Clona solo una rama                                             |
|    `git clone --depth 1 <url>`     | Clona solo el historial reciente (útil para repos grandes)      |

> Si tenemos detalles con la rama y tenemos un
> **HEAD detached at 07f368b
> nothing to commit, working tree clean**
> basta con realizar un **_git checkout main_** para regresar a la rama head

## CHECKOUT AND RESET

> Permite cambiarnos al origen. Al realizar un **_git checkout file.ext_** regresamos al inicio del ultimo pull.

> De misma forma podemos realizar el git reset **_git reset_**, y este regreara los archivos que han sido modificados, para asi poder regresarlos al inicio con el **_git checkout file.ext_**.

## Alias

podemos realizar comandos y guardas en un alias...

```
    git config --global alias.tree "log --graph --decorate --all --oneline"

    git tree
```

al realizar el **_git tree_** realizara la accion de listar los commits.

## Gitignore

Todos los archivos que queramos excluir en los commits podemos indicarlos en el archivo _.gitignore_

creamos el archivo `.gitignore` y dentro indicaremos los archivos que no se consideraran en los git add .
una vez agregados los nombres de los archivos, mandamos el gitignore a la rama principal (push)

## DIFF

Ayuda a mostrar en consola los cambios realizados a un archivo.

```bash
--- a/Git.md
+++ b/Git.md
@@ -50,6 +50,5 @@ al realizar el **_git tree_** realizara la accion de listar los commits.

 Todos los archivos que queramos excluir en los commits podemos indicarlos en el archivo _.gitignore_

-creamos el archivo `.gitignore` y dento indicaremos los archivos que no se consideraran en los git add .
-
-> \*\*/Archivo.ignorado
+creamos el archivo `.gitignore` y dentro indicaremos los archivos que no se consideraran en los git add .
+una vez agregados los nombres de los archivos, mandamos el gitignore a la rama principal (push)
```

## RESET HARD

nos ayuda a resetear a una version en especifico, ya sean una o varias versiones anteriores, o posteriores

`git reset --hard <id_commit>`

y con el comando
git reflog podemos revisar los logs de los cambios en las ramas y versiones, un log completo

## TAG

`git tag <nombre>`

con el git log, nos mostrara el la descripcion del head, y si tiene un tag para identificar al commit.
si realizamos un nuevo commit, el tag sigue identificando al commit, por lo que si me quiero cambiar basta con el git checkout tag

Podemos regresar a una version en la que se requiere modificar algo sin tener que borrar otros archivos.

## BRANCH & SWITCH

`git branch nombre_rama`

al revisar los logs podemos ver cuantas ramas existen y el Head dice en que rama se esta trabajando.

para cambiar entre ramas `git swtich nombre_rama`

## MERGE

unir/combinar cambios en un solo

`git merge main`

en caso de conflicto, se debera solucionar y despues se podra realizar el merge, para ello solo se adjunta el cambio.

> Si estamos realilzando cambios a un documento, y necesitamos cambiarnos a otra rama, no permitira, hasta realiazar el commit, sin embargo puede que eso aun este incompleto, porlo que necesitamos solo guardar klocalmente un cambio de esa párte, para ello el comando.

`git stash`
