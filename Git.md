# Comandos Git

## configuración de globales

```bash
git config --global user.name "username"
git config --global user.email "email@dot.com"
```

cuando al hacer `git init` se crea la rama Master, hay que cambiarse a la rama main
`git branch -M main`

|              Comando              | Descripción                                                     |
| :-------------------------------: | :-------------------------------------------------------------- |
|           `git status`            | Muestra el estado de trazabilidad los ficheros                  |
|  `git add <file>` o `git add .`   | Agrega el archivo al grupo que se enviaran a git                |
|     `git commit -m "message"`     | Realizamos el encapsulado de ficheros que se guardaran en stage |
|             `git log`             | Muestra los registros de los commit realizados por los usuarios |
|      `git push origin main`       | Guardamos la version en git                                     |
|         `git clone <url>`         | Clona un repositorio                                            |
|     `git clone <url> carpeta`     | Clona en una carpeta específica                                 |
| `git clone --branch <rama> <url>` | Clona solo una rama                                             |
|    `git clone --depth 1 <url>`    | Clona solo el historial reciente (útil para repos grandes)      |

> Si tenemos detalles con la rama y tenemos un
> **HEAD detached at 07f368b
> nothing to commit, working tree clean**
> basta con realizar un **_git checkout main_** para regresar a la rama head

## CHECKOUT AND RESET

> Permite cambiarnos al origen. Al realizar un **_git checkout file.ext_** regresamos al inicio del ultimo pull.

> De misma forma podemos realizar el git reset **_git reset_**, y este regreara los archivos que han sido modificados, para asi poder regresarlos al inicio con el **_git checkout file.ext_**.
