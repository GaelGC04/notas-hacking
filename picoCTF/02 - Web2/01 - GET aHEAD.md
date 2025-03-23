## Descripción
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:34561/](http://mercury.picoctf.net:34561/)

## Solución
Al abrir el sitio web se ve que se tienen dos opciones
Cuando se ve el html se ve dos forms
Uno para el color rojo y el otro para el azul
Un form tiene el método GET y el otro POST
Con el nombre del reto se sabe que se debe de enviar un HEAD como método
Con ayuda de burpsuite se manda el request al repeater donde se puede enviar una petición con el método HEAD y se ve la respuesta con la flag
```
picoCTF{r3j3ct_th3_du4l1ty_8f878508}
```
