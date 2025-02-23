## Descripción
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/136/challenge.zip)

## Solución
Se descarga el archivo con wget
Se aprecia que tiene un archivo .git
Se lee el archivo y al parecer la flag se borró
Por lo tanto se ven los commits con git log
Se regresa al commit donde se creó la flag con git checkout 87b85d7dfb839b077678611280fa023d76e017b8
Se lee el archivo con la flag
```
picoCTF{s@n1t1z3_ea83ff2a}
```
