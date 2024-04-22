# git-commands-tutorial
Tutorial inicial de git - github / Comandos básicos y versionado 🌱

## Requisitos previos 👀
Tener creada una cuenta y un repositorio en GitHub

[Link de como creaer una cuenta de GitHub](https://docs.github.com/es/get-started/start-your-journey/creating-an-account-on-github)

[Link de como creaer un repositorio en GitHub](https://docs.github.com/es/repositories/creating-and-managing-repositories/quickstart-for-repositories)
### Programas necesarios
* [GIT](https://git-scm.com/downloads)

* Algun entorno de desarrollo, ejemplo: [VSCode](https://code.visualstudio.com/download) (opcional)


## Comandos básicos 🏗️

### Configurar un usuario, mail y password dentro de nuestro sistema (opcional)
```bash
git config user.email "email@ejemplo.com" 
git config user.name "nombre" 
git config user.password "token de seguridad"
```
> **Importante!!**Al momento de realizar un git pull a un repositorio tanto privado como público si es que no hemos configurado un usuario, mail y token nos va a aparecer una ventana emergente que nos pedirá iniciar sesión o ingresar un token. Si tienen un token generado, usen la segunda opción si no la primera que te permite loguearte con una cuenta de github directamente.

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

## Flujo para actualizar una versión específica (opcional)
> git checkout -> Nos permite movernos entre las diferentes ramas dentro de nuestro repositorio local
```bash
# Traemos los ultimos cambios (por si es que no teníamos actualizado el tag)
git pull origin v1.0

# Creando una rama temporal con el estado del proyecto de una versión
git checkout v1.0

# Añadimos y agregamos un commit con los cambios específicos
git add .
git commit -m "nombre-del-commit"

# Actualizamos nuestra versión con el último commit que acabamos de crear
git tag v1.0 -f

# Enviamos los cambios a nuestro repositorio
git push origin v1.0 -f

# Eliminamos esta rama temporal
git switch -
```

### Comandos extras pero *importantes* ✍🏼
1. Nos permite clonar un repositorio
   
   ```bash
   git clone url-repo
   ```  
3. Conocer la rama en la que estoy
   
   ```bash
   git branch
   ```

   * Crear una nueva rama
     
     ```bash
      git branch new_branch
     ```
   * Eliminar una rama
     
     ```bash
     git branch -D new_branch
     ```

3. Nos permite movernos de una rama a otra y también genera una rama si es que ya no existe
   
   ```bash
    git checkout new_brach
    ```

5. Nos permite funcionar una rama con otra. En la siguiente imagen se ve como se fucion la rama feature con nuestra rama principal (main o master)

![img-merge](https://media.geeksforgeeks.org/wp-content/uploads/20230519161317/git-merge-dev.png)

```bash
git merge feature
```
> Importante!! Al ejecutar el siguiente comando se va a funcionar todo el contenido de la rama que mencionamos dentro del comando con la rama en la que estemos parados. Para comprar en qué rama estamos ejecute el comando `git branch`

## Documentación oficial de GIT 😺

[Link de la documentación](https://git-scm.com/doc)

[Link de documentación alternativa (Explicación mas visual)](https://www.atlassian.com/es/git)

## Material extra 📖
### Metodología GIT FLOW

[Link a la pagina oficial](https://danielkummer.github.io/git-flow-cheatsheet/index.es_ES.html)

