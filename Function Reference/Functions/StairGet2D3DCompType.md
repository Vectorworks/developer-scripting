# StairGet2D3DCompType

## Description
<lineList ident=2>
<line>
Returns 2D3D components type of stair.
</line>
<line>
1: 2D
</line>
<line>
2: Hybrid
</line>
<line>
-1: Error
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>
</lineList>

```pascal
FUNCTION StairGet2D3DCompType(stair : HANDLE): INTEGER;
```

```python
def vs.StairGet2D3DCompType(stair):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultN := StairGet2D3DCompType(stair);
```
```python
import vs

# Returns 2D3D components type of stair.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.StairGet2D3DCompType(stair)
vs.Message('StairGet2D3DCompType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021 SP3

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
