
**Ejercicio 1:** La herramienta whois es muy útil cuando debemos obtener información sobre un dominio sin que pueda ser detectado por el blue team de este dominio. Esta herramienta está disponible para su uso tanto por consola como desde la web de domaintools.com. Haz pruebas empleando tanto la herramienta por consola como a través de la web.

**Ejercicio 2:** El uso de la herramienta domaindossier puede ser muy interesante para obtener información del registro de una web, de sus DNS y otros aspectos. Empléala, haciendo énfasis en obtener datos interesantes y analizar dichos resultados objetivos. Obtener los datos y no analizarlos no nos servirá de nada, por lo **que este trabajo es tan importante como lanzar la propia herramienta.**

**Ejercicio 3:** En este ejercicio vamos a aprender el uso de la herramienta theHarvester.

  
Para emplear esta herramienta vamos a necesitar de una distribución GNU/Linux basada en Debian, como Debian, Ubuntu, Linux Mint, o Kali Linux. Se recomienda fuertemente emplear Kali Linux, pues viene por defecto instalada en ella, y el proceso de instalación no es sencillo en otras.  
  
[https://github.com/laramies/theHarvester](https://github.com/laramies/theHarvester)  
  
Y para su instalación: [https://github.com/laramies/theHarvester/wiki/Installation](https://github.com/laramies/theHarvester/wiki/Installation)  
  
Si usáis la Kali ya debe estar instalado.  
  
Una vez instalado theHarvester vamos a comenzar con algunos comandos. Si el proceso de instalación ha ido bien, al escribir “theHarvester --version” debe indicarte que usas la versión 3.x.x (por ejemplo, yo tengo la 3.2 en el momento de escribir esto).  
  
Una vez instalado procederemos a buscar información del dominio juntadeandalucia.es en Google.  
  
theHarvester -d juntadeandalucia.es -l 100 -b google  
  
-d indica el dominio sobre el que buscar  
  
-l indica la cantidad de resultados máxima que queremos obtener  
  
-b indica el buscador con el que realizar la búsqueda  
  
  
Además es posible hacer que los resultados los vuelque en un archivo con “-f <nombre_archivo>”.  

  
  

**Ejercicio 4:** Shodan es un buscador muy potente para realizar footprinting. En esta práctica vamos a comenzar a ver cómo se podría usar en nuestro beneficio.  

  

En primer lugar debemos tener configurada ya la herramienta “theHarvester”. Con ella podemos lanzar búsquedas de dominios para encontrar emails o subdominios.

  

1. Escojamos un objetivo (imaginemos por ejemplo que nos ha contratado una universidad pública o alguna administración a nivel local, autonómico, etc… Sed creativos).
    
2. Realicemos una búsqueda con theHarvester para obtener subdominios.
    
3. Con esa búsqueda de subdominios dirijámonos a shodan. 
    
4. Para emplear shodan tenemos dos opciones. Existe un plugin para Firefox que funciona bastante bien o también podemos emplearlo desde la propia web.
    

1. NOTA: Para obtener la ip de un dominio podemos usar la herramienta “host -a” o “ping”
    

6. En la web escribimos el subdominio y obtenemos información sobre el tipo de servidor web que está ejecutando.
    
7. Ahora procederemos a hacer una búsqueda en google de ese servidor web y versión para buscar vulnerabilidades.
    

1. Por ejemplo “nginx 1.1 vulnerabilities”
    

9. Buscamos el CVE de alguna vulnerabilidad
    
10. Vamos a [https://www.rapid7.com/db/?type=nexpose](https://www.rapid7.com/db/?type=nexpose) para buscar más información sobre la misma.
    

  

Ejercicio 5: Uso de la extensión de navegador Hunter para encontrar direcciones de correos asociadas a dominios.

  

Ejercicio 6: Uso de la extensión de navegador Wappalyzer para encontrar las tecnologías con las que está hecha la página web.

------------------------------------------------------------------------
Se pide mínimo 3 dominios, los 3 dominios iniciales serán:
1.- netflix.com
2.- disneyplus.com
3.- primevideo.com

Dominios extra por si alguno de los anteriores no tuviera contenido suficiente:

# Ejercicio 1

![[Who.is Netflix - 1.png]]

![[Who.is Netflix - 2.png]]

![[Who.is Disneyplus - 1.png]]

![[Who.is Disneyplus - 2.png]]

![[Who.is Primevideo - 1.png]]

![[Who.is Primevideo - 2.png]]

# Ejercicio 2
![[Domain Dossier Netflix.png]]

![[Domain Dossier Disneyplus.png]]

![[Domain Dossier Primevideo.png]]

# Ejercicio 3
Para este ejercicio usaremos theHarvester y ademas, usaremos 3 navegadores diferentes en cada uno, Brave, duckduckgo y bing.

## Netflix
![[theHarvester - netflix brave.png]]

![[theHarvester - netflix duckduckgo.png]]

![[theHarvester - netflix bing.png]]
customerevents.netflix.com - Puedes entrar pero lo primero que te aparece es que no es segura y solamente sale un mensaje de "BLOCKED"

## Disneyplus

![[theHarvester - disneyplus brave.png]]

![[theHarvester - disneyplus duckduckgo.png]]

![[theHarvester - disneyplus bing.png]]

## Primevideo

![[theHarvester - primevideo brave.png]]

![[theHarvester - primevideo duckduckgo.png]]

![[theHarvester - primevideo bing.png]]
# Ejercicio 4
En el caso de netflix, no hemos encontrado ninguna vulnerabilidad escaneando sus subdominios, pero en el caso de disneyplus (help.disney.plus, con la ip 172.233.154.74)

Podemos ver que tiene Los puertos 22, 25, 1234, 1925, 5005, 5222, 5800, 8001, 8080, 8112, 8181, 8800
![[Shodan - Imagen general 172.233.154.74.png]]

Podemos ver que tanto el puerto 22 (/TCP usado para OpenSSH) y 8181 (/TCP usado para SSL Certificate) tienen vulnerabilidades. de las cuales una de las vulnerabilidades del puerto 22 es Roja.
![[Shodan - Puerto 22 172.233.154.74.png]]

![[Shodan - Puerto 8181 172.233.154.74.png]]

Vamos a escoger una vulnerabilidad roja del puerto 22. una azul y una negra y del puerto 8181 vamos a comprobar las dos vulnerbailidades que tiene, Ademas de comprobar las 3 vulnerabilidades mas reciente aunque no tiene CVSS.
![[Shodan - Vulnerabilidades recientes 172.233.154.74.png]]

# CVE-2008-3844 (2008)
Como podemos ver en la descripcion, solamente afecta a aquellos que hayan obtenido este servicio mediante fuentes no oficiales.
![[CVE-2008-3844.png]]

Aunque es una vulnerabilidad con un CVSS bastante elevado, no tiene un gran riesgo como tal, ya que no es una vulnerabilidad como tal, si no que el paquete ha sido distribuido por personas ajenas a Red Hat GPG Key y este contenia una trojano junto al contenido, Para solucionar este problema nos facilitan un archivo  que comprueba los paquetes que han podido ser modificados
![[Analisis de CVE-2008-3844.png]]

# CVE-2016-41617
Esta vulnerabilidad esta en varias versiones, siendo esta (2.0) la que menos riesgo tiene (aun no se han evaluado los riesgos de la version 4.0)
![[CVE-2021-41617.png]]
Esta vulnerabilidad es debido a que se pueden activar unas configuraciones (que vienen desactivadas de base) que son AuthorizedKeyCommand y AuthorizedPrincipalsCommands, debido a esto podemos realizar una escalada de privilegios de manera local. 

# CVE-2021-36368
Esta vulnerabilidad consiste en que a la hora de un usuario conectarse con una autentificacion de clave publica usando un agente pereo sin el -oLogLevel=verbose, el atacante podria cambiar a donde se conecta dicho usuario.
![[CVE-2021-36368.png]]

# Ejercicio 5
Comprobar el xk no me va Hunter.io


# Ejercicio 6
Podemos ver que la pagina de help.disneyplus.com usa las siguientes tecnologías, En el caso de help.disneyplus.com no nos aparece ninguna version de las tecnologias
![[Wappalyzer - help.disneyplus.png]]

Sin embargo en el caso de Netflix, si que nos aparecen la version de una de las tecnologias (Lodash 4.17.21)
![[Wappalyzer - Netflix.png]]

Con esta información podemos buscar si Lodash 4.17.21 tiene algún tipo de vulnerabilidad, como podemos ver no hay ninguna vulnerabilidad conocida para la versión actual pero si para anteriores.

![[Lodash - Security Vulnerabilities.png]]

Como podemos apreciar en Primevideo, podemos ver que nos da la versión de una de las tecnologías que utiliza, en este caso es core-js 3.6.5, con esto ya podemos buscar vulnerabilidades de dicha tecnología.
![[Wappalyzer - Primevideo.png]]

Después de buscar vulnerabilidades de dicha tecnología, podemos apreciar que no tiene ninguna vulnerabilidad conocida actualmente.


