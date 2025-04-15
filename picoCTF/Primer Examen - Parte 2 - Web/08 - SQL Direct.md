## Descripción
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 50241 -U postgres pico`Password is `postgres`

## Solución
Se hace hace la conexión a la base de datos
Se muestran todas las tablas con la sentencia
```
SELECT table_name
  FROM information_schema.tables
 WHERE table_schema='public'
   AND table_type='BASE TABLE';
```
Se muestra que está la tabla flags
Se obtiene todo de la tabla con `SELECT * FROM flags` y dentro de los registros está la bandera

```
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
```
