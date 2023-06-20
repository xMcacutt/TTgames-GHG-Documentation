# GHG

## File Header

|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword|File Size|Inclusive|
|0x8|Dword|||
|0xC|Dword*|Pointer Usually To 0x90||
|0x10|Dword|||
|0x14|Dword*|Pointer To Section B?||
|0x1C|Dword*|||
|0x20|Dword*|Pointer To Section C?||
|0x24|Dword*|???||
|0x30|Dword*|Pointer To String Table||
|0x34|Dword|String Table Length||
|0x4C|Dword*|Pointer To Layer Data||
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

### Layer Data
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword*|Pointer To Name||

#### Subsection A
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0xC|Dword*|Pointer To First Strip List||

### Geom
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword*|Pointer To Next Geom|0x0 If Last Geom|
|0x4|Dword|Geom ID||
|0xC|Dword*|Pointer To Strip List||

|---|---|---|---|
|0x0|Dword|Strip ID?|Always x00 x00 x07 x10|
|0x8|Dword|???|Always x08 x01 x00 x01|
|0x10|Dword|??? ID|Always x04 x00 x08 x30|
|0x14|Word|!!!||
|0x1C|Word|||
|0x1E|Word|||
|0x20|Dword|??? ID|Always x04 x00 x08 x30|
|0x24|Word|!!!||
|0x2C|Word|||
|0x2E|Word|||
|0x33|Byte|Always 0x50||
|0x34|Word|Offset To Strip Data From Start Of Strip List Excluding Strip List Header||

### Strip Header
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Byte|Strip Data Length|When Multiplied By 0x10|
|0x2|Word|???|Always x06 x60|
|0x8|Byte[4]|???|Bools|

#### Strip
##### Strip Chunk
|Offset|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x00|Dword|Chunk ID|Always xD2 x80 x01 x6C|
|0x04|Byte|???||
|0x05|Byte|???|Always x80|
|0x08|Qword|???|Always x00 x40 x02 x30 x12 x05 x00 x00|
|0x14|Dword|???|Always x02 x80 x01 x6D|
|0x18|Word|???|Always 4 times 0x4|
|0x1A|Word|???|Always x01|
|0x20|Word|???|Always x04 x02 or x03 x01|
|0x22|Word|???|Always x00 x01|
|0x24|Word|???|Always x03 x80|
|0x26|Byte|Chunk Float Count||
|0x27|Byte|???|Always x6C|
