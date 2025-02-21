## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución
Se descarga el archivo con wget
Pide de nuevo una contraseña
Pide `chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)`
Se transforma de hexadecimal a texto plano con ayuda de CyberChef: 4ec9
```
picoCTF{tr45h_51ng1ng_9701e681}
```

## Referencias
* https://gchq.github.io/CyberChef/