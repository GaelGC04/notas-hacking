## Descripción
There's an interesting script in the user's home directory
The work computer is running SSH.
We've been given a script which performs some basic calculations, explore the script and find a flag.
```
Hostname: saturn.picoctf.net
Port:     57446
Username: picoplayer
Password: password
```

## Solución
Hacer ssh al usuario picoplayer
Ejecutar useless
Leer el código con cat
Leer el manual de useless con `man useless`
```
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5136}
```
