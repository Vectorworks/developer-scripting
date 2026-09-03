# WallThickness

## Description
Returns the thickness of walls that meet the criteria.

```pascal
FUNCTION WallThickness(c : CRITERIA): REAL;
```

```python
def vs.WallThickness(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := WallThickness(c);
```
```python
import vs

# Returns the thickness of walls that meet the criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.WallThickness(c)
vs.Message('WallThickness returned: ' + str(value))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Criteria](../Categories/Criteria.md)
