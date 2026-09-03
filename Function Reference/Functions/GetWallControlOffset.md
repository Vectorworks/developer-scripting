# GetWallControlOffset

## Description
Returns the default wall control line offset value.

```pascal
FUNCTION GetWallControlOffset : REAL;
```

```python
def vs.GetWallControlOffset():
    return REAL
```

## Examples
```pascal
resultVal := GetWallControlOffset;
```
```python
import vs

# Returns the default wall control line offset value.
value = vs.GetWallControlOffset()
vs.Message('GetWallControlOffset returned: ' + str(value))
```

## Version
GetWallControlOffset is obsolete as of VectorWorks12.5<P>

Availability: from VectorWorks8.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
