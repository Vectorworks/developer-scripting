# IsTextStyleByClass

## Description
Procedure IsTextStyleByClass returns whether the class text style is used for the referenced object.
[Dieter@DWorks]: This doesn't seem to be working on polygons. I assume this only works on text objects?

```pascal
FUNCTION IsTextStyleByClass(objectId : HANDLE): BOOLEAN;
```

```python
def vs.IsTextStyleByClass(objectId):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectId|HANDLE|handle to object|

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
