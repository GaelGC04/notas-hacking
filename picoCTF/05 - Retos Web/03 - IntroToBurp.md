## Descripción
Try [here](http://titan.picoctf.net:63631/) to find the flag

## Solución
Se abre la página web donde primero se llena un formulario de registro, luego pide una segunda autentificación con un OTP, si se usa burpsuite se puede interceptar el request y se borra el campo de otp obteniendo una página de bypass del otp con la bandera

```
picoCTF{#0TP_Bypvss_SuCc3$S_3e3ddc76}
```
