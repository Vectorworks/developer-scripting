# GetTextStyle

## Description
Procedure GetTextStyle returns the text style at a specified position within the referenced text object.

The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

{| class="wikitable_c"
|+ Table - Text Style
! Style !! Constant
|-
| Plain
| style="text-align:center"| 0
|-
| Bold
| style="text-align:center"| 1
|-
| Italic
| style="text-align:center"| 2
|-
| Underline
| style="text-align:center"| 4
|-
| Outline
| style="text-align:center"| 8
|-
| Shadowed
| style="text-align:center"| 16
|-
| Superscript (VW 2011+)
| style="text-align:center"| 32
|-
| Subscript (VW 2011+)
| style="text-align:center"| 64
|}

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
