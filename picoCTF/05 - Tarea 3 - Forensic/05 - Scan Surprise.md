## Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/15/challenge.zip)

The same files are accessible via SSH here:`ssh -p 49997 ctf-player@atlas.picoctf.net`Using the password `1db87a14`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

## Solución
Se descarga el archivo con wget
Se usa unzip para desempaquetar el contenido del archivo
Se entra en la carpeta y se ve el contenido de la imagen
Se escanea el QR de la imagen y se obtiene la flag

```
picoCTF{p33k_@_b00_19eccd10}
```
