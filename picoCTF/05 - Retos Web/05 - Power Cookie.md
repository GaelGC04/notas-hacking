## Descripción
Can you get the flag?Go to this [website](http://saturn.picoctf.net:60130/) and see what you can discover.

## Solución
Al abrir el sitio se tiene la opción de ingresar como invitado pero carga una página donde se tiene que por el momento no se tiene ese servicio
Dentro de las cookies se tiene un binario de es admin en 0 indicando false, si se cambia a 1 y se envia la cookie, se obtiene la bandera

```
picoCTF{gr4d3_A_c00k13_65fd1e1a}
```
