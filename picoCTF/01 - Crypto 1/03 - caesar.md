## Descripción
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext).

## Solución
Se descarga el archivo con wget
Se abre el documento y se aprecia que hay texto cifrado:
`picoCTF{gvswwmrkxlivyfmgsrhnrisegl}`
Al aplicar 22 rotaciones con caesar se obtiene la flag

```
picoCTF{crossingtherubicondjneoach}
```
