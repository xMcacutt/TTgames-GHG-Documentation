# GHG

## File Header

|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword|File Size|Inclusive|
|0x8|Dword|||
|0xC|Dword*|Pointer Usually To 0x90||
|0x10|Dword|||
|0x14|Dword*|Pointer To Section B?||
|0x1C|Dword*|Pointer To Bones?||
|0x20|Dword*|Pointer To Section C?||
|0x24|Dword*|???||
|0x4C|Dword*|Pointer To Objects Header||
|0x90|Dword*|Pointer To Textures Header||

## Textures 

### Textures Header
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

## Objects

### Objects Header
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword*|Pointer To Object Name?||
|0x8|Dword*|Pointer To Start Of Subsection A||
|0x10|Dword*|???||

#### Subsection A
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0xC|Dword*|Pointer To First Strip List||

### Strip List Header
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword*|Pointer To Next Strip List Header|0x0 If Last List Header|
|0xC|Dword*|Pointer To Strip List||

### Strip List


### Chunk Header
|Offset|Data Type|Definition|Extra Information|
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
