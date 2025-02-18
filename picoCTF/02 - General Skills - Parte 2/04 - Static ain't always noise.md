## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Solución
Se descarga el archivo static y el bash script
Se le asigna el permiso de ejecución al script y se inserta lo siguiente:
* `./ltdis.sh static`
De ese modo se obtiene un archivo desensamblado
Obtener la flag usando el comando grep
* Usando `cat static.ltdis.strings.txt | grep CTF`
```
picoCTF{d15a5m_t34s3r_6f8c8200}
```