## Descripción
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:61292/) out.

## Solución
Dentro de la página no se aprecia nada importante, pero al buscar en el robots.txt se encuentra un texto cifrado, con ayuda de cyberchef se obtiene el siguiente texto `flag1.txt©Ì½µå¥js/myfile.txtËì²ÈcÁë¢ÂènËÝjÉ^`
Si el texto cifrado se separa en partes se obtiene
`flag1.txt; js/myfi; js/myfile.txt`
Al buscar flag.txt sale un 404 pero al buscar js/myfile.txt se obtiene la bandera

```
picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}
```
