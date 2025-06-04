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
