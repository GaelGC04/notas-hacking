## Descripción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:27177/](http://mercury.picoctf.net:27177/)

## Solución
Se abre la página web y se abre la herramienta de inspección, dentro de la herramienta de application se tiene las cookies del sitio, donde se tiene el name y el valor
Cuando se ingresa snickerdoodle se aprecia que el valor cambia a 0, por lo tanto cada valor regresa un nombre diferente
El valor 18 oculta la flag
```
picoCTF{3v3ry1_l0v3s_c00k135_064663be}
```
