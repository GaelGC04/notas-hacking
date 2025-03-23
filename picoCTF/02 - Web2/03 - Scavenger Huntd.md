## Descripción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796

## Solución
Al entrar al sitio web se tiene un login donde se tiene que Joe tiene una contraseña segura
Se obtienen las dos primeras partes de el html y el css
Luego en el js de la página se hace referencia a ocultar la indexación de la página por lo tanto habla del robots.txt donde está la siguiente parte
Luego en el robots se habla de que está en un servidor apache, al buscar varios archivos se tiene que cuando se busca .htaccess se muestra la siguiente parte
Luego se habla de que se hacen websites con la mac y al buscar se encontró que se genera un archivo automátco llamado .DS_Store y cuando se busca en el url sale la siguiente parte terminando la flag
```
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_f7ce8828}
```
