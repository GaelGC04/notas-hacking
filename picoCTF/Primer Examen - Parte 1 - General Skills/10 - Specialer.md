## Descripción
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 58967 ctf-player@saturn.picoctf.net`. The password is `d8819d45`

## Solución
Se hace ssh al servidor. Se tiene que no se puede usar comandos como ls o cat
Se puede usar echo .\* \*/\* para mostrar todos los elementos del directorio actual
Para obtener el contenido de los archivos se puede usar echo "$(<NOMBREARCHIVO)"
Siendo que entre los archivos, aquel que tiene la flag es ala/kazam.txt

```
picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}
```
