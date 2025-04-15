## Descripción
Can you get the flag?Go to this [website](http://saturn.picoctf.net:53732/) and see what you can discover.

## Solución
Se hace nc al sitio y se abre una tienda de banderas, se puede ver el dinero actual, comprar banderas y salir. Cuando se compran banderas se resta el valor total y si la suma es menor al valor de monedas del usuario se pueden comprar banderas y ese valor se resta al saldo del usuario. Si se añade 9000000 hay un desbordamiento por la cantidad de costo de las banderas aumentando el salario del usuario teniendo el suficiente para comprar la bandera 1337

```
picoCTF{m0n3y_bag5_65d67a74}
```
