## Descripción
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

## Solución
Se descarga el archivo con wget
Se abre el documento y se aprecia que hay texto censurado
Se copia y se pega en un bloc de notas y con eso se puede ver la flag

```
picoCTF{C4n_Y0u_S33_m3_fully}
```
