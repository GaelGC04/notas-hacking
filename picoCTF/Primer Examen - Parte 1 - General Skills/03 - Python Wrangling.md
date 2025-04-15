## Descripción
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py) using [this password](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/pw.txt) to get [the flag](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en)?

## Solución
Se descarga el script de python con wget, la contraseña y la bandera
Se analiza el script y se ve que para poder ver ayuda se ingresa el script `python ende.py -h` 
Se debe de ingresar `python ende.py -d pole.txt` (tomando en cuenta que el nombre de la flag sea pole.txt)
Se ingresa el contenido del txt de contraseña y se obtiene la bandera

```
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}
```
