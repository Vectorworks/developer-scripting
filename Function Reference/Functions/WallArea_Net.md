# WallArea_Net

## Description
Returns the 2D gross surface area without doors and windows areas of walls that meet he criteria.

```pascal
FUNCTION WallArea_Net(c : CRITERIA): REAL;
```

```python
def vs.WallArea_Net(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := WallArea_Net(c);
```
```python
import vs

# Returns the 2D gross surface area without doors and windows areas of walls
# that meet he criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

area = vs.WallArea_Net(c)
vs.Message('WallArea_Net returned: ' + str(area))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Criteria](../Categories/Criteria.md)
