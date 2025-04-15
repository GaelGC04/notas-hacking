## Descripción
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:50164/) and good luck

## Solución
Al abrir la página se aprecia un inicio de sesión, al ingresar cualquier credencial se obtiene un mensaje diciendo que solo importan las cookies, al inspeccionar en la sección de aplicación se aprecia la cookie de secret_recipe la cual contiene un texto cifrado en base64, cuando se decifra se obtiene la bandera

```
picoCTF{c00k1e_m0nster_l0ves_c00kies_DE7A5E76}
```

## Referencias
* https://www.md5hashgenerator.com/