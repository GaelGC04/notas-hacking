## Descripción
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

## Solución
Se hace SSH al usuario
Al intentar usar comandos conocidos parece ser que no existen
Al buscar en internet se encontró que se puede usar `${parameter=COMANDO}` para poder interactuar con esta clase de sintaxis
Al ejecutar ${parameter=ls} se obtiene blargh
al usar ${parameter=cd blargh} se vuelve a imprimir ${parameter=cd blargh}
Al usar ${parameter=ls blargh} se muestra ${parameter=ls blargh} 
flag.txt
Se usa ${parameter=cat < blargh/flag.txt} y así se obtiene la flag
```
picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}
```
