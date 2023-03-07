# GHG

## File Header

|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Dword|File Size|Inclusive|
|0x8|Dword|||
|0xC|Dword*|Pointer Usually To 0x90||
|0x10|Dword|||
|0x90|Dword*|Pointer To Section A Header|

## X Header
32 Bytes Long
|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Word|||
|0x2|Word|||
|0x4|Dword|||
|0x8|Dword|||
|0xC|Dword|||

## X
|Address|Data Type|Definition|Extra Information|
|---|---|---|---|
|0x0|Word|File Size|Inclusive|
|0x2|Word|||
|0x4|Dword|||
|0x8|Dword|||
|0xC|Dword|||
