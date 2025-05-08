## Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)

## Solución
Se descarga el archivo con wget
Se desempaqueta con gzip
Se usa mmls para obtener la información del disco
Se usa `fls disk.flag.img -o 411648 -r | grep flag` para ver archivos con flag
Se usa `icat disk.flag.img -o 411648 1782` para ver el contenido del archivo pero no es posible de leer: `Salted__ށeBJc$QE&$4jMKGeE^Ȥ7 ؎$'%`
Para ver mejor los archivos se envia el contenido a un archivo con `fls disk.flag.img -o 411648 -r > archivos`
Se ve el contenido con ayuda de vi archivos
Al buscar flag sale acompañado de un bash history
```
+ r/r 1875:     .ash_history
+ r/r * 1876(realloc):  flag.txt
```
Se usa `icat disk.flag.img -o 411648 1875` para ver el contenido del historial
```
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
```
Se mueve el contenido de la bandera encriptada para poder desencriptarla con ayuda de openssl `icat disk.flag.img -o 411648 1782 > flag.txt.enc`
Se aplica el comando `openssl aes256 -salt -out flag.txt -in flag.txt.enc -k unbreakablepassword1234567 -d` y se obtiene la flag

```
picoCTF{h4un71ng_p457_5113beab}
```
