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
