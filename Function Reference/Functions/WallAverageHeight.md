# WallAverageHeight

## Description
Returns the average height of walls, including wall peaks and different starting and ending heights.

```pascal
FUNCTION WallAverageHeight(c : CRITERIA): REAL;
```

```python
def vs.WallAverageHeight(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := WallAverageHeight(c);
```
```python
import vs

# Returns the average height of walls, including wall peaks and different
# starting and ending heights.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.WallAverageHeight(c)
vs.Message('WallAverageHeight returned: ' + str(value))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Criteria](../Categories/Criteria.md)
