---
layout: post
title: "Escalar Privilegios Bypass UAC en Windows 8-8.1-10"
quote: "Hacking General"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

Esta vez vengo con este nuevo post sobre como bypassear el UAC, empecemos por entender primero que es el UAC.

Según Wikipedia: El Control de Cuentas de Usuario (UAC por sus siglas en inglés) es una tecnología e infraestructura de seguridad que Microsoft introdujo con Windows Vista. Su objetivo es mejorar la seguridad de Windows al impedir que aplicaciones maliciosas hagan cambios no autorizados en el ordenador. Debido en parte a las frecuentes alertas que conlleva usar este sistema, se puede desactivar en Windows 7 y Windows Vista.

Supongamos que hemos comprometido un sistema Windows y hemos tenido una sesión meterpreter mediante Post-Explotación el siguiente paso sería bypassear el UAC.

Primero ponemos el comando `getuid` para ver el tipo de usuario en el que estamos.
{% include image.html url="http://bit.ly/2gDj87P" %}


Debemos salir de la sesión para eso usamos el comando `background`.
{% include image.html url="http://bit.ly/2g6HByK" %}


Ahora buscamos los exploits para uac para eso usaremos el comando `search uac` y obtenemos los siguientes:
{% include image.html url="http://bit.ly/2fa0Kmz" %}


Seleccionamos el exploit con el comando `use exploit/Windows/local/bypassuac_injection` y después decimos que nos muestre la información de este exploit, con el comando `info`.
{% include image.html url="http://bit.ly/2gjG9vO" %}


Añadimos lo siguiente:
{% include image.html url="http://bit.ly/2g6MibN" %}
Como el sistema comprometido es de 32 bits en TARGET pongo 0 en caso de que sea de 64 bits poner 1 por ultimo ponemos el comando `exploit`.


Una vez que hemos hecho esto tendríamos una nueva sesión, comprobamos usando el comando `getsystem` y vemos que hemos obtenido todos los privilegios del sistema y por ultimo con el comando Shell verán que me ha arrojado una bonita Shell de Winbugs XD.
{% include image.html url="http://bit.ly/2fI1qvQ" %}

Con esto hemos terminado nos vemos en el siguiente POST!!.   
