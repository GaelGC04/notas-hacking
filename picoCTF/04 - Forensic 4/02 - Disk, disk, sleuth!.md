## Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz)
## Solución
Se descarga el archivo .gz con wget
Se busca información relacionada a sleuth kit commands
Se encuentra lo siguiente:
- **srch_strings** - Display printable strings in files.
Se desempaqueta el archivo con `gzip -d dds1-alpine.flag.img.gz`
Se abre una imagen y se usa el comando `srch_strings dds1-alpine.flag.img | grep pico`
Con eso se obtiene la flag
```
picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}
```
