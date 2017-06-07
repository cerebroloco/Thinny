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

{% include image.html url="https://lh3.googleusercontent.com/JpLNvt-cpf7NHJKMwu4aJqH0jE5eRwfCegduAqEuFWsnRA4d2fRe1rxlg6RuATI65971SwEudSl-do1xnskPvPCpOcckzxPpO0gUK5QbfiH0hWlLQHMege-PzCvdxP62BN6ud_DcfwzSp56P8JZlX4LLfe6I9wglDg8Rn4zX9eKL7FYYiSBm3vJ38SfIP2Pudsl_gq2BLWs2PC4xrNqDY2M4tGgv7QX5dCD9by2iXZFZCMchN0CIQkqFachRMOipI2A783bNyciBWP6ZoFXjPO7OzVz9LpKpZRekLZhspQY3RBxNmnbjMidbO1DzAJ_c1FDyv2Hc97_3GTbM37MGakj7h_1Eb8P19soef7L6_cwalKtuyrVCYRKCC8a9zk2wMd9SMOZHExBQBw2-2A4FTJivVw3MeK77hCdcAnWehg7x5UO5QxA_MquiiDG6w-mevsSWTuX1P7XGjB_O0PI5dzqEd5RAByeSaQWpb35FQTRNpZU0ugWoa_FeVRQ3FTsDM9I8DL5y6DyWQG4Y-ouz2U3tI8wE9oZT56cf1S3L6IUliE4rUQAS2Y7UkDOPkDyDeIYrYWw7jt44gnpUD3-4fM5WoPmctGvuDgecmq_P-V92TlMDj2U76D5UAUdEEhkEWBCMrKoHN1ZZn9Lru4IXujHV7slvfz1Na_0NVfiOkA=w1196-h672-no" %}

{% include image.html url="https://lh3.googleusercontent.com/6QuA4qfNua9VF4y8IpbgYC80g7MwGMJQbD-4xrcwYc8I_jThkaRJNocbA5Nro9rmm7IyNGDNfYmgjL_Zj5ZdQ6phXgiGV5ba-Zc1qNx2TznKYbY1NvgYMl6rIiQax-3kCSCaHO6Upz7e-j6aNfyPGqe452xajBo5NTz6ZSK6WNefZdYtiJQuOvWJ9oMCAJS_zvv6VJqlS6QJETcjuE1t2LLm8UK7SVTlARB_YDINUw9E1Gi_FlhxRW1zCQvUj54lmPyieyELSkgil1CgPs54UWsWvjtDajzzd-RNnWVWLONgkLzDj1jcSSnR1-0KKEmjJ6DaOyqcKpMlXzfcDNP_-gy1d5s-EJTa3xkpmqaPRxF2-B6PPH77MxlSWgl7eN0gB_gwiLGtfkorVmziteeK291AhBvaMeWemmMdiuuASuTbZHfC9RTrx7H_j9qUxgUzN8vVDF_gK1Kh0848WB3cZ2-LAvifZz7HH4FSF-GgN1I1WbnKzRIN2klEa5N213rWYdT_kwjKlCXdYKrXgC-7hxU2HKS9_wHmC6w3UKH6nJxkgEaqJRBsTwhiO8cgKHR_ORXQq7n2eZpxncdvxHn_16SQNWZ9Yyd5efo_KA6M5rsC_qbTFDnJy5U4KB0fZaQ4ce8Y_dGwr5Laj5qb5W1sWI97VCmIqhm6rwmUGox6pw=w1196-h672-no" %}


### Instituto Tecnológico de Huejutla

Continúo con el segundo tecnológico en busca de algunas vulnerabilidades que puedan comprometer a esta, Bahahah también en unos minutos me encuentro 
con algunos fallos que me han llevado hasta la base de datos de este Tecnológico.

{% include image.html url="https://lh3.googleusercontent.com/qjQq4J1Rr5Zo8yyiDF-p7HS9O4BlujS5foVaMwyPmx2VwQkp77sZHT8Lt0M_FfnRYXKQJEni6GR7dE6vSvFiqLdXWpEnbeyee6eS56pF9yVMDwqJEYoHNbWkaFEBugF8WBftNKNQKo__AcwHiP7OBLzENIYcSEX1XjOUWAdQ2bFQrbfLQ_wokEn3bI20PpkFN6dWTAIJ8IzoKX5fV2TgTv-255AszQ3lvGh5O_kHBJGlz_L1mlyG_Hzx12YjgBpNGJE5X36SWm9kYvJMNf4HCsb3Ba3aetDC-IjKCBEgLzV35yOEDT5acDZxDSAyIGMvD9kUcZDjeK1mCwLxkuDXHuvMjk0LtiSsu3xXierMkTZUvmNy6vyutL_C4QpFn3mFDcdxq7iK8aKLm035tQUYserY9vboUIQnlD-NZtOT-WCYThgPCTr-b6bsAWFy36znG0iwxBSd51yxmh2ssUnpz6wbt-tPmIYEjEPkgdGWCU8Ea7P99R6AsmFNjxKnzCvLPNQ6oJRvoKxuPDIji9ONipiMFXCKAV_zjbTL8K7O5bNlRglW4JN5rb0d5xWuFxnFPaQQlowGXQfwd3T6z9o0327a93O4kocx-_2H-sxpquVroN40b_fbF2NtKCaKNRp3exyz7k2qIecCx4Ewn-gQEHNweiDsBKVco2TSAsCn_w=w658-h516-no" %}

{% include image.html url="https://lh3.googleusercontent.com/SUhYNxUEfmWzQBvIq9uiZv0q4AA7KeF_x2UAnMIDFr0kleGK0aJIrm1rmREeIw6tzcw5SZvePUmWWK8jv7yGQ-bNOdzD5wzT5usDhj8YpPV1AwYlQRYgimI9MqP8dv1hZLEP9wH5nyyktEGswzd5qbaeEfSWYbY5-9HNRJXPh477aTqRVFO7j3Vdi8HLZO59kc27r9wW3wZ0Qw0s45bjyHHU3Nnx1jAbS1qyIX-JFi39o77bcR_5cQzplrbOI-flug5a2vFtLOycLFul34ojoB99bE89jin3_YnxFXDlfA54_CjtCYZhlEOj8164Adeg3SJ2Ubjya-qqKGMIz6D-MijWZJesHuXyLoeEYcxN3t0fJJ_9kNZ37b2WE8tR8LjgY1hooIviEXeTwjRZgaBywRXwJwmT5n_2v7EoZ8e05fn3B05mMcVhB03rYjTW2gufgnTr-kFu0qJ5thLgEyxxeZskH2FiLOmniz0ss9M22GUS9oYqW80MrqP-JonepVZttnf6q0IpHc9N5LG5R7ZeOJlqkVG1Hzpx1YAL58lb9GarVgGzlEdT8Ym4TE0POK5uKt9YzeqHqd7WQ-MyupM2NXqSjo6UcLg5i_tXJ-7tf6z6vWT8XFlR1sD28ahW8AR8XFzcEmw2mBFMaPygw_mYTcUS0tOukwcWDB5wc0ggdw=w658-h320-no" %}

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
