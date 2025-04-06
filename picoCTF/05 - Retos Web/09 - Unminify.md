## Descripción
I don't like scrolling down to read the code of my website, so I've squished it. As a bonus, my pages load faster!Browse [here](http://titan.picoctf.net:59931/), and find the flag!

## Solución
Se abre la página web y se tiene que la flag ya está en la página, dentro de las clases de los elementos se tiene la clase flag{} repetida muchas veces, al buscar picoCTF{ en todo el html se encuentra la bandera dentro de un elemento

```
picoCTF{pr3tty_c0d3_ed938a7e}
```
