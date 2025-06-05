# GetTextStyle

## Description
Procedure GetTextStyle returns the text style at a specified position within the referenced text object.

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

**Table - Text Style**

| Style                | Constant |
|----------------------|----------|
| Plain                | 0        |
| Bold                 | 1        |
| Italic               | 2        |
| Underline            | 4        |
| Outline              | 8        |
| Shadowed             | 16       |
| Superscript (VW 2011+)| 32      |
| Subscript (VW 2011+) | 64       |

```pascal
FUNCTION GetTextStyle(
				TextHd   : HANDLE;
				Position : INTEGER): INTEGER;
```

```python
def vs.GetTextStyle(TextHd, Position):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|Position|INTEGER|Position in text string.|

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
