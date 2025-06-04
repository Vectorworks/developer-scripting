# GetTextFont

## Description
Procedure GetTextFont returns the font of the referenced text object at a specified position in the string.

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

```pascal
FUNCTION GetTextFont(
				objectHd : HANDLE;
				Position : INTEGER): INTEGER;
```

```python
def vs.GetTextFont(objectHd, Position):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Examples
#### VectorScript ####
```pascal
fontID:=GetTextFont(handleToText,2);
```
#### Python ####
```python
fontID = vs.GetTextFont(handleToText,2)
```

## See Also
VS Functions:
[GetFontName](GetFontName.md) 
| [GetFontID](GetFontID.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
