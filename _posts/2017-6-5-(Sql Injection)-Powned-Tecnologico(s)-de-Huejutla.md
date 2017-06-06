---
layout: post
title: "(Sql Injection)-Powned Tecnologico(s) de Huejutla"
quote: "Hacking"
image:
      url:/assets/images/fondo.jpg
video: false
comments: true
theme_color: 302F2D
---

Hi, antes de empezar con esta entrada quiero dejar bien en claro que lo que escribiré acá no es con el fin de perjudicar a la Universidad 
ni a sus Alumnos, he reportado las vulnerabilidades encontradas con sus posibles soluciones, que por cierto hasta ahora no me han respondido, 
es por eso que expondré lo siguiente.

Hace unos días me encontraba en Huejutla, asi que me entro la curiosidad por ver que tan seguras eran las páginas de las universidades de este lugar.


### Universidad Tecnológica de la Huasteca Hidalguense

Bueno, comienzo por una de las Universidades más prestigiosas de este lugar, así que me puse a trastear un rato haciendo diferentes pruebas de manera 
manual con diferentes parámetros, como era de esperarse en un par de minutos me encontré con algunas vulnerabilidades que me permitieron entrar 
a la administración de esta web.

{% include image.html url="https://lh3.googleusercontent.com/TT-t_RfK4bQg6VbUm6uLq1dAB87lTE4Pa5cpvXf2pRqe3h_-eEBhmbkUEQ2lASNlInaw8wZPsuaAV5kFwwyLZ8xjDuuTXRdneiQKOA3fHygL0KzAIfTHCc1AOvbYxmew8L_DVmz2D-QsdnEAwAudf2rsahjLuBAB-jE39xdjx4CSQ0v3fsmuRiosZXfRgYF-WUCf--O1ee7x6yJ3q-FbsOXMa9a8pRQwilF4aeTL8-nKe_67puNPoM0VQ-e2VBt9eyxTMgDWy_wWh0r-MmQbYALu6AFbfYwk-VjuuoxCuSup3tebSfKRE5FaynYNf5vPNxoYLyFsUUBd2XTPAg_kA4SwSfxkVDc24LR2JMrCc0LFwGRc84GKw49V6W-2ifpmxvAvniLd0scq3H-F6QxV7oLYO4n2jNSE2opoEiKpqs2dxhO4iDofOzpGwU-At8mo19PBO1110xWB3SWmLvFSbWdCrOC87th0wwtAkqSvLTmB5if_9K8qqc1gr35Cj_O3dhNESlII7-E8dOBWpU8xd9fcOoUd54U9gjImAFtvkgTPV-1eCT8Tsh7ysDO_fHwLWB2-zDvcaPgJEdFOgsIdhdtIcXetPVHcKhKNTCvZR--8TBk-DIRc=w1196-h672-no" %}

{% include image.html url="https://lh3.googleusercontent.com/CpqMmge04jflu9Kw0hDrjVMNnIC41dV5N7qJL8hwtZd2v3bZ_-P35L2VtK83BwbiOdYvurFdaeVNZeh4vImRnB6iEEQTWrvR-Iff7IhspPxdivk2FwIsSC1UE3nX0aODZX9emPB-xzqZ38EhZpy6L8fB4apTqqjwt9hkh6PgMgk4L4Qchu8CuvCjsyhpn5mVk8HszXPcQPHGq4nNX146NTusM3QXDrWzWSNqalV28Wi4Oo-VEGNREtyoE8SJH7wVrq1Q2kdb6qU0lMkpLgo0mhHayIEpaIccPolYRdS796ch2aUL8e9KtHBl9q3wkU7ylfBbUd1lpuj9-x831TCfLJ5j7wJmY8QV6NAj6XFXEFVqcRETPccD4-tXX65nN-79NGrzadgUbzmKoVIh5fh5Zal-bwUdseZikEk7HHUsB1M2innr7PctolwFy6AFlsXAXdfKnHZB0bRPwTor9fYeY-kTw1wPeyjbpQ5u93bv3GPpDu5pVLdnN5P9ODBsV7xVJQ4oUXtbeEQmGiwgPJQHb8-WwLsoWfV6Vbqdq1Pq3s_NOPM8CammzKkKoA61N73704UedWOJP-tXhLoU218PfDEJWcQUiFrp0wktrcQng0eygrqAQIzP=w1196-h672-no" %}


