# Plant_GetToolPlcMode

## Description
Gets the current placement mode associated with the plant tool.

```pascal
FUNCTION Plant_GetToolPlcMode : INTEGER;
```

```python
def vs.Plant_GetToolPlcMode():
    return INTEGER
```

## Examples
```pascal
resultN := Plant_GetToolPlcMode;
```
```python
import vs

# Gets the current placement mode associated with the plant tool.
resultN = vs.Plant_GetToolPlcMode()
vs.Message('Plant_GetToolPlcMode returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
