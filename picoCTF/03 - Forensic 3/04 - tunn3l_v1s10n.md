## Descripción
We found this [file](https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n). Recover the flag.

## Solución
Se descarga el archivo con wget
Se aprecia que está ofuscado y dentro de la cabezera del archivo se tiene BM que se refiere a BMP
Al buscar información de BMP se encuentra como debe de estar estructurada la cabecera
Se edita el archivo con ayuda de hexeditor
`00000000  42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00`
Se aprecia que la bandera no se muestra dentro de la imagen
Se busca cambiar el tamaño de la imagen para que esté más alta y muestre lo demás
`00000010  00 00 6E 04  00 00 40 04   00 00 01 00  18 00 00 00`
Al abrir la imagen se aprecia la flag

```
picoCTF{qu1t3_a_v13w_2020}
```
