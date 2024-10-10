1 - Extracción de ficheros 
Busca el fichero Anakiyaki en la memoria de Bob. Extráelo y calcula su hash md5. Formato de respuesta: VOL{hash}

2 - Listado de procesos 
Lista los procesos de la memoria de Bob. Por favor, indica en qué momento se ejecutó winlogon.exe. Formato de respuesta (UTC): VOL{YYYY-MM-DD HH:MM:SS}

3 - La IP de Bob 
Averigua la IP de Bob. Formato de respuesta: VOL{IP}

4 - La IP de Clark 
Averigua la IP de Clark. Formato de respuesta: VOL{IP}

5 - Persistencia en el registro de Windows 
Consulta las claves del registro de Windows para persistencia en "Software\Microsoft\Windows\CurrentVersion\Run". ¿Alguna entrada relativa a Clark que pudiese ser de interés? Formato de respuesta: VOL{ruta\absoluta\archivo.extension}

6 - Persistencia en el registro de Windows 
Vistas las entradas del registro de Windows para persistencia en "Software\Microsoft\Windows\CurrentVersion\Run". Relativas a Clark, ¿puedes indicar cuándo se actualizó la clave por última vez? (UTF) Formato de respuesta: VOL{YYYY-MM-DD_HH:MM:SS}

7 - Manejadores de ficheros 
Con volatility también podemos ver qué manejadores usan los procesos... si miramos los manejadores para el proceso de DumpIt, en concreto para los de tipo fichero, ¿puedes decirnos por favor cuál es la segunda ruta absoluta que aparece en Details? Formato de respuesta: VOL{ruta/absoluta}

