## Descripción
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.

## Solución
Se accede al sitio web donde se tiene varias imagenes de banderas
Se aprecia que entre todas estas se tiene una un poco diferente llamada `Upanzi, Republic The`
Se descarga la imagen con wget
Se usa el comando stepic con los parámetros -d (decode) y -i (archivos) `stepic -d -i upz.png` y se obtiene la flag

```
picoCTF{fl4g_h45_fl4g00518d32}
```
