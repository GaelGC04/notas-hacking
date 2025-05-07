## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Solución
Se descarga la imagen con wget
Se usará binwalk para extraer el contenido del archivo `binwalk -e dolls.jpg`
Se van desempaquetando carpetas nuevas con más muñecas
Se usa binwalk hasta obtener el archivo de la flag

```
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}
```
