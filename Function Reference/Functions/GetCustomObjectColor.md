# GetCustomObjectColor

## Description
Get an auxilary color index stored in'objectHand' previously  with SetCustomObjectColor .  Aplication will preserve the color mapped to inTagID.

```pascal
FUNCTION GetCustomObjectColor(
				objectHand        : HANDLE;
				inTagID           : INTEGER;
				VAR outColorIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetCustomObjectColor(objectHand, inTagID):
    return (BOOLEAN, outColorIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|
|inTagID|INTEGER|   |
|outColorIndex|INTEGER|   |

## Remarks

## Examples
[CustomObject](examples/CustomObject.md)

```pascal
resultOK := GetCustomObjectColor(objectHand, 1, 2);
```
```python
import vs

# Get an auxilary color index stored in'objectHand' previously with
# SetCustomObjectColor.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer
inTagID = 1

ok, outColorIndex = vs.GetCustomObjectColor(objectHand, inTagID)
vs.Message('GetCustomObjectColor returned: ' + str((ok, outColorIndex)))
```

## See Also
VS Functions:
[SetCustomObjectColor](SetCustomObjectColor.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
