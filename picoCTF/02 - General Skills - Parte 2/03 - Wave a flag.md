## Descripción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...

## Solución
Con ayuda de wget se obtiene el archivo de warm
Se convierte en ejecutable con ayuda de chmod +x ./warm
Se le añade el parámetro -h para obtener ayuda donde se encuentra la flag
```
picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```
