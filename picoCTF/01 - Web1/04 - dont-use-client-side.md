## Descripción
Can you break into this super secure portal? https://jupiter.challenges.picoctf.org/problem/17682/ (link) or http://jupiter.challenges.picoctf.org:17682

## Solución
Se entra dentro de la página web
Al abrir las herramientas de desarrollador se puede ver que dentro del html se tiene una etiqueta de script donde se verifica la contraseña del usuario verificando sus substrings en desorden
Se arma la flag poniendo los substrings en orden y con eso se accede
```
picoCTF{no_clients_plz_b706c5}
```
