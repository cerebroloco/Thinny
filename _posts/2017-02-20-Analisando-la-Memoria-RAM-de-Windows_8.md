---
layout: post
title: "Análisis  de la Memoria RAM (Windows 8)"
quote: "Analisis Forense"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---
Uno de los temas que más me apasiona es el Análisis Forense así que hoy mostrare como podemos obtener información útil de la memoria RAM.

### DUMP DE LA MEMORIA RAM

Empezaremos por realizar una copia bit a bit de la memoria RAM, es decir una copia exacta, en mi caso usare la herramienta `FTK Imager` [Descargar FTK Imager](https://mega.nz/#!2xUUyQ4a!STKxDblF7sAshZtKoI5SzJ67UT0PacRnlXLgji2Il9E).
{% include image.html url="http://bit.ly/2mklFTV" %}

Ahora seleccionamos `Capture Memory`. 
{% include image.html url="http://bit.ly/2kU7QP7" %}


Seleccionamos el destino de la copia y capturamos memoria.
{% include image.html url="http://bit.ly/2mf5BWL" %}
{% include image.html url="http://bit.ly/2lMN0Ae" %}

### ANALISIS DE LA MEMORIA RAM

Una vez que ya hemos obtenido la copia de la memoria tenemos que analizarla para eso usaremos la herramienta `volatility`.

El uso de esta herramienta es muy sencilla, colocamos el nombre del plugin a usar, la ruta donde se encuentra el archivo de nuestra imagen de la ram y después el tipo de perfil. 

```
volatility [plugin] –f [Ruta] --profile=[profile] 
```

Para saber el tipo de perfil ponemos:
{% include image.html url="http://bit.ly/2lzApji" %}

Seleccionamos el perfil en mi caso como es el de un sistema Windows 8 seleccionare esta:
```
Win8SP1x86 
```

Si queremos saber que procesos estaban activos en el momento que realizamos el DUMP de la memoria usaremos `Pslist`.
{% include image.html url="http://bit.ly/2lh20n0" %}

Con el comando `Pstree` mostrara una lista de procesos en forma de árbol.
{% include image.html url="http://bit.ly/2mshBAi" %}

Si queremos imprimir la listas de dlls cargados para cada proceso usaremos `dlllist`.
{% include image.html url="http://bit.ly/2mf99II" %}

Con `callbacks` Imprime rutinas de notificación de todo el sistema.
{% include image.html url="https://lh3.googleusercontent.com/qS7_FEQ9wIm4o1HSK3VqvaiH--wlktSPrvOxcsZ8J11aFz3gbCbUQX7oqHIKdI5RGEibB_h1HLeL5dcpbI2UtfZPXS1AZwqRWnG2AkveVehIt107Iglc4g0RY0qxf94ptPh7QtyLstyZKzSzW9SzrVvgXf0YbmI-yaFPwrFKg2Km5aB6dT8dEW2jUygq_0-sr_A016Ash_0_1ja9e2o0P-AwqU8PXRwgcMn16m-7rm3Z_TASMkZXzzzP3eEB1wU00urhBrSkJoOg32lH4fz-DVbjABbs0c3_26_3-WhRE5EzcLfoqdJn3S02yKY1m_usFqV7NnkQlRADawPT9oxFlKpdMr1ljQV2qXVYmF76tZvv9jGLbxKVyOscG8EF8rby4-0mX5DzlHQuyjmCdGSHZPC2HMxMyv0amnk4x7QCGC7idTuBK84vyGXJm-VIBMfHL1GgiKwnp2x31S3IyEaTHCwsAjtmqF19hxuPTczjvlySfW0AAKHPWr7SVse0H6mZIgIzaCsOtNtlYLlLdMcW5OrG_ndNk2xlh_Nnd5YUocyWzAio6LZgcRkI-RK6UwJfE20d1dpEtmg-2052DgcaXsSwIm1V5EBOsVPuAA0lghF5kOF3yaVsZWjWUOwlPOBHMHGZlxZ436qS5jLvjMqc5VR3XaraWq8Qu1IJ9qtWoQ=w914-h592-no" %}

Con `Modules` Imprime lista de modulos cargados.
{% include image.html url="https://lh3.googleusercontent.com/iHMjEhPDEfYwNEZUPTjVPM_pI2PTraRHofnOifZWONVGlHJuNQo9blKoe9bdwDDmmLgaKsAL28fpt1i7Olk9ItEyDDIEaMo9MeQijeptiNQNb8C2t3D4AcBxXgCzK0nLKWGJNOuhEecv8uuoxwieeChXMk_vdXMHCXR-m7A9dxxZgRXic4wLJEB-IWuhHGUD8ub8hmLPZaTJ_bzTlDPP0SrkALmX3O5gzokrSJM1hmW5XtWwjtQDAgnXo9I_lxOHSH72uvYsX6VBewYdn97IZf74Xd_wxzqGCSNyRJHdCNnHnA4OKywBdiTM1HcQ-Z3kPF4KpWaPu135SPtBeRh9Z2d5o7QjOpg0NCEiCd_n5-FdWGozRDJ1UWs3En1BmhoIVnD5Epbw1A8966vW7mI-7Nn4g_AgZMCOBzrqI0O8hS11wsYMhOivJFVfoOMi_WoUDWRkpbKdgNc4ScpmwO9vpaJrji011SOXOxbP7GMbR4W9Vo_cvzJuMVcX11dc8cpBNMt8BASKvGHl8XE-ZLi30LIDWSuf7oDQofUAx3APZEhXqEKqdK4e2JhFp7LcEw0pggi9AGOHRbjeq86GdrTSKTMRaxfEUkQfZsoXukAZwvChC3asLvwW4UPhoZ9XoRB7c5JxAz5XoYwUYhx2vezC3-ioD6wuyAOwXUXGDHEA1Q=w914-h592-no" %}

<div class="message">
Como dato extra me di cuenta que algunos de los modulos de volatility que funcionan bien en sistemas windows 7 no todos funcionan en windows 8.  
</div>

By Torres
