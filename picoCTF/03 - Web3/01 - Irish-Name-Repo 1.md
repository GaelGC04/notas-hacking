## Descripción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!

## Solución
Al abrir el sitio web se aprecia una página web la cual tiene una sección de inicio de sesión de admin donde se intenta ingresar credenciales y las rechaza
Cuando se ingresa ' or 1 = 1; se puede iniciar sesión debido a que el form lo que busca es hacer que se devuelva un true de la base de datos y como recibe el true del 1 = 1 entonces es posible ingresar
```
picoCTF{s0m3_SQL_fb3fe2ad}
```
