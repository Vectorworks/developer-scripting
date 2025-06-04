# GetCharColor

## Description
Function GetCharColor returns the color of a character at a specified position in the given text object.<BR>
The position is in a range between 0 and 32767, representing a character position in the text string. An index of 0 refers to the first character in the string.

```pascal
PROCEDURE GetCharColor(
				theText   : HANDLE;
				position  : INTEGER;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetCharColor(theText, position):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle of the text object|
|position|INTEGER|Position of the character in the text string (0-based)|
|red|LONGINT|   |
|green|LONGINT|   |
|blue|LONGINT|   |

## See Also
VS Functions:
[GetCharFontIndex](GetCharFontIndex.md) 
| [GetCharSize](GetCharSize.md) 
| [GetCharStyle](GetCharStyle.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
