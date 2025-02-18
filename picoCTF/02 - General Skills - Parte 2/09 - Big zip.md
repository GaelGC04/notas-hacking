## Descripción
Unzip this archive and find the flag.
- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
## Solución
Se descarga el archivo con wget
Se le aplica unzip y  se entra a la carpeta
Se usa el siguiente comando para encontrar la flag: grep -r "CTF" .``
```
picoCTF{gr3p_15_m4g1c_ef8790dc}
```