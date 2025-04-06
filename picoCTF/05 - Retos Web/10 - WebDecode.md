## Descripción
Do you know how to use the web inspector?

Additional details will be available after launching your challenge instance.

## Solución
Se carga la página y se tiene que inspeccionar los html para buscar la flag
Dentro de about se tiene un atributo de un elemento llamado notify_true que contiene un texto que parece estar cifrado `cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMTBmOTM3NmZ9`
Cuando se descifra de base 64 se obtiene la flag

```
picoCTF{web_succ3ssfully_d3c0ded_10f9376f}
```
