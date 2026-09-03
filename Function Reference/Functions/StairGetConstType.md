# StairGetConstType

## Description
<lineList ident=2>
<line>
Returns construction type of stair.
</line>

<line>
1: Solid
</line>
<line>
2: Stringer underneath
</line>
<line>
3: Stringer outside
</line>
<line>
4: Concrete 
</line>
<line>
5: CircularWithTangentialSteps /* Special type used by circular stairs only */
</line>
<line>
-1: Error
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>

</lineList>

```pascal
FUNCTION StairGetConstType(stair : HANDLE): INTEGER;
```

```python
def vs.StairGetConstType(stair):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Examples
```pascal
resultN := StairGetConstType(stair);
```
```python
import vs

# Returns construction type of stair.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.StairGetConstType(stair)
vs.Message('StairGetConstType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
