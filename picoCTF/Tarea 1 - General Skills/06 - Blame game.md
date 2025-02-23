## Descripción
Someone's commits seems to be preventing the program from working. Who is it?
You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/158/challenge.zip)

## Solución
Se descargó el archivo con wget
Se ve que el archivo no tiene nada interesante, pero tiene git
Se ve los cambios en archivos con git blame message.py
El nombre del editor tiene la flag
```
picoCTF{@sk_th3_1nt3rn_2c6bf174}
```