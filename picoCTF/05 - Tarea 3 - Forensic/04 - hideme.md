## Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/257/flag.png).

## Solución
Se descarga la imagen
Usando el comando strings en la imagen se puede ver la información de la imagen
Se ven directorios como secret/UT, secret/flag.pngUT
Se usa binwalk en la imagen para desempaquetar los archivos dentro
Se entra en la carpeta y se tiene secrets
Dentro se tiene la imagen flag.png que contiene la flag

```
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_dc2ab58f}
```
