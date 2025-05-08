## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 53673`
## Solución
Se entra a la carpeta /tmp
Se descarga el archivo de disco con wget
Se desempaqueta con `gzip -d disk.img`
Se usa mmls que pertenece al kit de sleuth y se obtiene información con respecto a la imagen
Se hace netcat
Se pide el tamaño de la partición de linux que es de 0000202752
Se obtiene la flag

```
picoCTF{mm15_f7w!}
```
