# Plant_GetToolSpacing

## Description
Gets the current spacing associated with the plant tool.

```pascal
FUNCTION Plant_GetToolSpacing : REAL;
```

```python
def vs.Plant_GetToolSpacing():
    return REAL
```

## Examples
```pascal
resultVal := Plant_GetToolSpacing;
```
```python
import vs

# Gets the current spacing associated with the plant tool.
value = vs.Plant_GetToolSpacing()
vs.Message('Plant_GetToolSpacing returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
