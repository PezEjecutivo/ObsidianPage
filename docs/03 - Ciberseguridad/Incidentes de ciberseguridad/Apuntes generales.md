
1.- General
leaks
contraseñas
2fa

2.- Plan de concienciación y protección puesto de trabajos (Prevenir)

3.- Montar un CyberSOC (Detectarlos)
SIEM
AWS

SOC -> Secutiry Operation Center

4.- Gestión de incidentes de ciberseguridad (Erradicarlos)

5.- Notificar, documentacion, lecciones aprendidas

# Unidad 1 - establecimiento de planes
leaks: se define como una fuga de informacion y datos. Esto es algo que puede estar publico en internet.

Para mitigar los leaks deberemos usar multiples contraseñas diferentes y multiples correos diferentes.



Tener diversos correos
Personal
Trabajo
Ocio
Compras online

Bitwarden es un gestor de contraseña gratuito

No registrarse con la cuenta de google o similares.

Si no queremos usasr gestores de contraseña podemos utilizar el siguiente metodo
(tiene que ser larga y contener un poco de todo)
1.-Cogueremos varios elementos
2.-Un numero
3.-Uno de esos elementos estara completa en mayuscula
4.-Separar los elementos con caracteres especiales
5.-Añadirle un prefijo o un subfijo relacionado con el sitio

Ejemplo: 
FB#ventana-MONITOR.12
TW#ventana-MONITOR.12
ventana-MONITOR.12#NF

(privacy guides, una pagina web que recomienda cosas de seguridad)

Lo recomendable es usar contraseñas fuertes y combinarlas con otros metodos.

# Que hacer si te hackean/powdnean?

Para entrar a una cuenta hace falta email y password, para evitar que alguien entre con esos datos deberemos usar tecnicas como 2FA (2 Factores de Autentificacion) y MFA (Multiples factores de autentificacion)

(para hacerlo en google tendremos que entrar a la parte de myaccount y activar en seguridad la verificacion en dos pasos)
Como usar los 2FA, con Sms, App (google authenticator, Aegis, FreeOTP(iphone)), Yubikey, email


# Buenas Praxis de ciberseguridad
No utilices tus credenciales de acceso corporativas en aplicaciones de uso personal. (No crees cuentas de ocio con el correo del trabajo o clases)

No pinches en enlaces (links) sospechosos.

Mejor escribe la dirección en la barra del navegador.

Protege la información impresa utilizando mobiliario con cierres, cajas fuertes o armarios ignífugos.

Procura no transportar información sensible en dispositivos extraíbles. Si lo haces, cifra la información.

Aprende a detectar los ataques de ingeniería social y cómo defenderte. Avisa si ver un comportamiento anómalo.

Bloquea la sesión de tu equipo cuando abandones tu puesto de trabajo.

No modifiques la configuración de tus dispositivos móviles ni instales aplicaciones no autorizadas.

Evita el uso de equipos no corportavios para acceder a servicios de la empresa. Si accedes al correo corporativo desde tu equipo peresonal, no descargues ficheros al equipo.

Destruye la información sensible en formato papel. No te limites a tirarla a la papelera y evita una fuga de información.

Se cuidadoso con el uso del correo electrónico. Evita los correos en cadena.


# Retos
## Reto 1
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

### Solución
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

## Reto 2
Descripción 

Después de muchos años recopilando documentación, fotos y artículos, se ha decidido realizar una limpieza y llevar la documentación antigua a una nueva sala que le ha cedido el instituto. 
En esta sala se pueden archivar de una forma sencilla por fecha todos los documentos del periodico.

Pregunta 

Durante este proceso moviendo documentos, una hoja extraña se cae entre los documentos que llevais. Contiene un texto ilegible junto a la referencia del emperador Julio César. ¿Podrás sacar en claro que quería decir la nota?


Datos proporcionados: 

Yn fvthvragr vasbeznpvba rf pbasvqrapvny. Gr nlhqnen n cebfrthve ra yn vairfgvtnpvba. Ab gr pbasvrf, ab gbqnf ynf vasbeznpvbarf qr ynf dhr qvfcbarzbf fba gna snpvyrf pbzb rfgn ebgnpvba qr pnenpgrerf. Sveznqb: ha nzvtb.  
synt{rfgnzbf_rzcrmnaqb_n_pbabpre_nytb_qr_uvfgbevn}

### Solución
Nos hablan de que el texto estaba junto a una referencia de julio cesar, si buscamos en Google "código cesar" o similares nos aparecerá el Cifrado Cesar, una vez con esta información podemos buscar un descodificarlo online y nos dará el siguiente resultado una vez introduzcamos el texto.

El texto estaba cifrado en Cesar 13

La siguiente información es confidencial. Te ayudara a proseguir en la investigacion. No te confies, no todas las informaciones de las que disponemos son tan faciles como esta rotacion de caracteres. Firmado: un amigo.  
flag{estamos_empezando_a_conocer_algo_de_historia}
