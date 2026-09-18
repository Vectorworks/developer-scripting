# RoofArea_HeatedProj

## Description
Returns the heated (interior) area projected on the ground plane of roofs or roof faces that meet the criteria.

```pascal
FUNCTION RoofArea_HeatedProj(c : CRITERIA): REAL;
```

```python
def vs.RoofArea_HeatedProj(c):
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
resultVal := RoofArea_HeatedProj(c);
```
```python
import vs

# Returns the heated (interior) area projected on the ground plane of roofs
# or roof faces that meet the criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

area = vs.RoofArea_HeatedProj(c)
vs.Message('RoofArea_HeatedProj returned: ' + str(area))
```

## See Also
* [RoofArea Heated](RoofArea_Heated.md)
* [RoofArea Total](RoofArea_Total.md)
* [RoofArea TotalProj](RoofArea_TotalProj.md)

## Version
Availability: from Vectorworks 14.0

## Category
* [Criteria](../Categories/Criteria.md)
