## Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)

## Solución
Se descarga el archivo gz
Se desempaqueta con gzip
Se usa mmls para ver la info de disco
Se ingresa `fls disk.flag.img -o 0000360448 -r | grep flag` para iterar las carpetas
Se obtiene carpetas que coinciden con flag
```
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
```
Se cambia grep flag por el 2371 y se usa icat `icat disk.flag.img -o 0000360448 -r 2371` y se obtiene la flag

```
picoCTF{by73_5urf3r_3497ae6b}
```
