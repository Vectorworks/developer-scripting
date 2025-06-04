# SetTextStyleRef

## Description
Procedure SetTextStyleRef sets the text style of an object to the referenced style. Reference 0 means Un-Styled.  This procedure will replace by-class styling.

```pascal
PROCEDURE SetTextStyleRef(
				objectId     : HANDLE;
				textStyleRef : LONGINT);
```

```python
def vs.SetTextStyleRef(objectId, textStyleRef):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to object|
|textStyleRef|LONGINT|text style reference id|

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
