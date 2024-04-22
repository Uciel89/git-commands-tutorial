# git-commands-tutorial
Tutorial inicial de git - github / Comandos básicos y versionado 🌱

## Programas instalados previamente 👀
> [GIT](https://git-scm.com/downloads)

> Algun entorno de desarrollo, ejemplo: [VSCode](https://code.visualstudio.com/download) (opcional)

## Comandos básicos 🏗️

### Configurar un usuario, mail y password dentro de nuestro sistema (opcional)
```bash
git config user.email "email@ejemplo.com" 
git config user.name "nombre" 
git config user.password "token de seguridad"
```
### Inicializar un repositorio local en un proyecto
Inicializamos una instancia de un repositorio remoto dentro de nuestro proyecto
```bash
git init 
```
Agregamos todos nuestros archivos dentro del repositorio local.
```bash
git add . 
```
Indicamos todos los cambios que vamos a realizar dentro de nuestro repositorio local bajo un nombre
```bash
git commit -m "nombre del commit" 
```

### Vinculamos un repositorio remoto a nuestro repositorio local
Indicamos todos los cambios que vamos a realizar dentro de nuestro repositorio local bajo un nombre
```bash
git remote add nombre-vinculo url-repo
git remote add origin https://github.com/Uciel89/git-commands-tutorial.git
```
### Subimos nuestro proyecto / cambios a nuestro repositorio remoto
Subimos el último commit que generamos al repositorio remoto
```bash
git push origin nombre-rama
git push origin master
```
## Flujo de comandos para versiones 📒
![img-tag](https://miro.medium.com/v2/resize:fit:1400/1*34EO-6Ra2ath8-p4iBQBRQ.png)
Ejecutamos los mismos comandos que al momento de inicializar nuestro repositorio local
```bash
git add .
git commit  -m "Actualización de repositorio"
```
Vamos a generar nuestro tag o etiqueta que representará a nuestro versión
```bash
git tag -a indicamos-versión -m "Descripción de la versión"
git tag -a v1.0 -m "v1.0"
```
Para indicar a nuestra visión que tome las últimas confirmaciones de nuestro repositorio local
> -f significa que vamos a ejecutar el comando de forma forzada
```bash
git tag indicamos-version -f 
```
Por último vamos a subir esta etiqueta a nuestro repositorio remoto para por fin tener nuestras **versiones**
```bash
# Primero actualizamos nuestra rama principal
git push origin master

# Segundo enviamos los mismo cambios pero dentro de nuestra etiqueta
# (la primera vez lo generara)
git push origin v1.0
```

## Flujo para actualizar una versión especifica (opcional)
> git checkout -> Nos permite movernos entre las diferentes ramas dentro de nuestro repositorio local
```bash
git pull origin v1.0
git checkout v1.0
git add .
git commit -m "nombre-del-commit"
git tag v1.0 -f
git push origin v1.0 -f
git switch -
```

### Comandos extras pero *importantes* ✍🏼
```bash
# Nos permite clonar un repositorio
git clone url-repositorio
# Nos permite saber en que rama estamos 
git branch
  # Crear una nueva rama
  git branch new_branch
  # Eliminar una rama
  git branch -D new_branch
# Nos permite movernos de una rama a otra y tambien genera
# una rama si es que ya no existe
git checkout new_brach 
```
## Documentación oficial de GIT 😺

[Link de la documentación](https://git-scm.com/doc)

## Material extra 📖
### Metodología GIT FLOW

[Link a la pagina oficial](https://danielkummer.github.io/git-flow-cheatsheet/index.es_ES.html)
