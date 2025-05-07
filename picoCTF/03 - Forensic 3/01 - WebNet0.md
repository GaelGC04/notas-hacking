## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Solución
Se descarga la captura de paquetes con wget y la llave
Se usa la herramienta wireshark con `wireshark capture.pcap`
Se carga la llave con Edit > Preferences > Protocols > TLS > RSA List, se agrega la llave y con eso se desencriptan los paquetes
Se busca la bandera como texto y se encuentra en uno de los paquetes

```
picoCTF{nongshim.shrimp.crackers}
```
