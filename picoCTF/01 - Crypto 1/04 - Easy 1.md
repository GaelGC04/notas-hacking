## Descripción
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

## Solución
Se descarga la tabla y con la flag encruptada se busca la fila con la letra
Se filtra por la letra correspondiente de la key en la fila y la letra de la flag es la letra desencriptada nueva. Asi se hace hasta tener toda la flag

```
picoCTF{cryptoisfun}
```
