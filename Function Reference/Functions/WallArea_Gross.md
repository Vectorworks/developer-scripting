# WallArea_Gross

## Description
Returns the 2D gross surface area of walls that meet the criteria.

```pascal
FUNCTION WallArea_Gross(c : CRITERIA): REAL;
```

```python
def vs.WallArea_Gross(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := WallArea_Gross(c);
```
```python
import vs

# Returns the 2D gross surface area of walls that meet the criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

area = vs.WallArea_Gross(c)
vs.Message('WallArea_Gross returned: ' + str(area))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Criteria](../Categories/Criteria.md)
