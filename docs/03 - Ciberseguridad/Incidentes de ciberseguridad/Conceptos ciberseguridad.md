Seguridad: algo que no tiene riesgo y esta fuera de todo peligro (el problema es que no existe una seguridad al 100%) por ende la seguridad suele llamarse fiabilidad

Aspectos generales: Confidencialidad, integridad y disponibilidad

Elementos a proteger: HW, SQ y datos

Amenazas, tipos: Interrupcion, interceptacion, modificacion y fabricacion.
Origen: Personas, amenazas logicas, catastrofes

Mecanismos: prevencion

## Aspectos generales de ciberseguridad
Al tener algo abierto al exterior, estamos expuesto.
Cuando hablamos de aumentar la ciberseguridad, hablamos del triangulo de la ciberseguridad
![[Cia Triad.png]]

<span style="color:rgb(64, 156, 255)">Disponibilidad</span>:  Los datos sean accesible siempre que sea necesario.

<span style="color:rgb(64, 156, 255)">Confiabilidad</span>: Los datos están disponibles solo para las personas con permisos
Para que algo sea confiable hace falta que haya autentificación y autorización.

<span style="color:rgb(64, 156, 255)">Integridad</span>: Los datos están completos y sin modificaciones o alteraciones (Hashes)

## Amenazas

### Tipos
Proceso habitual:
Escaneo de puertos (portscan): detectar que servicios ofrece una maquina. Abiertos, cerrados o protegidos  (cortafuego)

Interceptación lógica (sniffing): analizar los paquetes que circulan por el medio compartido (dominio de colision)

fabricación (spoofing)

denegación de servicio (Dos) Distribuido (DDoS)

(Botnet, cuando un atacante tiene acceso a muchos dispositivos a la vez para poder mandar muchisimas veces paquetes a una maquina haciendo una colision)


DDoS usando DNS, al pedirle un dato, cuesta 80Kb, la respuesta del DNS 500mb (ejemplo).

Sabiendo esto, entonces nosotros mandamos la petición con la IP de origen del servidor que queremos atacar en vez de la nuestra, haciendo que la DNS le mande los 500mb (ejemplo) al propio servidor acumulando los recursos del servidor, ya que se ira acumulando (Aplicación por DNS / dos over dns)

### Origen
Personas: personal, ex-empleados, curiosos, crackers, terroristas, hackers, intrusos remunerados, etc...

La mejor forma de despedir a alguien, es deshabilitar todo lo que tenga el empleado y una vez no tenga acceso a nada, despedirle, ya que si no puede intentar causar algún tipo de problema.

Amenazas lógicas: programas, ya sea mediante bugs o malware.
Catástrofes naturales: incendios, inundaciones, terremotos, etc.

En los últimos 10 años el malware mas popular ha sido el ramsonware, ya que encripta los datos y no permite recuperarlo a no se que pagues, por lo que es bastante lucrativo.

## Mecanismo
Prevención, detección y recuperación.

Prevención: Aumentan la fiabilidad durante el funcionamiento normal, previniendo la ocurrencia de violaciones de seguridad
(Antivirus, Cifrado, Corta fuegos, contraseñas seguras/2FA)

Detección aquellos que se utilizan para revelar violaciones de seguridad o intentos

Recuperación: se aplican cuando la violación del sistema se ha detectado. Deben devolver el sistema a su funcionamiento normal. (Copias de seguridad)

Firewall: Sistema o grupo de sistemas que hace cumplir una política de control de acceso entre dos redes.

Perímetro de seguridad: es el espacio protegido por el cortafuegos. Suele ser propiedad de la organización.


LAN: Local Area Network
WAN: Wide Area Network

Es un cortafuego pero mas bestia, en vez de haber un muro, hay una red entera entre ellos
![[DMZ.png]]

## Criptografia
Criptología:  Ciencia que trata los problemas teóricos relaciones con la seguridad den el intercambio de mensajes en clave entre un emisor y un receptor a través de un canal de comunicaciones.

Dos ramas:
	Criptografia
	Criptoanalisis

El objetivo original de la criptografía era mantener en secreto un mensaje. Privacidad o confidencialidad.
En la actualidad se busca también garantizar la autenticidad, la integridad y el no repudio.
Existen dos formas de generar un criptosistema seguro: o manteniendo en secreto el algoritmo empleado o manteniendo en secreto algún valor empleado por el algoritmo.

M -> algoritmo -> C
HOLA -> +13 letras -> UBYN

Hoy en día los criptosistemas se basan en mantener en secreto una serie de parámetros, llamados claves. El algoritmo puede ser publico y conocido.

En la modernidad hay dos tipos, los simétricos y los asimétricos.

M --- Clave --> C --- Clave --> M
M --- Clave privada --> C --- Clave publica --> M

En el cifrado GPC, tenemos 2 claves, la clave privada solamente la tengo yo y la publica la tiene cualquiera.


