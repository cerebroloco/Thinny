---
layout: post
title: "Obteniendo Privilegios de Root en Linux (Vaca Sucia)"
quote: "Gnu Linux"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

{% include image.html url="http://bit.ly/2dTLEfp" %}

Resulta que hace unos dias se publico un exploit conocido como <strong>Dirty COW</strong> o <strong>CVE-2016-5195</strong> descubierto por <strong>Phil Oester</strong>,un experto en 
seguridad y desarrollador de Linux,

Este problema se localiza en el subsistema de memoria del kernel, en el proceso de copia virtual de operaciones en escritura. 
Esto quiere decir que un atacante local podría usar esto para obtener privilegios de administrador(root).

<center>
<strong>Video de Prueba de concepto en Debian.</strong>
</center>

<center>
<a href="https://youtu.be/VyVXXsj2-v0" 
target="_blank"><img src="http://bit.ly/2e68GmL" 
alt="IMAGE ALT TEXT HERE" width="340" height="280" border="8" /></a> </center>

 
