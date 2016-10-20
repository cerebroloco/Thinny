---
layout: post
title: "Compartir Internet por Ehternet de Windows a Debian"
quote: "Gnu Linux"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

Bueno esta vez mostrare como compartir internet mediante Ethernet, resulta que hace poco instale  Debian en mi Notebook y bueno  me encontré con un problema en la tarjeta inalámbrica debido a que Debian no añade por defecto soporte de software non-free y por lo tanto no tenía acceso a wifi y para acceder a internet solo era posible mediante Ethernet, como contaba con otra notebook con Windows que esta tenia conexion a wifi y mi unica opcion seria compartir el internet mediante ethernet ya que no tenia acceso fisico al router, _empecemos_...

### Primero Configuramos Windows

Presionamos la tecla `inicio + R` y escribimos `NCPA.CPL`.
{% include image.html url="https://lh3.googleusercontent.com/XaxhdBp7MyMobIHhs-lTHPifynhZsd1xLA5T1Ll8JiRvm03Y8KYdId4PdKp3kzB3l3AkOWJLCxtfl_pJVFBaTND1u8_Cinl-MaNwaZnEQDx7OX-Gy8S2iNAUzDJwk5uBLYkcP_aQ-otxXuxX1tMdkDhuEgC7Xzm_6gwstNEN9Xp8clpprHtipk3Ic02K04RF96_y7p7gp5jwLvsW6VBLHU2bR3Jjh2qxA3kBZEVXC2zsiTvPeCs40vpHixDaMdfc1Oe2xoWCiujSuAnxN0-Xa-zBHsAiEJ52Yfre1ibj7VLnWXrIE6VFcYHU8O9ZmFAHoq2dVuSle8OliFxcsW25vvVdSuhyVHuyuyc8y6IFmIuLI9q6MICOKScCnPphsMjlWkvBerVTPsWq78qY06edQrge6sYnsBmne2CamxnleK4ZpExDVVrIajL897oqhN7-lYV3RtShIYJmUS4SfniMYEjM4WFhUTww5nzdqNxqmZ8aECUrgaxRe-qarVmg8MgHJZMMa9437ZLdSE51h2b_DU-O7v3yTvHevkeBcxTU2CPHF3KJz0zbAIlWksigmsUnbvUuJuCgY__kR4FRv-YcVWOoUtsSDiMTJj5ta5F0yeR8zjs=w412-h211-no" %}

Una vez dentro de conexiones de red seleccionamos `WI-FI` y le daremos click derecho y hacemos click en`propiedades`.
{% include image.html url="https://lh3.googleusercontent.com/N2DXZBqJM7b8lT4iq6ybyg49PYPrO65WSPB1V_IZZm0We2lVeh3cjtETyvCVbS3hfcEFkKSHLGtiLuxswK_7CVVy6osALZWjnsXWmJkdyAbMWJd2XSzlMhWTphBp6CJ99mBmUoL7nlS3wncPCtoQOTgwkM6ASX0oSn1QqIjaG0dU_n9oo_sOx0voDYN9aHQD30A-26gK1ElBBygu7-DJB59Lk6R9RY8xuaAiFvLnddzCNkUsvZcxHrEwrXAHoVduNZjJV-Nw2P9oYYVcnM8ZBxLjG7_lOuWAgHqtKnTLzVYUwLLTBUz4pgcRmC4U4r_8g86o8aBmxoDcDQ_voU4r9xdDYydNFYsV307avoSZdiu-hexhDRMAuFm6uGC6fmlLquPDQfJuMqAv3iecmTCnCNPmPsyM2Zu3Y1v4bAWgPP-oJGe0h8Il9T9QbCa-Ze9wS7K5T9GT-4g3IkMIow-2vzLyCpeBCagXCacHixfronIIc-WZwhZ8tg2pfL1LN5sgk5k7MSNsyY1vYTq9eTlMxhAe6gR_3XoiOF4yaKP2V6JixtWru9iO4z6YxWr6e2_sf2Z5aXqrfev-3FQ-Df_bIpi51ZQFP4Cu31JIo9-jbhyjje4=w786-h438-no" %}


Ya dentro de las propiedades nos vamos a la pestaña de `Uso compartido` y seleccionamos las opciones marcadas y damos click en aceptar.
{% include image.html url="https://lh3.googleusercontent.com/hSS95YzIjtE_GB7VlQZMx3zHCWyxaZlBSuXAm1ZXCZTc2oBXIu4Va4SSEjHcAJsBh2UEk-yXWTsUKnv3p6iseGdbYDudni_wNA7lTyJbDKfuOxC63JXyyDIKTn0kSAZ3eVxH2DUP9UvN_fkCh4N18NgNADq2FLKTsH-aCr4Q5HlUcs5--y4-5UNAUtgNxU2quGJaIRa_jNN85aZBJsOV6bYXRZQ6OozVTSSu7VRIjRQrQ4smcXZGEWhugshYQZboSK6fzATQ-5gqtqymH_XqGMSHY4MqRFbLDXh04uxTAm3-BamWsGK6e6QhTKkeMyrk0I0b-YbMr5hxLRvAFUZBuNOYNadXr2EHrzX13hga-kXoFPVWmavG02uPofJFlp5iI2rYNf_hb7j6oFtX166liokTiAEPFIGZvI2jjG-Ka8h3xH2kMY6xW_F_7OfFbr7n4OYauknTcOKYWmnEseidYntRnVqtBNFky0EjiBT3rH-5klD_EmjAWkl_SUmXPJJl60JzFxN5c7z6a4xx40BwKiQGUrFKeWBMO387otF6JfRMFX5KGiRj31vVxUCIDQCMeD4kKbfAEvf1I_CYJ1s6nGE5WJyjPTXZHBHNzD7m0jUELpU=w376-h472-no" %}
Con esto ya estamos compartiendo internet por ethernet.

