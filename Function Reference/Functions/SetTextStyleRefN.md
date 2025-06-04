# SetTextStyleRefN

## Description
SetTextStyleRefN sets the text style of a specified substring of a text object to the referenced style. Reference 0 means Un-Styled. This procedure will replace by-class styling.

```pascal
FUNCTION SetTextStyleRefN(
				objectId     : HANDLE;
				start        : INTEGER;
				count        : INTEGER;
				textStyleRef : LONGINT): BOOLEAN;
```

```python
def vs.SetTextStyleRefN(objectId, start, count, textStyleRef):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to text object|
|start|INTEGER|Start position in text string, zero-based.|
|count|INTEGER|Length of substring.|
|textStyleRef|LONGINT|text style reference id|

## See Also
VS Functions:
[SetTextStyleRef](SetTextStyleRef.md) 
| [GetTextStyleRef](GetTextStyleRef.md) 
| [GetTextStyleRefN](GetTextStyleRefN.md) 
| [SetTextStyleByClass](SetTextStyleByClass.md) 
| [SetTextStyleByClassN](SetTextStyleByClassN.md) 
| [IsTextStyleByClass](IsTextStyleByClass.md) 
| [IsTextStyleByClassN](IsTextStyleByClassN.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
