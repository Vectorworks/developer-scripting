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

## Examples
```pascal
GetCharColor(theText, 1, 2, 3, 10);
```
```python
import vs

# Function GetCharColor returns the color of a character at a specified
# position in the given text object.
theText = 'Example text'
position = 1

red, green, blue = vs.GetCharColor(theText, position)
vs.Message('GetCharColor returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
GetCharFontIndex
| GetCharSize
| GetCharStyle

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
