# IsTextStyleByClassN

## Description
IsTextStyleByClassN returns whether the class text style is used at a specified position within the text object.

```pascal
FUNCTION IsTextStyleByClassN(
				objectId : HANDLE;
				position : INTEGER): BOOLEAN;
```

```python
def vs.IsTextStyleByClassN(objectId, position):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to text object|
|position|INTEGER|Position in text string, zero-based.|

## Examples
```pascal
resultOK := IsTextStyleByClassN(objectId, 1);
```
```python
import vs

# IsTextStyleByClassN returns whether the class text style is used at a
# specified position within the text object.
objectId = vs.FSActLayer()  # handle to the first selected object on the active layer
position = 1

ok = vs.IsTextStyleByClassN(objectId, position)
if ok:
    vs.Message('IsTextStyleByClassN succeeded')
else:
    vs.Message('IsTextStyleByClassN failed')
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
