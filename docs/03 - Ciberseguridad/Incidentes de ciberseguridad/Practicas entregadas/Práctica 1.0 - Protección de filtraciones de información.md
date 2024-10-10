Ejercicio 1: Cuando hablamos de leaks estamos hablando de una fuga de información de datos. Esto es algo que puede estar accesible en Internet. Pastebin es una web donde cualquier usuario puede subir textos para que estén visibles al público, y donde podemos encontrar muchos leaks de diferentes tipos.

Haz uso de pastebin.com junto con las búsquedas de Google como hemos visto en el tema para buscar y encontrar leaks de correos electrónicos y tarjetas de crédito.  

Explica todo el procedimiento desde las búsquedas hasta el momento de encontrar los leaks.

Enumera los enlaces de los leaks que hayas encontrado.

(hacerlo usando las busquedas avanzadas de google, como site:, "palabra", related:, info:)


Ejercicio 2: Para comprobar qué filtraciones puede haber sufrido nuestro correo electrónico existen diversas webs que nos pueden ayudar. Una de ellas es HaveIBeenPwnd. Usa dicha web para comprobar si tus correos habituales han formado parte de una filtración de datos. Una alternativa a HaveIBeenPwnd es BreachDirectory ([https://breachdirectory.org/](https://breachdirectory.org/)), aunque probablemente la base de datos en la que se basan sea similar.


Ejercicio 3: Crea una cuenta en Bitwarden.com. Instala la extensión en tu navegador ([https://bitwarden.com/](https://bitwarden.com/)).

Ejercicio 4: Crea una cuenta en Firefox y usa Firefox Relay ([https://relay.firefox.com](https://relay.firefox.com/)).

Ejercicio 5: Crea una cuenta en tryhackme con un alias de firefox relay y generando una contraseña con bitwarden. Almacena la contraseña en bitwarden.

Ejercicio 6: Usa aegis ([https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)) o FreeOTP ([https://apps.apple.com/mx/app/freeotp-authenticator/id872559395](https://apps.apple.com/mx/app/freeotp-authenticator/id872559395)) desde tu móvil para activar el 2FA en Tryhackme.

Actividad opcional: un sitio interesante que investigar y donde suelen publicarse muchas filtraciones es BreachForums. Debido a su naturaleza, el dominio suele cambiar a menudo. Investiga sobre BreachForums ([https://en.wikipedia.org/wiki/BreachForums](https://en.wikipedia.org/wiki/BreachForums)) y busca en el foro filtraciones de información que te llamen la atención ([https://breachforums.is/](https://breachforums.is/)). (buscar cual es el sitio de breachforum actualmente).

https://breachforums.st/member?action=login

# Ejercicio 1

(añadir cuentas de redes sociales, servicios de streaming y datos peresonales propios)

Los metodos de busquedas especiales de google son: site: "palabra", related:, info:.

A la hora de utilizar el metodo site: deberemos poner el dominion entero, por ejemplo si queremos buscar en pastebin, deberemos poner pastebin.com, en otro caso no funcionara
![[Uso incorrecto del metodo de busqueda avanzada site.png]]

# Tarjetas de crédito
Para buscar leaks de tarjetas de credito en pastebin, usaremos la busqueda avanzada de site:pastebin ademas, de eso escribiremos en ingles para aumentar el rango de busquedas, ya que hay más cosas en ingles que en español

Busqueda realizada: site:pastebin.com credit cards leaks.
URL:https://pastebin.com/vyispz9n

En este caso la busqueda tenia 4 paginas de longitud, ya que es algo bastante amplio y no hemos usado las comillas para detallar aun mas el margen de busquedad
![[4 paginas de resultado de busquedas.png]]

Si usáramos las comillas nos aparecerían 5 enlaces con leaks (de los cuales solamente 2 tienen tarjetas de créditos directamente)
![[Pastebin - Tarjetas de creditos.png]]

# Correos electrónicos
En este caso hemos usado un conjunto de búsquedas avanzadas de Google, site:pastebin.com y las comillas para buscar exactamente lo que queríamos, que en mi caso han sido emails del fbi, "fbi email leaks".

Búsqueda realizada: site:pastebin.com "fbi email leaks"
URL: https://pastebin.com/dwj5BsVU

En el caso de esta búsqueda ha sido el único enlace que me ha aparecido
![[Busqueda de correos del FBI usando metodos avanzandos.png]]

Este es el leak con los supuestos correos de agentes del FBI.
![[Pastebin - Correos del FBI.png]]

# Ejercicio 2

![[Check de correo - waterlolbusiness@hotmail.com.png]]

![[Check de correo - waterargentino@hotmail.com.png]]

![[Check de correo - valladaresgonzalezpablo@hotmail.com.png]]

![[Check de correo - water111polo@hotmail.com.png]]

# Ejercicio 3

![[Bitwarden - Pagina de descarga.png]]

![[Bitwarden - chrome extension store.png]]

Crear cuenta en bitwarden.
![[Bitwarden - Creación de cuenta.png]]

Una vez nos logueemos veremos esto:
![[Bitwarden - Primer login.png]]

Bitwarden tiene una serie de pestañas las cuales son:
## Pestañas
Que nos indicara cuando tengamos alguna notificación en alguna de nuestra cuenta (asegurarse de que es asi)
![[Bitwarden - Pestaña.png]]

## Caja fuerte
Donde nos apareceran los correos que tengamos
![[Bitwarden - Caja fuerte.png]]

## Send
El cual sirve para enviar un correo electronico desde el propio bitwarden
![[Bitwarden - Send.png]]

## Generador
Sirve para generar contraseñas automáticas con las características que especifiques
![[Bitwarden - Generador.png]]

## Ajustes
Sirve para cambiar los ajustes, como en mi caso, la apariencia
![[Bitwarden - ajustes.png]]

Cuando vayamos a iniciar sesion en algun sitio nos aparecera bitwarden de la siguiente manera
![[Inicio de sesion con Bitwarden sin tener una entrada.png]]

Rellenaremos los datos en la izquierda
![[Bitwarden - Creación de una entrada.png]]

Una vez lo añadamos, saldra de la siguiente manera
![[Inicio de sesion con bitwarden teniendo una entrada.png]]

# Ejercicio 4
![[Firefox Relay - Descarga.png]]

![[Firefox Relay - Mascara de correo electronico.png]]

![[Tryhackme - Creación de cuenta con bitwarden y firefox relay.png]]

![[Tryhackme - welcome screen.png]]

Como podemos ver el email ha sido reenviado desde la mascara del firefox relay
![[Firefox Relay - Correo reenviado a nuestro correo.png]]

## Activar doble factor en aegis
![[Tryhackme - 2FA.png]]

### Paso 1
![[Tryhackme - 2FA Paso 1.png]]

### Paso 2
![[Tryhackme - 2FA Paso 2.png]]
### Paso 3
![[Tryhackme - 2FA Paso 3.png]]
### Paso 4
![[Tryhackme - 2FA Paso 4.png]]

Hecho esto ya tendremos el 2FA
![[Tryhackme - 2FA Confirmado.png]]
