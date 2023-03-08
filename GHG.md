# GHG

## File Header

|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword|File Size|Inclusive|
|0x8|Dword|||
|0xC|Dword*|Pointer Usually To 0x90||
|0x10|Dword|||
|0x90|Dword*|Pointer To Section A Header|

## Textures 

### Texture Header
32 Bytes Long
|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Word|||
|0x2|Word|||
|0x4|Dword|||
|0x8|Dword|||
|0xC|Dword|||

### Texture
TIM2 Headerless PQRS Format
|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Word|File Size|Inclusive|
|0x2|Word|||
|0x4|Dword|||
|0x8|Dword|||
|0xC|Dword|||

## Mesh

### Chunk Header
|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword|Chunk ID|Always xD2 x80 x01 x6C|
|0x4|Byte|???||
|0x5|Byte|???|Always x80|
|0x8|Qword|???|Always x00 x40 x02 x30 x12 x05 x00 x00|
|0x14|Dword|???|Always x02 x80 x01 x6D|
|0x18|Word|???|Always 4 times 0x4|
|0x1A|Word|???|Always x01|
|0x20|Word|???|Always x04 x02 or x03 x01|
|0x22|Word|???|Always x00 x01|
|0x24|Word|???|Always x03 x80|
|0x26|Byte|Chunk Float Count||
|0x27|Byte|???|Always x6C|
