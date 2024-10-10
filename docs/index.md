# Como usar Obsidian con GitHub Pages!

## Métodos para hacerlo.

Aunque he encontrado varios métodos para hacerlo con diferentes aplicaciones/repositorios, solamente explicare uno en detalle, el que estoy usando.

Estas son las alternativas al método que vamos a utilizar:

- [datopian/obsidian-flowershow](https://github.com/datopian/obsidian-flowershow): plugin for publishing with flowershow direct from your obsidian vault.

- [kmaasrud/oboe](https://github.com/kmaasrud/oboe): tool to convert an Obsidian vault into a static directory of HTML files.

- [Jackiexiao/foam-mkdocs-template](https://github.com/Jackiexiao/foam-mkdocs-template): template for Obsidian/Foam using mkdocs/mkdocs-material/mkdocs-roamlinks-plugin

- [foambubble/foam-template](https://github.com/foambubble/foam-template): Foam workpace template

- [ObsidianPublisher/obsidian-mkdocs-publisher-template](https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template): Obsidian Mkdocs Publisher, a free obsidian publish alternative throught Mkdocs

- [KosmosisDire/obsidian-webpage-export](https://github.com/KosmosisDire/obsidian-webpage-export): Webpage HTML Export lets you export single files or whole vaults as HTML websites or documents. It is similar to publish, but you get direct access to the exported HTML.

- [Enveloppe/obsidian-enveloppe: publish your notes on a GitHub repository from Obsidian Vault](https://github.com/Enveloppe/obsidian-enveloppe)

Nosotros lo haremos desde el siguiente repositorio:
[Repositorio utilizado](https://github.com/jobindjohn/obsidian-publish-mkdocs?tab=readme-ov-file).

## Pasos a seguir:

### 1.- Clonar el repositorio / usar la plantilla

Al entrar al repositorio en la barra principal de dicho repositorio nos aparecerá a la derecha del todo un botón que pone "Use the template". 
![[Pasted image 20241010230800.png]]
Si no queremos darle al botón también podemos usar este [enlace](https://github.com/jobindjohn/obsidian-publish-mkdocs/generate) el cual se encuentra en el readme.md de dicho repositorio.

(Ambos casos tienen el mismo resultado, por lo que depende de tu preferencia).

Lo único que tendremos que hacer es ponerle un nombre al repositorio, este será el que aparezca justo después de nuestro nombre, es decir en mi caso, mi cuenta de github es PezEjecutivo, entonces el enlace seria: pezejecutivo + .github.io + / + Nombre del repositorio/. En mi caso [pezejecutivo.github.io/ObsidianPage](https://pezejecutivo.github.io/ObsidianPage/).
![[Pasted image 20241010231010.png]]

(Tengo entendido que puedes poner el repositorio tanto en privado como en publico, pero no he podido comprobar que funcione en privado.).

### 2.- Estructura del repositorio

Ya que no podemos actuar sin saber, primero veremos un poco de la estructura del repositorio seria el siguiente:
![[Pasted image 20241010231636.png]]

<span style="color:rgb(0, 176, 240)">github/workflows:</span> Debemos tener en cuenta que github/workflows es para que se nos despliegue la pagina como debe ser, ya que sin el la pagina no funcionaria de manera adecuada, así que debemos evitar tocar esa carpeta.

<span style="color:rgb(0, 176, 240)">docs:</span> Esta será la carpeta en la que debemos crear el vault de Obsidian para que según creemos las notas se creen en dicho repositorio, haciendo que lo único que tengamos que hacer una vez escribamos la nota sea subirlo a git (mediante git add . | git commit "mensaje" | git push).

<span style="color:rgb(0, 176, 240)">.gitignore:</span> Podremos usar este archivo para añadirle las cosas que no queramos que se suban de nuestras notas de Obsidian, por normal general no suele usarse para este uso, pero en nuestro caso nos sirve para ocultar cosas sin problemas y no tener que separar las notas en diferentes baúles en caso de que no queramos.

<span style="color:rgb(0, 176, 240)">mkdocs.yml:</span> Es el archivo que se encarga de hacer el despliegue de github pages, este archivo tiene contenido que puede ser modificado pero debemos entenderlo primero y tener cuidado a la hora de modificarlo, ya que podrías tumbar la pagina, en este fichero se pueden cambiar ajustes como los plugins, temas y demas. (Para cambiar el titulo de la pagina deberemos cambiar la primera linea y poner lo que nosotros elijamos).

El resto de elementos son 3 imágenes diseñadas para el readme, las cuales podríamos quitar junto al readme.md (Lo verdaderamente correcto seria modificar dicho readme.md en vez de eliminarlo, pero si lo eliminamos tampoco sucedería ningún problema.). Tambien hay una licencia, el propio readme.md.

### 3.- Crear el baúl de Obsidian

Simplemente tendremos que abrir el menú de selección de los baúles, el cual esta abajo a la izquierda o te aparece nada mas abrir Obsidian en el caso de que no tengas ningún otro baúl o sea la primera vez que lo abres.

Clicaremos en la segunda opción "Open folder as vault" y seleccionaremos la carpeta docs de nuestro repositorio.
![[Pasted image 20241010232813.png]]

### 4.- Como añadir contenido

Una vez estemos dentro, veremos el menu de la izquierda el cual tiene el contenido actual de la pagina, podremos borrarlo o mantenerlo y modificarlo, dependiendo del uso que quieras darle, pero ya estaria practicamente todo hecho. Solo queda que crees tus notas y lo subas tal y como mencionamos anteriormente.

![[Pasted image 20241010233104.png]]

(Recordatorio de que aunque nosotros solo modifiquemos la carpeta docs, el repositorio esta en la carpeta principal, por lo que debemos hacer los comandos de git desde alli, no desde docs)

git add .
git commit -m "mensaje"
git push

Después de unos minutos la pagina deberá estar con el contenido nuevo añadido.

Algunas de las cosas no funcionan tal y como se ven en Obsidian, por lo que hay que tener cierto cuidado con ello, ya que podemos tener un formato diferente en nuestro Obsidian que en la pagina, para saber como funciona algo en nuestra pagina podemos comprobarlo desde este [enlace](https://squidfunk.github.io/mkdocs-material/reference/ "Documentacion de nuestra plantilla").

### 5.- Github pages
Para subirlo a github pages, iremos settings, en el apartado de "Code and automation" y en Branch pondremos la rama de gh-pages, aunque nosotros estemos actualizando la rama de main en vez de la de gh-pages seguirá funcionando sin ningún tipo de problema.

![[Pasted image 20241011001731.png]]

Si es la primera vez que lo usamos, podemos llegar a pensar que no funciona ya que no nos da ningun tipo de feedback, simplemente deberemos esperar un poco y visitar nuestra pagina a ver si esta, si clicamos en el enlace que nos sale en ese mismo apartado que pone github-pages, podremos ver el estado de la pagina.
## Pablo Valladares González y Juan Francisco González Gómez