## Descripción
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:60389/).

## Solución
Al entrar en la página se tiene un sitio de seguridad
En las pistas del reto se tiene folder
Por lo tanto se busca secret/ y se tiene una pista, al inspeccionar la página se tiene que hay una carpeta donde se guardan assets llamada hidden/
Al acceder a esta se tiene un formulario donde siempre se rechaza las credenciales, pero dentro del form se tiene un input escondido con otra carpeta llamada superhidden/
Dentro de esta no hay nada pero al inspeccionar el html se obtiene la bandera

```
picoCTF{succ3ss_@h3n1c@10n_51b260fe}
```
