# PerimN

## Description
Returns the perimeter of an object. If more than one object matches the search criteria, the function will return the sum of the matching objects' perimeters.

```pascal
FUNCTION PerimN(c : CRITERIA): REAL;
```

```python
def vs.PerimN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
PerimValue := PerimN(C='Fence');
{returns the total perimeter of all objects in the class 'Fence'}
```

```pascal
resultVal := PerimN(c);
```
```python
import vs

# Returns the perimeter of an object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.PerimN(c)
vs.Message('PerimN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
