## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
Se descargan los paquetes al igual que los paquetes del ejercicio anterior
Se abre Preferences > Protocols > TLS, se añade la llave proporcionada
Se puede ver que entre los paquetes que se descifraron hay una imagen  
Se puede extraer del tráfico con Export Objects > HTTP y se descarga
Al usar el comando `strings vulture.jpg | grep pico` se obtiene la flag
```
picoCTF{honey.roasted.peanuts}
```
