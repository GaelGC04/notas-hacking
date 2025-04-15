## Descripción
Can you win in a convincing manner against this chess bot? He won't go easy on you!You can find the challenge [here](http://verbal-sleep.picoctf.net:57518/).

## Solución
Se abre la página web y se abre un juego de ajedrez
Se analiza el funcionamiento del web socket
Se tiene la función makeBestMove() y sendMessage()
Cuando se envía un mensaje el enemigo responde a partir de la cantidad que se de en el string
Cuando se envia mate 10 empieza diciendo que va a ganar en 10 movimientos
Si se envia un eval con un número negativo el enemigo cree que perdió y por lo tanto devuelve la bandera

```
picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_c0789e29}
```
