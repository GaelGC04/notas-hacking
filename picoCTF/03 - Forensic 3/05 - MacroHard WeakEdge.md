## Descripción
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm)

## Solución
Se descarga el archivo con wget
Se aprecia que es un archivo de power point (pptm)
Se aplica unzip al archivo
Al buscar dentro de los ficheros se tiene una carpeta con un archivo llamado hidden el cual contiene el siguiente texto `ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ`
Al descifrarlo de base 64 se obtiene la bandera

```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```

## Referencias
* https://www.base64decode.org/