### Ahora Configuramos Debian.

Editamos el siguiente fichero de configuración:

```
sudo nano /etc/network/interfaces
```

mostrara la siguiente ventana:
{% include image.html url="https://lh3.googleusercontent.com/Bq6_XdBUPjflc-OuN4sgcfJm_TrITQldlI4iIPjAMFRzoh832qLt0EduS2JMBqT9d4Z06JTSeI-BCPvo27JjDrXlUsCnR6cGTeGsU-IveKyW0_BfN2rJXdg0I0JmQYEwpajbF2IW1Bo1SXjI0Z5-Iqx8VbVZl2ltBblXJ9SXjLbdHWcwbvmNSfWM_B2eJd5nhihOqgQBNf6Avk1J1Vtr0JZ-Jyx1Yni1H8b2_u8R_fxcALsw-ZkVjloXgM6B9UK-ZfWzLK-skFHQ3jGwsp0rfjbyxtfbX4lfuozrnIS8INFdSfJjDZwgj-DPL_L2I6h9vXiZx6sddrai4MuU0R6Ku-4bcf0GLtX5b5nd2LK0E6CMXITAMYeuxGKfp5nzd0JRfK8yndhNTH4NARzwMvb6OM79A4vPXvjDViju2Ny3tKOlvQM8Ud7JyDoJWS5swFoEXXBYKTlS3oCLb5Rq-k2TaflNil8PKk0F9RYIQzzyOlma6oVb_5IIDuJeiXoI9FByKkBiM_A-xQATgkBfvcCo7jaxKuYEcHXvpuJBHcDf8M1laQKW3qTmPVjkqofFyP9F9Zgb5oS2X2M5hH7Zr0iCKr1CgIYPBFcMBKdkTeggFXw4iKs=w740-h495-no" %}

Ahora agregamos las siguientes lineas:

```
# The primary network interface
  auto eth0
  iface eth0 inet static
  address 192.168.1.134
  netmask 255.255.255.
  gateway 192.168.1.1
```
  
Con esto estamos indicando que la interfaz haga un loopback y la eth0 se levante de forma automática, sea estática, tenga esa IP, esa máscara y asignada esa puerta de enlace predeterminada.

{% include image.html url="https://lh3.googleusercontent.com/2QJECk3Xdm0mAiFcNRSqH0yHvoYbah_1YcYS7nDawY7l7HxsksAc2dHnxx9qnOP7hXuzoE3J7-4Hts6cTAjcxxS8E5N9CRAWSPnxO9JCK3vk2sHEN205I4nV1enWrrK_gL9u2JvJtI19p7BLRWIDBEJZ0M1O4yR4uuIy7JjaaCdVOOVhsM4TTcsu3RvSe9eJVM8oCoODUpNxVGu5y9gutUb9wTEDRA8WsTG1k7A_LJy2pYl9fDt5xQ3ul-CYin5J9nr5ZJHw_h_4gQv6HiaTGM92AzHjh_zNqgZY6Aq3KnidRmyI5eIsWj98iUUgY665-IQxDOpP7o0MXii9uSXW4IVdin5_x6xUQh2h0qWtKfxsbrweMwKY0bzq4fTT_81aw9ae-pmBWZneuOxk5WZkLXh3r0aPaNWp7q9mkiGs2m6WBBAWOd76SS6y2UKbnphp1CxzqExChIVBT4mf4JuHZqxKoghuRFuCCIM4uLwG2zSvevsEv_UHHt5xNJHwKZadnVKqMFW2yuGEOPa360w7nqyzNgpGiUcCzxZeTAFW83OCTnZ8z3_ybh8lDY9LrzYenuRN_-teO6viXg2XIr5ZUgcuPaSpc0tUqVRnbz-O_Yfy3KI=w737-h492-no" description="Quedaría de esta manera." %}

Una vez realizados los cambios debemos de reiniciar el servicio, para ello podemos:
1.Pararlo y levantarlo completamente (recomendado):

```
root@torres:~# /etc/init.d/networking stop
root@torres:~# /etc/init.d/networking start
```

2.Reiniciarlo(Opcional)

```
root@torres:~# /etc/init.d/networking restart
```


Hemos terminado :D!...
