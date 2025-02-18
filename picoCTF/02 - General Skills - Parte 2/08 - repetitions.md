## Descripción
Can you make sense of this file?
Download the file [here](https://artifacts.picoctf.net/c/477/enc_flag).

## Solución
Se descarga el archivo con wget
Con ayuda de base64decode se convierte de base 64 a texto plano una y otra vez hasta que sea texto con sentido (flag)
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}
```

## Referencias
* https://gchq.github.io/CyberChef/