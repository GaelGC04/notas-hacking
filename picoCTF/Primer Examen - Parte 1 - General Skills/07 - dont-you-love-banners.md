## Descripción
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 56402`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 54930`. From the above information abuse the machine and find the flag in the /root directory.

## Solución
Se hace nc tethys.picoctf.net 54930 y al acceder se pide una contraseña la cual se obtiene al hacer nc al puerto 56402 que es My_Passw@rd_@1234
Luego se ingresa DefCon que es la conferencia de ciberseguridad mas grande y el nombre del primer hacker John Draper logrando acceder
Se aprecia que en el folder root no se puede leer la flag pero dentro del script.py se tiene que se imprime el archivo de /home/player/banner por lo tanto se hace un link simbólico de la flag
Se borra el archivo banner y se hace un link con `ln -s /root/flag.txt /home/player/banner`
Se cierra la sesión se vuelve a acceder y se obtiene la flag

```
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_68ca8b23}
```
