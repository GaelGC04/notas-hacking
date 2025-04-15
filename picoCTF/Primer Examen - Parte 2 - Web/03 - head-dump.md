## Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.The website is running [picoCTF News](http://verbal-sleep.picoctf.net:57525/).

## Solución
Al entrar en el sitio web se ve una página de hacking, dentro de el index se tiene un enlace a la documentación de la api
Entre los elementos se tiene una sección /heapdump, al acceder se descarga un archivo en el cual vienen muchas lineas de texto, al buscar picoCTF se encuentra la bandera

```
picoCTF{Pat!3nt_15_Th3_K3y_439bb394}
```
