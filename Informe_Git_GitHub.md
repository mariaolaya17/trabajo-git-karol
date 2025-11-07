# **Informe de Git y GitHub**

##  ¿Qué es Git?

Git es un **sistema de control de versiones distribuido** creado por *Linus Torvalds*.  
Se diseñó para que los programadores puedan trabajar de forma eficiente, segura y rápida en proyectos, guardando el historial de cambios y permitiendo volver atrás si algo sale mal.

---

## Instalación de Git

Para descargar Git se entra a la página oficial:  
[https://git-scm.com/](https://git-scm.com/)

Ahí se da clic en **“Download for Windows”**, luego en **“Click here to download”**, y comenzará la descarga del instalador.  
Solo hay que seguir los pasos del asistente y presionar **Install → Finish** cuando termine.  
Listo, ya tienes Git en tu PC.

![pagina oficial de git](./pagina%20oficial%20de%20git.PNG)
![download windows](./download%20windows.PNG)
![instalador del git](./instalador%20del%20git.PNG)
![instalando](./instalando.PNG)

## Configuración inicial

Una vez instalado, abrimos la **terminal de Git Bash**.  
Antes de usarlo, hay que configurarlo con nuestro nombre y correo (estos datos aparecerán en cada commit):

```bash
git config --global user.name "TuNombre"
git config --global user.email "tu@email.com"
```
![usuario y correo](./usuario%20y%20correo.PNG)

Para confirmar:
```bash
git config --list
```
![git config list](./git%20config%20list.PNG)

---

## Comandos básicos de consola


 `ls`  Muestra los archivos y carpetas del directorio actual. 
![ls](./ls.PNG)

 `cd nombrecarpeta`  Permite moverte entre carpetas. 
![cd](./cd.PNG)

 `mkdir nombrecarpeta` Crea una carpeta nueva. 
![mkdir nombrecarpeta](./mkdir%20nombrecarpeta.PNG)

Ejemplo:
```bash
cd desktop
mkdir gitkarol
cd gitkarol
```

---

## Primeros pasos con Git

Inicializa el repositorio dentro de la carpeta del proyecto:
```bash
git init
```
Esto crea una carpeta oculta llamada `.git` que contiene toda la información del control de versiones.
![git init](./git%20init.PNG)

Verifica el estado:
```bash
git status
```
![git status](./git%20status.PNG)

Si no hay archivos, Git te lo dirá.  
Crea uno (por ejemplo `notas.txt`), y vuelve a ejecutar `git status`.  
Aparecerá como “untracked”.
![git status y echo](./git%20status%20y%20echo.PNG)

---

## Agregar y confirmar archivos

 Agrega el archivo al área de preparación:
```bash
git add notas.txt
```
![git add status](./git%20add%20status.PNG)


 Crea el primer commit:
```bash
git commit -m "Primer commit: agrego archivo notas.txt"
```
![git commit](./git%20commit.PNG)


 Si haces cambios al archivo, Git lo marcará como “modificado”.  
Para guardar esos nuevos cambios, repite:
```bash
git add .
git commit -m "Actualizo archivo notas.txt"
```

---

## Consultar historial de versiones

Para ver los commits:
```bash
git log
```
![git log](./git%20log.PNG)

O en versión corta:
```bash
git log --oneline
```

Si quieres regresar un archivo a su versión anterior:
```bash
git checkout -- notas.txt
```
en mi caso no lo hare porque no es necesario

---

## Ramas en Git

Las ramas sirven para trabajar en nuevas funciones sin afectar la principal.

 `git branch`  Muestra las ramas existentes. 
 `git branch git`  Crea una rama llamada *git*. 
![git branch](./git%20branch.PNG)
![nueva rama](./nueva%20rama.PNG)

 `git switch git`  Cambia a la rama *git*. 
![trabajaramagit](./trabajaramagit.PNG)

 `git merge git` |Une la rama *git* con *main*. 
 `git branch -d git`  Borra la rama *login*. 
en mi caso no hare ninguna de las dos porque no lo requiero

---

## Conectando con GitHub

GitHub es una plataforma en la nube que permite guardar y compartir repositorios.  
Una vez creado tu repositorio en GitHub, sigue estos pasos desde la terminal:

```bash
git remote add origin https://github.com/tu_usuario/tu_repositorio.git
git branch -M main
git push -u origin main
```
![enlacerepositorio y main](./enlacerepositorio%20y%20main.PNG)

Si es la primera vez, Git te pedirá iniciar sesión en el navegador.

Desde ese momento tu repositorio local queda sincronizado con el remoto.

---

## Comandos GitHub más usados

 `git fetch`  Descarga los cambios del repositorio remoto sin aplicarlos. 
 `git pull` Descarga y actualiza el repositorio local con los cambios remotos. 
 `git push`  Sube los commits locales a GitHub. 
 `git push -u origin <rama>` Sube una rama nueva y la enlaza con GitHub. 
 `git clone <url>`  Clona un repositorio remoto en tu computadora. 
![comandos github](./comandos%20github.PNG)
![git push y repositorio](./git%20push%20y%20repositorio.PNG)

Ejemplo:
```bash
git clone https://github.com/mariaolaya17/trabajo-git-karol.git
```

---

## Otros comandos útiles

 `git diff`  Muestra los cambios entre versiones. 
 `git reset --hard`  Elimina los cambios no confirmados. 
 `git revert <id_commit>`  Deshace un commit anterior. 
 `git stash` / `git stash pop`  Guarda y recupera cambios temporales. 
 `git tag <nombre>`  Marca versiones importantes. 

---

## Conclusión

Git y GitHub son herramientas poderosas que permiten trabajar en equipo de forma organizada.  
Con Git puedes controlar el historial de tu código, crear ramas para probar cosas sin miedo a romper nada y volver atrás si algo sale mal.  
GitHub te da la ventaja de tener tu proyecto en la nube y colaborar con otros desarrolladores desde cualquier parte del mundo.

