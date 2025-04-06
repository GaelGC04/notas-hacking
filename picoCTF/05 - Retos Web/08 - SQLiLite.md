## Descripción
Can you login to this website?Try to login [here](http://saturn.picoctf.net:64928/).

## Solución
Se abre la página que contiene un formulario de login
Como el reto consiste en sqlite se ingresa `' or 1=1;--` para obtener true
La flag se encuentra escondida dentro del html

```
picoCTF{L00k5_l1k3_y0u_solv3d_it_ec8a64c7}
```
