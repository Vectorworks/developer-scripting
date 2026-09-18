# SlabThickness

## Description
Returns the thickness of slab objects that meet the criteria.

```pascal
FUNCTION SlabThickness(c : CRITERIA): REAL;
```

```python
def vs.SlabThickness(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|   |

## Examples
```pascal
resultVal := SlabThickness(c);
```
```python
import vs

# Returns the thickness of slab objects that meet the criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.SlabThickness(c)
vs.Message('SlabThickness returned: ' + str(value))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Criteria](../Categories/Criteria.md)
