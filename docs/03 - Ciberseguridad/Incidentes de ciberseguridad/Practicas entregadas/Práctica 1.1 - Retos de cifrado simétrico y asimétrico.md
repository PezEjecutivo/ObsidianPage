
<div style="text-align: center; font-size:30px">
Incidentes de Ciberseguridad
</div>

![[Portada practica Retos de cifrado.png|  500 500]]

<div style="text-align: center;">C.E. en Ciberseguridad en Entornos de las Tecnologías de la Información <br />
IES Mar de Cádiz - El Puerto de Santa María <br />
2024/2025</div>

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

- [[#Enunciado|Enunciado]]
		- [[#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.|Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:|Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:]]
- [[#Resolución|Resolución]]
	- [[#Resolución#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.|Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.]]
		- [[#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.#Reto 1|Reto 1]]
		- [[#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.#Solución|Solución]]
		- [[#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.#Reto 2|Reto 2]]
		- [[#Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.#Solución|Solución]]
	- [[#Resolución#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:|Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#1. Generar unas claves para nuestro equipo.|1. Generar unas claves para nuestro equipo.]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#2. Exportar nuestra clave.|2. Exportar nuestra clave.]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#3. Importar las claves de gpg  de otro compañero.|3. Importar las claves de gpg  de otro compañero.]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#1. Listar todas las claves privadas y listar todas las claves publicas|1. Listar todas las claves privadas y listar todas las claves publicas]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#5. Crea un archivo .txt y escribe un texto fácil en él. Cifra dicho archivo con la clave pública del receptor (tu compañero). Envíale ese archivo cifrado.|5. Crea un archivo .txt y escribe un texto fácil en él. Cifra dicho archivo con la clave pública del receptor (tu compañero). Envíale ese archivo cifrado.]]
		- [[#Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:#1. Descifra el archivo recibido con nuestra clave privada.|1. Descifra el archivo recibido con nuestra clave privada.]]
- [[#Bonus|Bonus]]
- [[#Conclusion|Conclusión]]
- [[#Bibliografia|Bibliografia]]


<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

## Enunciado

#### Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.

#### Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente:  
  

1. Generar unas claves para nuestro equipo.
2. Exportar nuestra clave.
3. Importar las claves de gpg  de otro compañero.
4. Listar todas las claves privadas.  
    
5. Listar todas las claves públicas.
6. Crea un archivo .txt y escribe un texto fácil en él. Cifra dicho archivo con la clave pública del receptor (tu compañero). Envíale ese archivo cifrado.
7. Descifra el archivo recibido con nuestra clave privada.  

Si no hubiera grupos de dos personas, se puede realizar en grupos de 3, pero cada uno debe generar sus claves.

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

## Resolución

### Ejercicio 1: Hay dos archivos con mensajes cifrados de forma algorítmica. Descífralos.

#### Reto 1
Descripción 

Desde la creación del instituto, algunos alumnos se han encargado de la gestión del periodido local, "El noticiero", donde se intercambian mensajes y escriben artículos didácticos. En uno de los artículos alguien anónim@ ha lanzado un reto. Asegura haber escondido un mensaje en el libro más universal de la literatura castellana. En su mensaje advierte que para empezar, nos proporciona algunas coordenadas para que las mentes mas brillantes del instituto puedan resolverlo. 

Pregunta 

¿Cuál es el mensaje secreto que ha enviado el alumno anónimo y ha escondido este alumn@?


Datos proporcionados 

Libro: "El quijote de la mancha"
10:8:2   
23:11:1  
30:8:2   
30:26:7 
35:1:7  
151:19:10 
151:11:8  
152:11:5  

#### Solución
Para solucionar este reto tenemos que coger las coordenadas que nos ofrecen, estas son La pagina, la linea de texto y la palabra, dando como resultado: 

10:8:2         - Querer
23:11:1       - Saber
30:8:2         - noticia  
30:26:7       - sobre
35:1:7         - conocer
151:19:10   - misterio
151:11:8     - quien
152:11:5     - hizo

Querer saber noticia sobre conocer misterio quien hizo

#### Reto 2
Descripción 

Después de muchos años recopilando documentación, fotos y artículos, se ha decidido realizar una limpieza y llevar la documentación antigua a una nueva sala que le ha cedido el instituto. 
En esta sala se pueden archivar de una forma sencilla por fecha todos los documentos del periodico.

Pregunta 

Durante este proceso moviendo documentos, una hoja extraña se cae entre los documentos que llevais. Contiene un texto ilegible junto a la referencia del emperador Julio César. ¿Podrás sacar en claro que quería decir la nota?


Datos proporcionados: 

Yn fvthvragr vasbeznpvba rf pbasvqrapvny. Gr nlhqnen n cebfrthve ra yn vairfgvtnpvba. Ab gr pbasvrf, ab gbqnf ynf vasbeznpvbarf qr ynf dhr qvfcbarzbf fba gna snpvyrf pbzb rfgn ebgnpvba qr pnenpgrerf. Sveznqb: ha nzvtb.  
synt{rfgnzbf_rzcrmnaqb_n_pbabpre_nytb_qr_uvfgbevn}

#### Solución
Nos hablan de que el texto estaba junto a una referencia de julio cesar, si buscamos en Google "código cesar" o similares nos aparecerá el Cifrado Cesar, una vez con esta información podemos buscar un descodificarlo online y nos dará el siguiente resultado una vez introduzcamos el texto.

El texto estaba cifrado en Cesar 13

La siguiente información es confidencial. Te ayudara a proseguir en la investigacion. No te confies, no todas las informaciones de las que disponemos son tan faciles como esta rotacion de caracteres. Firmado: un amigo.  
flag{estamos_empezando_a_conocer_algo_de_historia}

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

### Ejercicio 2: En este ejercicio vamos a trabajar en grupos de dos personas. El objetivo es usar gpg para el envío de mensajes cifrados. Concretamente vamos a realizar lo siguiente: 

#### 1. Generar unas claves para nuestro equipo.

Para generar nuestras claves utilizaremos el comando `gpg --generate-key`

Una vez usemos dicho comando, nos pedira: Nombre y correo, despues de eso podremos ponerle una contraseña de manera opcional para mayor seguridad, en mi caso he puesto una contraseña para mayor seguridad ya que estamos en un ciclo relacionado con eso y hay que concienciar a la gente sobre ello.

![[gpg --generate-key.png]]

![[gpg --generate-key - Passphrase.png]]

#### 2. Exportar nuestra clave.

Para exportar nuestras claves tendremos que usar  `gpg --export --armor -output fichero`

--export para exportarla
--armor para reforzar el codigo ascii (created ascii armored output)
--output fichero para escoger el nombre del archivo que nos devuelve

Una vez usamos dicho comando, para comprobar que esta creado, usamos el comando ls y comprobamos que este en el directorio el archivo que acabamos de crear.
![[gpg --export --armor.png]]

#### 3. Importar las claves de gpg  de otro compañero.

Para importar la clave de un compañero primero necesitaremos que este nos la pase, en mi caso nos la ha pasado por driver.
![[Antonio.pub compartido.png]]

Una vez en el directorio con el arhcivo hacemos el siguiente comando `gpg --import fichero`

con este comando importaremos las claves de dicho fichero, tambien podemos hacerlo poniendo la ID, que por normal general sera lo que nos aparezca al hacer TAB
![[gpg --import.png]]
#### 4. Listar todas las claves privadas y listar todas las claves publicas

Para mostrar las claves publicas haremos el siguiente comando `gpg --list-public-keys`

Este comando mostrara todas las claves publicas, nos podemos asegurar de ello, ya que aunque parezca que es la privada, a la izquierda del todo pone pub de public, en vez de sec de secret.
![[gpg --list.png]]

####  5. Crea un archivo .txt y escribe un texto fácil en él. Cifra dicho archivo con la clave pública del receptor (tu compañero). Envíale ese archivo cifrado.

Creamos el archivo con un texto sencillo, en este caso con el texto de "Como te va el dia?"
![[gpg - Mensaje sencillo.png]]

Para encryptarlo usaremos el comando `gpg --encrypt --recipient ID fichero`

--encrypt para encriptarlo
--recipient ID para escoger con que clave vamos a encriptarlo
fichero, el nombre del arhccivo a encriptar
![[gpg --encrypt --recipient.png]]

####  6. Descifra el archivo recibido con nuestra clave privada.

Para descifrar un archivo haremos el comando `gpg --decrypt fichero`
En el caso de que nuestra clave de encriptacion tenga contraseña nos la pedira.
![[gpg --decrypt.png]]

Como podemos ver, una vez hemos hecho el comando, nos mostrara el mensaje justo despues, en este caso "good morning chavalote"
![[gpg --decrypt.png]]

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

## Bonus

Como podemos ver, si abrimos el archivo de la llave publica. nos aparecera el texto asi. de esta forma podemso comprobar que la llave es la publica, ya que lo pone y esta completamente bien.

![[cat PabloVG-gpg.pub.png]]

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

## Conclusión

Creo que hay muchas formas de poder ser atacado y es necesario ir con precaución cuando tratamos información sensible o importante que necesita de confidencialidad, como hemos visto hay ataques de interceptación (Sniffing)  y modificación (Man in the middle) de los cuales podemos ser victimas cuando mandamos alguna información por internet, creo que a la hora de enviar un documento muy importante, como podría ser datos de la cuenta bancaria o personales. Si los encriptamos nos aseguramos de tener una mayor fiabilidad de que no nos pase nada, creo que es util el saber este tipo de cosas, aunque por normal general no vayamos a hacerlo siempre. Para cuando queremos ese extra o somos paranoicos es algo muy util de saber.

No creo que vaya a usarlo demasiado en mi vida personal, pero si que creo que debería ser una practica habitual cuando pasamos información sensibles a terceros aunque pueda llegar a ser mas incomodo, como una frase famoso que dice "A mayor seguridad, mayor incomodidad".

<div style="page-break-after: always; visibility: hidden"> \pagebreak </div>

## Bibliografía 

gcg --help  (con la ayuda del comando | grep palabra, cuando sabia que podía estar relacionado con algo)

https://medium.com/@biicaleb316/how-to-perform-encryption-and-decryption-with-kali-linux-using-gpg-gnu-privacy-guard-utility-fc5915644bff

[Red Hat](https://www.redhat.com/sysadmin/creating-gpg-keypairs)

[Stack Exchange / superuser](https://superuser.com/questions/999286/how-to-install-public-keys-with-gpg)

[David Poza](https://davidinformatico.com/cifrar-con-gpg)
