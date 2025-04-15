## Descripción
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 65533 ctf-player@mimas.picoctf.net`Use password: `84b12bae`

## Solución
Se accede con nc y se aprecia que no se pueden ingresar letras
Se ingresa * como wildcard viendo que blargh no es un comando, por lo tanto se obtiene el directorio blargh
Cuando se usa \*/\* se devuelve `bash: blargh/flag.txt: Permission denied`
Por lo tanto se debe de imprimir el contenido de flag.txt con algún script de lectura de root
Un script útil puede ser base64 de bin
Se intenta acceder con /\*/?????? pero hay confusión por base64 o base32
Se ingresa /\*/????64 pero hay problema con base64 y x86_64
Se ingresa /\*/???\[!\_]64 para negar la barra obteniendo base64
Se usa el comando `/*/???[!_]64 */????.???` para cifrar con base64 la flag obteniendo: cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV9iMGQ1ZTg1NX0=
Y cuando se descifra se obtiene la bandera

```
picoCTF{7h15_mu171v3r53_15_m4dn355_b0d5e855}
```
