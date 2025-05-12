## Descripción
RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)

## Solución
Se descarga la imagen con wget
Se ven los metadatos con exiftool
Se aprecia que se tiene un poema 
Se usa zsteg para mostrar datos ocultos dentro de la imagen `zsteg red.png`
Se obtiene un texto que contiene cadenas cifradas en base64 repetidas veces `cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==`
Al descifrarlo se obtiene la flag

```
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}
```
