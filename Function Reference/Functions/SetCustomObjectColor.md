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

## Examples
```pascal
resultOK := SetCustomObjectColor(objectHand, 1, 2);
```
```python
import vs

# Store/Set an auxilary color index in 'objectHand' so GetCustomObjectColor
# can access it later.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer
inTagID = 1
inColoIndex = 1

ok = vs.SetCustomObjectColor(objectHand, inTagID, inColoIndex)
if ok:
    vs.Message('SetCustomObjectColor succeeded')
else:
    vs.Message('SetCustomObjectColor failed')
```

## See Also
VS Functions:
[GetCustomObjectColor](GetCustomObjectColor.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
