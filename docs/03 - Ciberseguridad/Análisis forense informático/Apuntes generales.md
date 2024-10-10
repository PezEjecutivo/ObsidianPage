 [ISO - Google Drive](https://drive.google.com/drive/folders/1M1sBn_ebD1IbKK42gWP--8v704e6mU7P)

## Sistema de evaluación
<span style="color:rgb(64, 156, 255)">primera evaulacion</span>: 60 Practicas - 20 Observaciones diarias - 20 Exámenes/Exposiciones.
<span style="color:rgb(64, 156, 255)">Segunda evaluación</span>: 30% Practicas - 25% Informe forense - 25% Proyecto investigación - 20% Observación diaria
## Programas:
<span style="color:rgb(64, 156, 255)">everything</span>: (indexa todo lo que tenemos en los discos duro y nos lo muestra).
<span style="color:rgb(64, 156, 255)">Magnet RAM</span>: Captura de memoria RAM.
<span style="color:rgb(64, 156, 255)">VirtualBox</span>: Maquinas virtuales.
<span style="color:rgb(64, 156, 255)">Volatily</span>: ???


Una forma fácil de romper un archivo es cambiarle un valor hexadecimal.

el análisis forense informático hay diferentes campos: Forense PC, Forense en dispositivos móviles y Forense en la red...

Con las capturas de RAM se pueden hacer análisis forenses y análisis de malware (que es donde se almacenan los malwares)

Los pasos de las investigaciones son:
1. Investigación digital
2. Posible identificación de sospechosos
3. seguir
4. cercar
5. arrestar

1 al 4 privada, 5 publica (Cuerpos y fuerzas de seguridad)


El análisis forense es proactivo, debemos estar preparado, de esta manera si tenemos un incidente podremos conseguir mas pistas que si tardamos mas en reaccionar, ya que se pueden perder cosas o el propio delincuente borrar su huella para que sea mas difícil.

Si no hay evidencias no se puede demostrar nada, nuestro trabajo se basa en conseguir las evidencias y guardarlas para poder mostrarlas.

Una evidencia no es un fichero de logs, sino lo que sacamos de dicho fichero. (por ejemplo el fichero de logs), una evidencia tambien puede ser la ausencia de un fichero que deberia de existir

Una evidencia tiene que tener:
Relevancia, Fiabilidad y Suficiencia

Tenemos que evidenciar que una persona estuvo en paris en 2018 y en su ordenador sale una foto de el en paris pero sale de espalda, igual solamente esa imagen no es suficiente.

repetible: mismos procedimientos y metodos producen el mismo resultado 
reproducible: Cambio los metodos por unos equivalentes y me da el mismo resultado

Por ejemplo, siempre que use photoshop me va a dar el mismo resultado en caso de que sea repetible y reproducible seria que puedo usar cualquier otro programa similar me va a dar el mismo resultado.

Bob.raw -> Captura de la memoria RAM, volatility lo que hace es analizar dicha captura de memoria RAM.

1.-Profile = Es el tipo de maquina y/o sistema operativo estaba ejecutandose a la hora de hacer la captura de RAM. (Windows, linux, etc...)

<span style="color:rgb(64, 156, 255)">python vol.py -f memory.vmem imaeinfo </span>- Ver profile
Una vez tenemos el profile lo primero que tenemos que hacer es ponerle el profile


en regedits (registor de windows) tenemos los hives -> HKEY_

