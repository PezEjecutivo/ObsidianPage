# Prerrequisitos

Para realizar esta instalación necesitaremos un dispositivo USB (o su equivalente) con al menos 2GB de espacio para poder añadirle la imagen iso del Debian, la cual podemos obtener desde la [pagina oficial de Debian](https://www.debian.org).

Una vez tenemos el USB (o su equivalente) con la imagen iso de Debian, lo montaremos, en Windows tendremos que utilizar el programa "Rufus" [pagina oficial de Rufus (en español)](https://rufus.ie/es/).

# Instalación
## 1. Instalación
Apagaremos el PC y lo encenderemos, tendremos que pulsar una tecla en especifico para entrar al menú de arranque, una vez allí (es decir en el boot loader/BIOS) desactivaremos el secure boot y el fast boot. Esto es porque el secure boot puede darnos problemas al intentar instalar el Debian y el fast boot nos iniciaría automáticamente desde el disco duro con el sistema operativo, por eso lo desactivamos para que nos pregunte.

Una vez hecho esto volveremos a encender el ordenador y entraremos desde el USB con la iso de Debian.

## 2. Configuración del Debian
Nada mas entrar veremos esta pantalla, a la cual tendremos que darle a "Install", ya que no requerimos del Graphical install
![[Interfaz de instalación Debian.png]]

Una vez hecho esto nos hará varias preguntas sobre la distribución y configuración de teclado, lo pondremos en español y una vez hecho esto empezara a cargar.
![[Cargando componentes adicionales - Debian.png]]

Despues de este paso vendra la configuración de red, puede que salga un cartel de "Detección del hardware de red" y ponga que necesitamos instalar controladores desde un medio externo, simplemente le daremos a que no y continuaremos con la siguiente ventana, esta nos preguntara si usamos red wifi o cableada. 
![[Configuración de red - Debian.png]]

Una vez con la configuración de la red puesta y el dispositivo este conectado a ella, empezara a preguntarnos datos de la maquina, primero preguntara el nombre de la maquina, la cual en mi caso es A314-ceti04, ya que estamos en el Aula 314, en el curso de ceti y soy el puesto 4.
![[Nombre de la maquina - Debian.png]]

Ahora nos preguntara el nombre de dominio, el cual lo dejaremos vacio, ya que no vamos a usarlo (de momento), nos preguntara por la contraseña de super usuario, la cual sera maled0r. el nombre de usuario es usuario y la contraseña usuaria.
![[Contraseña del usuario - Debian.png]]

Terminado esta configuración, nos pedirá la configuración del reloj y empezaremos el particionado de los discos. Al tener varios dispositivos de almacenamientos, escogí el modo manual para poder escoger cual era el dispositivo que queria que tuviera el Debian.
![[Menu general de particiones (Manual) - Debian.png]]

Con el dispositivo de almacenamiento ya escogido, nos saldra para particionarlo como Debian utiliza sus dispositivos de almacenamiento de rooteo, una vez lo hagamos, simplemente tendremos que volver a la pestaña de metodo de particionado y escoger el modo "Guidao - Utilizar el espacio libre contiguo más grande".
![[Particionado de discos (manual) - Debian.png]]

Despues de haber realizado el paso anterior nos saldra el como queremos que se particione el dispositivo de almacenamiento, el cual escogueremos "Todos los ficheros en una partición (recomendado para nobatos)"
![[Particionado de disco, recomendado para novatos (Guiado) - Debian.png]]

Despues de unas pequeñas comprobaciones más, empezaria a instalarse el sistema base.
![[Instalando el sistema base - Debian.png]]

Ahora solo nos quedaria escoger el selector de paquetes y la selección de programas, en la cual marcaremos "Entorno de escritorio Debian, GNOME, SSH server, Utilidades estándar del sistema".
![[Selección de programas - Debian.png]]

## 3. Instalación de los drivers
Debian no trae por defectos alguno de los paquetes que vamos a necesitar, asi que vamos a añadirlos a la lista de librerias que tiene que descargar para ello utilizaremos el siguiente comando:
`nano /etc/apt/sources.list`

Una vez en el archivo añadiremos en la primera linea las 2 siguientes palabras "contrib" y "non-free"
![[nano etc-apt-sources.list.png]]

Despues realizaremos un apt update para que se nos descarguen los paquetes nuevos que hemos añadido a la lista y usaremos el siguiente comando para que nuestro Debian pueda funcionar en los dispositivos de clase:
`apt install nvidia-tesla-470-driver`
![[apt install nvidia-tesla-470-driver - Debian.png]]

