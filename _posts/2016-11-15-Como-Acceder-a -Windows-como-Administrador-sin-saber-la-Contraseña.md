---
layout: post
title: "Como acceder a Windows como Administrador sin saber la contraseña"
quote: "Acceso Físico"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

Esta vez mostrare como podemos acceder a un sistema windows sin saber la contraseña, para esto tendremos que usar algún liveCD de alguna 
distribución GNU Linux en mi caso usare Ubuntu.[Pueden obtenerla en este enlace](http://releases.ubuntu.com).

Reiniciamos el ordenador y entramos en modo liveCD.
{% include image.html url="http://bit.ly/2gkaoQS" %}

Una vez que estemos en el sistema, en la parte izquierda tenemos las unidades de disco y las particiones.
{% include image.html url="http://bit.ly/2g1Urym" %}

Ahora abrimos la partición en donde se encuentra instalado nuestro Windows y abrimos la carpeta llamada `windows`.
{% include image.html url="http://bit.ly/2giZ87J" %}

Dentro de la carpeta windows buscamos y abrimos la carpeta llamada `System32`.
{% include image.html url="http://bit.ly/2gj077Y" %}

Una vez que ya estamos dentro de la carpeta system32 buscamos `Utilman.exe`. 
{% include image.html url="http://bit.ly/2giZcVj" %}

Seleccionamos `Utilman.exe` y lo moveremos a otro directorio, para eso presionamos `Ctrl+x` que es para cortar y ahora `Ctrl+t` 
con esto abrimos una nueva pestaña, una vez que estemos en la nueva pestaña buscamos algun directorio y presionamos `Ctrl+v` 
que es para pegar, en mi caso lo moveré al directorio principal.
{% include image.html url="http://bit.ly/2gkjlJS" %}

Nuevamente volvemos al directorio System32 y ahora buscamos `cmd.exe`. 
{% include image.html url="http://bit.ly/2fpPyko" %}

presionamos `Ctrl+c y Ctrl+v` (copiamos y pegamos en el mismo dirctorio).
{% include image.html url="http://bit.ly/2gknAVQ" %}

Ahora renombramos la copia de cmd.exe y le pondremos el nombre de `Utilman.exe` como el que movimos anteriormente, reiniciamos e iniciamos Windows.
{% include image.html url="http://bit.ly/2gj5x2X" %}

Una vez iniciado nuestro Windows damos click sobre el botón accesibilidad y debería de arrojarnos el cmd.exe y pues con esto ya estaríamos dentro del sistema
{% include image.html url="http://bit.ly/2geEdRz" %}

Ahora mostrare un poco de lo que se puede hacer con el cmd para eso ponemos `taskmgr` y damos Enter, nos arrojara el administrador de tareas.
{% include image.html url="http://bit.ly/2geB8kK" %}

Ir a la pestaña Archivo y seleccionar Ejecutar nueva tarea.
{% include image.html url="http://bit.ly/2fpRIQR" %}

Mostrara la siguiente ventana, dar click en examinar
{% include image.html url="http://bit.ly/2gkpV39" %}

En el directorio C:\Windows\System32 buscamos `cmd.exe` y damos click en abrir y Aceptamos.
{% include image.html url="http://bit.ly/2fpYFSf" %}

Con esto obtendríamos el cmd con permisos de Administrador, es decir que no tendríamos ninguna restricción para realizar una acción.
{% include image.html url="http://bit.ly/2fE2alB" %}

Por ultimo si queremos quitar la contraseña del usuario hacer lo siguiente.

1.-Ponemos `net user` para que nos muestre la lista de cuentas de usuario del equipo.

2.-ahora ponemos `net user "usuario" *` con * lo que estamos diciendo que queremos hacer el cambio de contraseña y presionamos 2 veces Enter para que las nuevas contraseñas estén vacías y con esto ya podremos inciar sesión en Winbugs XD.
{% include image.html url="http://bit.ly/2gfWMZC" %}

```
Nota: Ir al directorio donde guardaste Utilman.exe y devolverlo al directorio original C:\Windows\System32!!
```

Hemos terminado :D!...
