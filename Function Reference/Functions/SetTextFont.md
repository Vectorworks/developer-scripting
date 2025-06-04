# SetTextFont

## Description
Procedure SetTextFont sets the font of a substring in the referenced text object.

```pascal
PROCEDURE SetTextFont(
				objectHd : HANDLE;
				Start    : INTEGER;
				Count    : INTEGER;
				FontNum  : INTEGER);
```

```python
def vs.SetTextFont(objectHd, Start, Count, FontNum):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Start|INTEGER|Start position in text string.|
|Count|INTEGER|Length of substring.|
|FontNum|INTEGER|Font ID for substring.|

## Remarks
Note that "Start" is zero-based.

## Examples
#### VectorScript ####
```pascal
SetTextFont(handleToText,0,5,GetFontID('Helvetica'));

{sets the first five characters of the referenced text string to Helvetica}
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetFontID](GetFontID.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
