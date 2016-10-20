---
layout: post
title: "Compartir Internet por Ehternet de Windows a Linux"
quote: "Linux."
image:
      url: /media/2014-02-27-hello-cosette/cover.jpg
video: false
comments: true
theme_color: 302F2D
---

Bueno esta vez mostrare como compartir internet mediante Ethernet, resulta que hace poco instale  Debian en mi Notebook y bueno  me encontré con un problema en la tarjeta inalámbrica debido a que Debian no añade por defecto soporte de software no-libre y por lo tanto no tenía acceso a wifi y para acceder a internet solo era posible mediante Ethernet así que como contaba con otra notebook con Windows que tenía acceso a la conexión wifi, así es que esta era mi única opción ya que solo me están proveyendo el internet, _empecemos_...

### Configurando Windows

Presionamos la tecla `inicio + R` y escribimos `NCPA.CPL`.
{% include url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipOfLFR5T3tJfwpWV5sJE7dapselFgGMpmpviqlD?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}


Una vez dentro de conexiones de red seleccionamos `WI-FI` y le daremos click derecho y hacemos click en`propiedades`.
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipO-uqTJ65vAxHkNbprjXPGDvZ_qlYcknUMiOPaO?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}


Ya dentro de las propiedades nos vamos a la pestaña de `Uso compartido` y seleccionamos las opciones marcadas y damos click en aceptar.
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipMYMc2X9W_cwhJeBTt5kL8na1PFP-3-VrKiFgbf?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}
Con esto ya estamos compartiendo internet por ethernet.

### Configurando Debian.

Editamos el siguiente fichero de configuración:
~~~
sudo nano /etc/network/interfaces
~~~
mostrara la siguiente ventana:
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipM_UKvvbgQU5bCCtipj8CkecR9Fxa-YECgwnZn-?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}

Ahora agregamos las siguientes lineas:
~~~
"# The primary network interface"
auto eth0
iface eth0 inet static
address 192.168.1.134
netmask 255.255.255.
gateway 192.168.1.1
~~~
Con esto estamos indicando que la interfaz haga un loopback y la eth0 se levante de forma automática, sea estática, tenga esa IP, esa máscara y asignada esa puerta de enlace predeterminada.

{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipOp01kmjHlzs9-HkE-Ev_c_Tp7JmZVIJj7F07x4?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" description="Quedaría de esta manera." %}

Una vez realizados los cambios debemos de reiniciar el servicio, para ello podemos:
1. Pararlo y levantarlo completamente (recomendado):
~~~
root@6581-Server:~# /etc/init.d/networking stop
root@6581-Server:~# /etc/init.d/networking start
~~~
2. Reiniciarlo
~~~
root@6581-Server:~# /etc/init.d/networking restart
~~~
Hemos terminado!...
