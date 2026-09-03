# RoofArea_Total

## Description
Returns the total area along the slope of roofs or roof faces that meet the criteria.

```pascal
FUNCTION RoofArea_Total(c : CRITERIA): REAL;
```

```python
def vs.RoofArea_Total(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Remarks
\_c\_ (2016.06.28): See remark on [[VS:RoofArea Heated]].

## Examples
```pascal
resultVal := RoofArea_Total(c);
```
```python
import vs

# Returns the total area along the slope of roofs or roof faces that meet the
# criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

area = vs.RoofArea_Total(c)
vs.Message('RoofArea_Total returned: ' + str(area))
```

## See Also
* [RoofArea Heated](RoofArea_Heated.md)
* [RoofArea HeatedProj](RoofArea_HeatedProj.md)
* [RoofArea TotalProj](RoofArea_TotalProj.md)

## Version
Availability: from Vectorworks 14.0

## Category
* [Criteria](../Categories/Criteria.md)
