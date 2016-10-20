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
{% include image.html url="https://lh3.googleusercontent.com/XaxhdBp7MyMobIHhs-lTHPifynhZsd1xLA5T1Ll8JiRvm03Y8KYdId4PdKp3kzB3l3AkOWJLCxtfl_pJVFBaTND1u8_Cinl-MaNwaZnEQDx7OX-Gy8S2iNAUzDJwk5uBLYkcP_aQ-otxXuxX1tMdkDhuEgC7Xzm_6gwstNEN9Xp8clpprHtipk3Ic02K04RF96_y7p7gp5jwLvsW6VBLHU2bR3Jjh2qxA3kBZEVXC2zsiTvPeCs40vpHixDaMdfc1Oe2xoWCiujSuAnxN0-Xa-zBHsAiEJ52Yfre1ibj7VLnWXrIE6VFcYHU8O9ZmFAHoq2dVuSle8OliFxcsW25vvVdSuhyVHuyuyc8y6IFmIuLI9q6MICOKScCnPphsMjlWkvBerVTPsWq78qY06edQrge6sYnsBmne2CamxnleK4ZpExDVVrIajL897oqhN7-lYV3RtShIYJmUS4SfniMYEjM4WFhUTww5nzdqNxqmZ8aECUrgaxRe-qarVmg8MgHJZMMa9437ZLdSE51h2b_DU-O7v3yTvHevkeBcxTU2CPHF3KJz0zbAIlWksigmsUnbvUuJuCgY__kR4FRv-YcVWOoUtsSDiMTJj5ta5F0yeR8zjs=w412-h211-no" %}
Con esto ya estamos compartiendo internet por ethernet.


Una vez dentro de conexiones de red seleccionamos `WI-FI` y le daremos click derecho y hacemos click en`propiedades`.
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipO-uqTJ65vAxHkNbprjXPGDvZ_qlYcknUMiOPaO?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}


Ya dentro de las propiedades nos vamos a la pestaña de `Uso compartido` y seleccionamos las opciones marcadas y damos click en aceptar.
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipMYMc2X9W_cwhJeBTt5kL8na1PFP-3-VrKiFgbf?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}
Con esto ya estamos compartiendo internet por ethernet.

### Configurando Debian.

Editamos el siguiente fichero de configuración:

<div class="message">
  sudo nano /etc/network/interfaces
</div>

mostrara la siguiente ventana:
{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipM_UKvvbgQU5bCCtipj8CkecR9Fxa-YECgwnZn-?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" %}

Ahora agregamos las siguientes lineas:
<div class="message">
  # The primary network interface
  auto eth0
  iface eth0 inet static
  address 192.168.1.134
  netmask 255.255.255.
  gateway 192.168.1.1
</div>

Con esto estamos indicando que la interfaz haga un loopback y la eth0 se levante de forma automática, sea estática, tenga esa IP, esa máscara y asignada esa puerta de enlace predeterminada.

{% include image.html url="https://photos.google.com/share/AF1QipPfJLKJhFA7YsKGRGeAu7AklW989gwET0g3heib4u-a0BMeY1Rx8m-cq8IgLri4yQ/photo/AF1QipOp01kmjHlzs9-HkE-Ev_c_Tp7JmZVIJj7F07x4?key=NGVsVkllb1dKZWtCRmNoRUVjNEE1Mk9OYm4zR0d3" description="Quedaría de esta manera." %}

Una vez realizados los cambios debemos de reiniciar el servicio, para ello podemos:
1.Pararlo y levantarlo completamente (recomendado):

<div class="message">
root@torres:~# /etc/init.d/networking stop
root@torres:~# /etc/init.d/networking start
</div>

2.Reiniciarlo(Opcional)
<div class="message">
root@torres:~# /etc/init.d/networking restart
</div>


Hemos terminado!...
