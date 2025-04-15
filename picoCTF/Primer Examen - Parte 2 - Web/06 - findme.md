## Descripción
Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:52820/).

## Solución
Se abre el sitio web, al llenar el form con test y test! anuncia que se redireccionó por lo tanto se usará burpsuite para ver el sitio paso a paso
Dentro de el path se tiene `/next-page/id=cGljb0NURntwcm94aWVzX2Fs` si el id se descifra de base64 se obtiene parte de la flag (picoCTF{proxies_al) y luego al seguir con la redirección se tiene otra url `/next-page/id=bF90aGVfd2F5X2JlNzE2ZDhlfQ==` y se obtiene la segunda parte de la flag (l_the_way_be716d8e})

```
picoCTF{proxies_all_the_way_be716d8e}
```
