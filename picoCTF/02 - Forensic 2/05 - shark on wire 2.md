## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución
Se descarga el paquete con wget
Se usa la herramienta wireshark para ver la captura de paquetes usando `wireshark capture.pcap`
Se abre la ventana de wireshark y se selecciona un paquete udp y se sigue su flujo
Entre el flujo se encuentra lo que parece ser una parte de una bandera incompleta
Se aprecia que del paquete 32 al 60 se tiene start y end respectivamente y comparten el puerto 22
Los puertos en los que se envían cuando se les resta 5000 y se convierten a texto se tiene que son la bandera, por lo tanto se tiene que descifrar con scapy
Se genera un script que guarde los caracteres dentro de un string y que solo sean los caracteres donde el protocolo sea UDP y el puerto sea 22
Además se verifica que el puerto de origen sea mayor a 5000 ya que se le resta 5000
```
from scapy.all import *

packages = rdpcap('capture.pcap')

flag=""
for p in packages:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag += chr(p[UDP].sport - 5000)

print(flag)
```


```
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```
