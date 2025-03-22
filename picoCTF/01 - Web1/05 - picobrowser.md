## Descripción
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704

## Solución
Con ayuda de las herramientas de desarrollador de firefox se puede editar los headers de la petición y se cambia el user agent ya que el sitio rechaza todo aquel que no sea picobrowser, se envia la petición y en las mismas herramientas se da la respuesta de la página con la flag
```
picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}
```
