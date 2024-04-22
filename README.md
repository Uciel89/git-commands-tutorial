# git-commands-tutorial
Tutorial inicial de git - github / Comandos basicos y versioando 🌱

## Programas instalados previamente 👀
> [GIT](https://git-scm.com/downloads)

> Algun entorno de desarrollo, ejemplo: [VSCode](https://code.visualstudio.com/download) (opcional)

## Comandos basicos 🏗️
### Inicializar un repositorio local en un proyecto
Inicializamos una instancia de un repositorio remoto dentro de nuestro proyecto
```bash
git init 
```
Agregamos todos nuestros archivos dentro del respositorio local.
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
Subimos el ultimo commit que generamos al repositorio remoto
```bash
git push origin nombre-rama
git push origin master
```
## Flujo de comandos para versiones 📒
Ejecutamos los mismos comandos que al momento de inicializar nuestro repositorio local
```bash
git add .
git commit  -m "Actualización de repositorio"
```
Vamos a generar nuestro tag o etiqueta que representara a nuestro versión
```bash
git tag -a indicamos-versión -m "Descripción de la versión"
git tag -a v1.0 -m "v1.0"
```
Para indicar a nuestra vesión que tome las ultimas configrmaciónes de nuestro repositorio local
> -f significa que vamos a ejecutar el comando de forma forzada
```bash
git tag indicamos-version -f 
```
Por ultimo vamos a subir esta etiqueta a nuestro repositorio remoto para por fin tener nuestras **versiones**
```bash
# Primero actualizamos nuestra rama principal
git push origin master

# Segundo enviamos los mismo cambios pero dentro de nuestra etiqueta
# (la primera vez lo generara)
git push origin v1.0
```

## Documentación oficial de GIT 😺

[Link de la documentación](https://git-scm.com/doc)

## Material extra 📖
### Metodologia GIT FLOW

[Link a la pagina oficial](https://danielkummer.github.io/git-flow-cheatsheet/index.es_ES.html)
