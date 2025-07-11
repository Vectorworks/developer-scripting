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

## See Also
VS Functions:
[SetCustomObjectColor](SetCustomObjectColor.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
