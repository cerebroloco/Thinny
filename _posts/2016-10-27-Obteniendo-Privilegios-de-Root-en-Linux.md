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

{% include image.html <center> url="http://bit.ly/2dTLEfp" </center>%}

Resulta que hace unos dias se publico un exploit conocido como Dirty COW o CVE-2016-5195 descubierto por Phil Oester,un experto en 
seguridad y desarrollador de Linux,

Este problema se localiza en el subsistema de memoria del kernel, en el proceso de copia virtual de operaciones en escritura. 
Esto quiere decir que un atacante local podría usar esto para obtener privilegios de administrador(root).


