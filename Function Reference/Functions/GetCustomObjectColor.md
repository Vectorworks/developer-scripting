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
See the &lt;a href=http://www.vectorlab.info/index.php?title=Colors_in_VectorWorks_2008%2B&gt;VectorLab&lt;/a&gt; article for more info.

## Examples
stomObject}}

## See Also
VS Functions:
[SetCustomObjectColor](SetCustomObjectColor.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
