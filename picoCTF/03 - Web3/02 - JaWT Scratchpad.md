## Descripción
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

## Solución
Se abre la página web se aprecia que se puede ingresar con el nombre de los usuarios siendo que no se puede acceder al usuario admin, se tiene un enlace a JWT donde se puede obtener los tokens de JSON cifrados y se pueden descifrar con un secreto, siendo que si se obtiene de Application de la cookie jwt, se cambia el valor del name por admin y el secreto se obtiene con la herramienta de john the ripper obteniendo ilovepico
```
picoCTF{jawt_was_just_what_you_thought_f859ab2f}
```
