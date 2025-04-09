## Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.

## Solución
Se descarga el archivo con wget
El archivo es un .wav que es como se enviaban fotos de la luna a la tierra
Se convertirá a una imagen con ayuda de la herramienta sstv decoder
Se clona desde el repositorio y se ejecuta el siguiente comando
`python setup.py install`
Seguido de esto se ejecuta el siguiente comando donde se convierte de .wav a .png el audio message.wav
`sstv -d ../message.wav -o resultado.png` 
De este modo se obtiene la imagen con la bandera

```
picoCTF{beep_boop_im_in_space}
```

## Referencias
* https://github.com/colaclanth/sstv