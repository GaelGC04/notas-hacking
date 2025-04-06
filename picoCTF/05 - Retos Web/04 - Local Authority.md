## Descripción
Can you get the flag?Go to this [website](http://saturn.picoctf.net:56498/) and see what you can discover.

## Solución
Se abre la página y se tiene un formulario de login
Cuando se envia se aprecia que no se pueden poner caracteres especiales
Cuando se ingresan credenciales cualquiera se abre una nueva pagina diciendo login failed, dentro de esta el html tiene un form escondido
Y un js
En el js se tiene un condicional si el username es 'admin' y la password es 'strongPassword098765' al enviar el form se tiene la bandera

```
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
```
