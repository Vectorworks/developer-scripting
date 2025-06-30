# SetCustomObjectColor

## Description
Store/Set an auxilary color  index  in 'objectHand' so GetCustomObjectColor  can access it later.  Application will preserve the color mapped to inTagID.

```pascal
FUNCTION SetCustomObjectColor(
				objectHand  : HANDLE;
				inTagID     : INTEGER;
				inColoIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetCustomObjectColor(objectHand, inTagID, inColoIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|
|inTagID|INTEGER|   |
|inColoIndex|INTEGER|   |

## Remarks

## See Also
VS Functions:
[GetCustomObjectColor](GetCustomObjectColor.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
