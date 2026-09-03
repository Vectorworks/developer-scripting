# GetPlantToolSpacing

## Description
This returns the spacing that is currently stored in the plant tool.

```pascal
FUNCTION GetPlantToolSpacing : REAL;
```

```python
def vs.GetPlantToolSpacing():
    return REAL
```

## Examples
```pascal
resultVal := GetPlantToolSpacing;
```
```python
import vs

# This returns the spacing that is currently stored in the plant tool.
value = vs.GetPlantToolSpacing()
vs.Message('GetPlantToolSpacing returned: ' + str(value))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Utility](../Categories/Utility.md)
