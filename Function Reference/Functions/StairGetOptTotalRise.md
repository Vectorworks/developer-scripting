# StairGetOptTotalRise

## Description
<lineList ident=2>
<line>
Returns Stair Total Rise Option.
</line>
<line>
0: By value
</line>
<line>
1: By layer elevation
</line>
<line>
-1: Error
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>
</lineList>

```pascal
FUNCTION StairGetOptTotalRise(stair : HANDLE): INTEGER;
```

```python
def vs.StairGetOptTotalRise(stair):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultN := StairGetOptTotalRise(stair);
```
```python
import vs

# Returns Stair Total Rise Option.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.StairGetOptTotalRise(stair)
vs.Message('StairGetOptTotalRise returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
