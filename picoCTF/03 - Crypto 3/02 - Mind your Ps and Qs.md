## Descripción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)

## Solución
Se descarga el archivo y se cuenta con la siguiente información:
```
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537
```
Se usa la herramienta dcode para obtener el texto cifrado:
Valor del mensaje de cifrado C = 843044897663847841476319711639772861390329326681532977209935413827620909782846667
Public Key E = 65537  
Valor de la clave pública N = 1422450808944701344261903748621562998784243662042303391362692043823716783771691667

Y así se obtiene la flag:
```
picoCTF{sma11_N_n0_g0od_00264570}
```

### Referencias:
- https://www.dcode.fr/rsa-cipher