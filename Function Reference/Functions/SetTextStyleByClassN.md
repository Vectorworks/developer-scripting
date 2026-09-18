# SetTextStyleByClassN

## Description
SetTextStyleByClassN sets a specified substring of a text object to use the class text style. To undo this, use SetTextStyleRef or SetTextStyleRefN on the text.

```pascal
FUNCTION SetTextStyleByClassN(
				objectId : HANDLE;
				start    : INTEGER;
				count    : INTEGER): BOOLEAN;
```

```python
def vs.SetTextStyleByClassN(objectId, start, count):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to text object|
|start|INTEGER|Start position in text string, zero-based.|
|count|INTEGER|Length of substring.|

## Examples
```pascal
resultOK := SetTextStyleByClassN(objectId, 1, 2);
```
```python
import vs

# SetTextStyleByClassN sets a specified substring of a text object to use the
# class text style.
objectId = vs.FSActLayer()  # handle to the first selected object on the active layer
start = 1
count = 5

ok = vs.SetTextStyleByClassN(objectId, start, count)
if ok:
    vs.Message('SetTextStyleByClassN succeeded')
else:
    vs.Message('SetTextStyleByClassN failed')
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
