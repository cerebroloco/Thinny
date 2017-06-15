---
layout: post
title: "Credmap:THE CREDENTIAL MAPPER"
quote: "Analisis Forense"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

Hace algún tiempo nos reunimos algunos miembros de la CUM, lo mejor fue conocer a grandes personalidades de la seguridad informática y 
convivir de cerca con ellos, bueno pues uno de ellos era el buen Ligthos. Asi que hablare de una de sus herramientas llamada 
Credmap. ~~Gracias por lo consejos sigo dándole duro a Python XD!!~~ 

Uno de los problemas más comunes de los usuarios al momento de registrarse en un sitio web, es la reutilización de contraseñas está 
demostrado que es una peligrosa práctica que facilita de gran manera la terea de un atacante, por lo tanto siempre debemos concienciar 
en el uso de contraseñas distintas para todos los servicios web que usamos.

### Credmap

Credmap desarrollada por R. Salgado a.k.a Ligthos. Es una herramienta para verificar credenciales en varios sitios populares de manera rápida. 
Esta herramienta es útil durante pruebas de penetración y análisis de vulnerabilidades para automatizar la identificación de 
reutilización de contraseñas. 
Fue presentada en Black Hat Europe 2015.

Su instalación es muy sencilla simplemente accedemos al repositorio y descargarmos:
```
git clone https://github.com/lightos/credmap 
```
{% include image.html url="https://lh3.googleusercontent.com/SxDuYhmGAuJ3xRSumLaUddFDBpNkQQTbxw-gSYzpKTG5xvgrmm8lSnzv08DsLHzwgGqeRRv8R7euUv048ZlmcV5XOwbbuS6UFb-LRC1z4iMqNU7xFQxUYIPt72KGPoZ-1jcc6VVbNpYpND09YzyfqXA9uruDD-TeGqGM9RT5nOJ6lMYMllhhZudeFAmtVQkjkHwGcYufpS-JlMTE-VAVd0pQ3pY4RaGRzO2bCYT5_it7CUTpvkgx48Pbou27wU_-GW3DF66k9rCcciO_Dg8wGLErf_wDg8O8NdsDz3yB-N4sW6M2-SoFD9LZMBOs7Zhg1dZbx5uK9WWEt5L5poSemLD8QNKDgQfvc7Fz82H0U6ZyqXpdI6B21axhhxA43yNRmaFP97F1NyQwrtM5O3_6_JaRUhIwVtPQ_20IyQbjAaHVsTB8nQhMRujekAkPslMK5fHGfUbss5d8mYn4RJVYi1ziA-p5q0Arb5a7kgVpTr4IV19BG6m3VMWR-uBNqBjTAAEC8ymQT8oSdojNgDpxzNxQWhLmvu3UmpIxjahUTzLLNs1u74zj5wwQ4IeIQKFIJMDLjwpKXYxPJB9aj8dwQj9wVpNia5OXJJeu9vthfTeU9rGoX3nalWKpF5-qORbLfUYvyKLTSI1IS8SakK155xYMAJS0VyizOCilRBc_aQ=w656-h198-no" %}


Para ejecutar credmap, sólo ejecutamos el script principal credmap.py –h para que nos muestre el menú de ayuda junto con algunos ejemplos de uso.
```
python credmap.py -h 
```
{% include image.html url="https://lh3.googleusercontent.com/SwC9Oe28T5YE_yVMcv3toITVmqpGhq3dJ4j963aT915saMOk06rIDXnL24EkdFHnVfNFSt7CDBIV8R9NYpIK_dYB5iKBzUlzN_SO48Ny_OaJa5Zi818Xegzd_5J-mIwPk0p47HUnvoelUKnlhBZ2L6djSV1Vl-07C94vWvjKAtTPPPK-5jsplaTqUQxbv6q26Tp3BCPsCcAu8AjVLu2jykGw6BnmiobuuG7MPV0puAdUBp8hfK6Yw3VOubyEoRo4ltdUc6Ds1dkvl2AljDvxMloUkSgVexgHJ1SW5AM_E-f3seffVLGOq7TQmXh0JUkc5BkHKU-npTjtob7E2lO_3nVFqabUol7XTu46YtttHZ-6akjF64TzaO1wJLruRURaU0Cm-OxdBm5v89gs3qvnNWtMQwpL5ZORRhrahdr9nOpgXVmQMNt38TfBxINe4bF1JPVi2McAhEVNBoZjk21uvIU9ATkpFMDyI8rMznYu8QEf3QOeYLNX4JtMdOr3abbkJYFVRKgHOYNhhYN_g0G-ffq3wAdFRlYelKey-k-wvHnXgOjfqJwMvOxqJ8NZTm1qDSAOef7QEL1hQALWuxCJ8hMASNbwS5MgV8zb4gJ71cFCn_C_1K0vmUCnIX5Tg5QToJr1-3xmTkyb_IeLTIBHdvwHJEjQNMo478JtnuJsSQ=w728-h672-no" %}


