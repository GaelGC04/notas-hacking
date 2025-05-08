## Descripción
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download disk image](https://artifacts.picoctf.net/c/71/disk.img.gz)
- Remote machine: `ssh -i key_file -p 56833 ctf-player@saturn.picoctf.net`

## Solución
Se descarga la imagen con wget
Se desempaqueta con gzip
Se obtiene los datos del disco con `mmls disk.img`
Se busca de nuevo el bash_history con `fls disk.img -o 0000206848 -r | grep history`
Se pone el identificador en el siguiente comando para leer el archivo `icat disk.img -o 0000206848 2344`, entre las líneas está que se generó una llave ssh por lo tanto se usa el siguiente comando `fls disk.img -o 0000206848 -r | grep .ssh` porque en .ssh es donde se guardan las llaves
Con `fls disk.img -o 0000206848 3916` se ve el contenido de la carpeta y esta el archivo id_ed25519
Se usa el siguiente comando para redirigir el contenido hacia el directorio /tmp de la máquina `icat disk.img -o 0000206848 2345 > key_file`
Se cambian los permisos de el ssh con `chmod 600 key_file`
Finalmente se usa el comando de ssh
Se hace ls y se ve el flag.txt que tiene la flag

```
picoCTF{k3y_5l3u7h_af277f77}
```
