## Descripción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796

## Solución
Al entrar al sitio web se tiene un login donde se tiene que Joe tiene una contraseña segura
Al ingresar con cualquier otro usuario se tiene una sesión, dentro de las herramientas de desarrollador se ve que en las cookies se tiene el nombre del usuario y si es admin
Al usar la sección application y se cambia admin de False a True y se recarga la página se obtiene la bandera
```
picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}
```
