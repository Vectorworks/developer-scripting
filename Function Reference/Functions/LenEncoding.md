# LenEncoding

## Description
Function LenEncoding returns the length of the specified string value in the specified encoding: 0 – mac; 1 – win; 2 – system; 3 – UTF8; 4 – UTF16

```pascal
FUNCTION LenEncoding(
				v        : DYNARRAY[] of CHAR;
				encoding : INTEGER): INTEGER;
```

```python
def vs.LenEncoding(v, encoding):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|DYNARRAY[] of CHAR|Source string.|
|encoding|INTEGER|0 – mac; 1 – win; 2 – system; 3 – UTF8; 4 – UTF16|

## Version
Availability: from Vectorworks 2018

## Category
* [Strings](../Categories/Strings.md)
