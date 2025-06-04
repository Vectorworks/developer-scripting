# Ord

## Description
Function Ord returns the corresponding ASCII number of the specified character value. Parameter Ord specifies the character.

```pascal
FUNCTION Ord(v : CHAR): INTEGER;
```

```python
def vs.Ord(v):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|CHAR|ASCII character.|

## Remarks
The encoding used is Apple MacRoman. This leads to a number of troubles if you are on Windows and use characters above ASCII 128.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Main;
VAR
str :STRING;
cnt :INTEGER;
BEGIN
str := GetText(FSActLayer);
FOR cnt := 1 TO Len(str) DO
AlrtDialog(Concat(Ord(Copy(str, cnt, 1))));
END;
RUN(Main);
```
==== Python ====
```python

```

## See Also
VS Functions:
[Chr](Chr.md)

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
