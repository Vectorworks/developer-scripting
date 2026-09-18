# ComponentVolume

## Description
Returns the total 3D volume of the specified component, minus any holes in the 3D object.

```pascal
FUNCTION ComponentVolume(
				c     : CRITERIA;
				index : INTEGER): REAL;
```

```python
def vs.ComponentVolume(c, index):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|The search criteria string.|
|index|INTEGER|The index of the component.|

## Examples
```pascal
resultVal := ComponentVolume(c, 1);
```
```python
import vs

# Returns the total 3D volume of the specified component, minus any holes in
# the 3D object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects
index = 1

vol = vs.ComponentVolume(c, index)
vs.Message('ComponentVolume returned: ' + str(vol))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
