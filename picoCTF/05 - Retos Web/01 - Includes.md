## Descripción
Can you get the flag?Go to this [website](http://saturn.picoctf.net:53732/) and see what you can discover.

## Solución
Se abre el sitio web donde se tiene un botón que dice `Say hello`
Al hacer click en este, sale un anuncio mencionando que este es un archivo aparte
Al inspaccionar el código html se ve que al hacer click en el botón se llama a una función por lo tanto hay un js, al abrirlo se tiene una parte de la bandera
Dentro del css se tiene otra parte de la bandera

```
picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}
```