Credmap en acción!
```
python credmap.py --email hackerman@gmail.com --user hackerman@gmail.com 
```
Luego pide alguna contraseña que se usa.
{% include image.html url="https://lh3.googleusercontent.com/eYzAxauumB4tT0RkI09mj3QdcQ03Z28S4aHhURjb8vLONNHcChXdGkT__-WXDechaHw_oOVU9biEEG6I_ncOHC3Z8FrColkkIbl6UwuH_Mpt65qsDIjLFg3M1hWDm5OJt-W8YA44eCIrv2G6sY23SZAr4Opbr1FmY8P29rKEi1GqM84ZVa1xWK1TyOhVvnJZpk8wg-j_yDtiTTjk2FWRkAEcjrEO5uz87W9fNh9fqPz8pKggDRARHjqRsvm9qLQJwkFW6QLGbaUPzq8UOK2PgHtG2aSbxcMt1rjlCHZxu4ZQQ5X2FrERbYY3YWlBl3NIWW84f1qomW92Ist06GLV887D833Sh3UkmrFGRuOtqwtvSLN-eIcZ0ORGsqrOlG407hYfdAAoeIncBD-s1NAKhSknfZyjOl643sy--s4A1WdXVbIoopH5XCopm_jpCmRU6d0jZM4dp6IHm1AzHRpfEj1cJAJkkAc2kOj8-9qZNaaOS41w3EKQalQTm650CXxSMzHD-5RCWOUQ_W1EICmxaP_g9bCbiEqL6r_5W-wUwzy925i_1LQNd6Zeum19Rl1TjP8KdLvQTGA8QEkm-9PQ-8yzXbLRE4expvN8h9dKgiJEiOJbppWxUvc9efs9CPmUKURavq4K7ebG5P0gNQrW4FsQGRSA3PHFFYZS9Vnoew=w658-h412-no" %}

Comienza el proceso de verificacion en diversos sitios para ver si la contraseña que usa en ese sitio (Ejemplo:Instagram) la usa en los demas.
{% include image.html url="https://lh3.googleusercontent.com/BItt8u3O51cDdQYPRtXsW2r1S9FaOdeNPLP6wUQfyljSYQjUcGe7d9In4e-Ek8Zz1yOLknqM858i5jxBZ5oLK0KXd3_MjFdPXra3-NmqqhcJGBSwZjCgTQ7TogCI-N9mqNXOZHinWMzKXgppfqQongONTm_Uv-NZ758S1D2fBiYaqWgGMZ4HXwXaDHoX-6iguR9bcDAJt0P3tXkj-vdGytQD-Iyxq3HLSUryYYloBAFdQbhGsXvVnm7cj4Kq29RVpNAo9sihBqaQ5ZE8hVhFu80t1f_JazyFu0-Q_i_upqkVFTtAF3MA8-SZpkxxBP9bslo66D4bpmXxXSDNDKAXxGPB6_y4Vei8Z8KR_MfbufnD_2eK6XmC7mV8j6qXIrbCHrPHoEuuJve68EO-62PGXslvLcV2Iq4av4IENzUNMKYiUNnkJO9qIaGHmQyg4907AVv2xRM1wvs-LdIC0pfRFo0R3m_Ygbi10VQGnZDueTzz9Y3ec4VJ5yBMg3LDsC0hkIP3JkE_tEwZdsY8y2_G_UFvzjBrNBE4w4WJ4uB94cm0Hm_Vgh_FCMiY4yNXsVn_bGXsTCsvnQPlN28YuwT1SzwrFOXz0J8XxnEHJGHFdEaJbYO7umE1FkwItNXLuMPELxUFv1fW4fl37g0AJcs6N_6tNBC5M_W2aeu3cli5xQ=w658-h412-no" %}

Nuevamente Gracias Ligthos por cierto una herramienta excelente !!!!

By Thorrez
