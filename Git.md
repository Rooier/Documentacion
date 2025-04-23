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
