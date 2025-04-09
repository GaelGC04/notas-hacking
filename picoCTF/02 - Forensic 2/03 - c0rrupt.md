## Descripción
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

## Solución
Se descarga el archivo con wget
Se usa el comando file para ver que tipo es diciendo que es data
Se aprecia que está corrupto
Se checa el inicio del hexadecimal del archivo con el comando `xxd mystery | head`
Para arreglar el tipo se cambia el contenido de la primer fila con el comando `hexeditor mystery` por 
```
89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  49 48 44 52
```
Como el archivo aun no se puede abrir se instala el paquete pngcheck para ver los errores con el comando `pngcheck -v mystery` devolviendo:
```
chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
```
Se reparan los errores de tamaño y los nombres de chunks teniendo entonces:
```
00000000  89 50 4E 47  0D 0A 1A 0A   00 00 00 0D  49 48 44 52                                                                                .PNG........IHDR
00000010  00 00 06 6A  00 00 04 47   08 02 00 00  00 7C 8B AB                                                                                ...j...G.....|..
00000020  78 00 00 00  01 73 52 47   42 00 AE CE  1C E9 00 00                                                                                x....sRGB.......
00000030  00 04 67 41  4D 41 00 00   B1 8F 0B FC  61 05 00 00                                                                                ..gAMA......a...
00000040  00 09 70 48  59 73 00 00   16 25 00 00  16 25 01 49                                                                                ..pHYs...%...%.I
00000050  52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F                                                                                R$.....IDATx^..?
00000060  8E 64 CD 71  BD 2D 8B 20   20 80 90 41  83 02 08 D0                                                                                .d.q.-.  ..A....
00000070  F9 ED 40 A0  F3 6E 40 7B   90 23 8F 1E  D7 20 8B 3E                                                                                ..@..n@{.#... .>
```

Y una vez que se cambia el archivo a .png se abre y está la bandera

```
picoCTF{c0rrupt10n_1847995}
```
