# GetTextStyleRefN

## Description
GetTextStyleRefN returns the text style reference at a specified position within the text object. Reference 0 means Un-Styled.<BR>
<BR>
If the text object is using class text style, this returns the effective style.  You should use the *TextStyleByClass* functions to check and preserve by-class behavior.

```pascal
FUNCTION GetTextStyleRefN(
				objectId : HANDLE;
				position : INTEGER): LONGINT;
```

```python
def vs.GetTextStyleRefN(objectId, position):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to text object|
|position|INTEGER|Position in text string, zero-based.|

## Examples
```pascal
resultN := GetTextStyleRefN(objectId, 1);
```
```python
import vs

# GetTextStyleRefN returns the text style reference at a specified position
# within the text object.
objectId = vs.FSActLayer()  # handle to the first selected object on the active layer
position = 1

resultN = vs.GetTextStyleRefN(objectId, position)
vs.Message('GetTextStyleRefN returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetTextStyleRef](SetTextStyleRef.md) 
| [GetTextStyleRef](GetTextStyleRef.md) 
| [SetTextStyleRefN](SetTextStyleRefN.md) 
| [GetTextStyleRefN](GetTextStyleRefN.md) 
| [SetTextStyleByClass](SetTextStyleByClass.md) 
| [SetTextStyleByClassN](SetTextStyleByClassN.md) 
| [IsTextStyleByClass](IsTextStyleByClass.md) 
| [IsTextStyleByClassN](IsTextStyleByClassN.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
