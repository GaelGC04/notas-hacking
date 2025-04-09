## Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
## Solución
Se descarga el archivo con wget
Con ayuda del comando file se aprecia que es un archivo unicode
Con el comando xxd se aprecia su contenido hexadecimal

Se hace un script en python usando el módulo de pwn
Removiendo cadenas que contengan 
```
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83', b'0')
data = data.replace(b'\x20', b'1')

data = data.decode('ascii')
data = unbits(data)

print(data)

```
Cuando se ejecuta el script se obtiene la bandera

```
picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}
```
