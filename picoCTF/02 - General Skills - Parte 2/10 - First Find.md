## Descripción
Unzip this archive and find the file named 'uber-secret.txt'
- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)

## Solución
Se dascarga el zip con wget
Con ayuda del comando `find ./ -name "uber-secret.txt"` se encuentra la ruta del archivo
Se hace cat al archivo y se obtiene la bandera
```
picoCTF{f1nd_15_f457_ab443fd1}
```