### Instituto Tecnológico de Huejutla

Continúo con el segundo tecnológico en busca de algunas vulnerabilidades que puedan comprometer a esta, Bahahah también en unos minutos me encuentro 
con algunos fallos que me han llevado hasta la base de datos de este Tecnológico.

{% include image.html url="https://lh3.googleusercontent.com/ysbEwIbYDPF-03EgCeVa5-f6YbpxH2LXiWaoJhjq62_U_NdOdAKuKHYg_tN7ywWsjB-3STnAd8-kbMl_wJtfrpUHRBaAiAQstM1_4XBpaCmHJgRBBqy9s1FZOivJWsEQ3a11XgL-tbAYSYlWLiPuqkwOZjaLhFZztIt8Zyen5XXQoPRk16LUkkml4TPXe2mNoBBBsTkVJOExIwOCHfj_l4MgxUBWDsCNsR8OptTTBJAjgUnSvPsLcBJT21fHn4R6m9FgDJHmVCQUJ9UpQ1sUy9XH8iHv-3jexSFBOSUGi8n5vvwqcjqOHIaVEFMgASXiVa-L7LIEX5ie-9_S-DCtzRwO3qxbksAGg272xwILt7b6fr62A7lMrhJ1pwCtD07QTQB-NnVT3hl1rePyVJbhd2lbz7MCT8gtwWs9PWa6i4Aer-srvmGapv5esWxnLTOnoxpYiX-FyVkKXBA0ZYefjiuO8xScMlvu3P8C6Wg4n9OEL2J8CeJtpAxE1riqdk8Q_mLmETsbxUxkwN2ykRY3IxaFfr1YAMHBfLmQN9RF3WJ-nXM8FSC2ARyR5nBdTXavLmlFnwZFL7Hj39hIWnxl8OnBZuwwIuqnVnpWknlBHvXZOIVVWAu8=w658-h516-no" %}

{% include image.html url="https://lh3.googleusercontent.com/sv3OC12NWut2yIhtJvdPh_L23Aa-lefmDZsyyqx23DqyTI-BZm0bUcHnXJxR_5FEjpGB9y_tn1d0qQQlPV46QYvfxFST_SdPe0DoPl4cHxY750ltuYPLNKXVcnQzygr7o2qRR916wkDB2MzLdoCK1ws35M8roOWP1m6X9dpcfTDgnF4-n8WMaxo2ksx040PVOq3YY9gT00g3pXD3dm34BVN7djcGh3wNngRqEDafStbAvDFhSKdmRh-xZ36Eu5BKpMMykvrOa6BucD255C4Ymm9ufN46-Dud5bj3QY-KxQRE9tXN2OBMsSZUN77xFTYcD33VusGCzovKMy4fA7qSFaSqghI5HJqMiqzgvT30C14PRNVIE0J-0BdjGnp5sROLU3BLw9g77N7-85IJZEFJzb0zndW1u42CUS72FvpA3-iUPyDhGgjFgGYsBuETMdry5qawGeJHhFuGiHQcFyA1aoVnZ_G-cBGBk68ZrLXWMHMw9NoYR2CssTz9FoWGwFf_wjngkMWC4yNYROiuLkHgmAkQ3EHM_2SIDlk1O6MYW2TPG-ERPTB6l0oIsSybiVMixCYoACYKk12RX8UtKQxaX1v99yQj6bJmBIId8MXCiEPldikrM8uJ=w658-h320-no" %}

Creo que como instituciones educativas es su responsabilidad en brindar una mejor seguridad a sus Alumnos y no exponer de manera fácil toda la información 
que debería de ser (privada).

Con esto está demostrado en como un atacante con intenciones maliciosas podria aprovechar de estos fallos y hacer mal uso de estos. 

Las vulnerabilidades ya fueron REPORTADAS con sus posibles soluciones!!

Toda la información obtenida me he deshecho de ella, ya que este post fue hecho con fines informativos y educativos.

<div class="message">
“¿Mi más grande motivación? Seguir retándome a mí mismo. Veo la vida como una larga educación universitaria que nunca tuve- 
todos los días estoy aprendiendo algo nuevo”.    Richard Branson.  
</div>

Saludos By Thorrez.
