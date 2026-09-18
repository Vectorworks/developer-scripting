# SetTextStyleByClass

## Description
SetTextStyleByClass sets the referenced object to use the class text style.  To undo this, use SetTextStyleRef on the object.

```pascal
PROCEDURE SetTextStyleByClass(objectId : HANDLE);
```

```python
def vs.SetTextStyleByClass(objectId):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to object|

## Examples
```pascal
SetTextStyleByClass(objectId);
```
```python
import vs

# SetTextStyleByClass sets the referenced object to use the class text style.
objectId = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetTextStyleByClass(objectId)
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
* [Object Attributes](../Categories/Object%20Attributes.md)
