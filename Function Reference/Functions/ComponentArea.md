# ComponentArea

## Description
Returns the area of one side of the specified component, minus any holes in the 3D object.

```pascal
FUNCTION ComponentArea(
				c     : CRITERIA;
				index : INTEGER): REAL;
```

```python
def vs.ComponentArea(c, index):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|The search criteria string|
|index|INTEGER|The index of the component.|

## Examples
```pascal
resultVal := ComponentArea(c, 1);
```
```python
import vs

# Returns the area of one side of the specified component, minus any holes in
# the 3D object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects
index = 1

area = vs.ComponentArea(c, index)
vs.Message('ComponentArea returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
