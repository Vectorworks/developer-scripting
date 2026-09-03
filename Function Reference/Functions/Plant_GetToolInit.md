# Plant_GetToolInit

## Description
Returns true if the plant tool is initialized.

```pascal
FUNCTION Plant_GetToolInit : BOOLEAN;
```

```python
def vs.Plant_GetToolInit():
    return BOOLEAN
```

## Examples
```pascal
resultOK := Plant_GetToolInit;
```
```python
import vs

# Returns true if the plant tool is initialized.
ok = vs.Plant_GetToolInit()
if ok:
    vs.Message('Plant_GetToolInit succeeded')
else:
    vs.Message('Plant_GetToolInit failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
