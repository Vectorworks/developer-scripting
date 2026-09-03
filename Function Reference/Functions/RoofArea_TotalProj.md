# RoofArea_TotalProj

## Description
Returns the total area projected on the ground plane of roofs or roof faces that meet the criteria.

```pascal
FUNCTION RoofArea_TotalProj(c : CRITERIA): REAL;
```

```python
def vs.RoofArea_TotalProj(c):
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
resultVal := RoofArea_TotalProj(c);
```
```python
import vs

# Returns the total area projected on the ground plane of roofs or roof faces
# that meet the criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

area = vs.RoofArea_TotalProj(c)
vs.Message('RoofArea_TotalProj returned: ' + str(area))
```

## See Also
* [RoofArea Heated](RoofArea_Heated.md)
* [RoofArea HeatedProj](RoofArea_HeatedProj.md)
* [RoofArea Total](RoofArea_Total.md)

## Version
Availability: from Vectorworks 14.0

## Category
* [Criteria](../Categories/Criteria.md)
