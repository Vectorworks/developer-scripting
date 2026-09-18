# GetPlantToolInitialized

## Description
Returns whether or not the plant tool has been initialized or not.

```pascal
FUNCTION GetPlantToolInitialized : BOOLEAN;
```

```python
def vs.GetPlantToolInitialized():
    return BOOLEAN
```

## Examples
```pascal
resultOK := GetPlantToolInitialized;
```
```python
import vs

# Returns whether or not the plant tool has been initialized or not.
ok = vs.GetPlantToolInitialized()
if ok:
    vs.Message('GetPlantToolInitialized succeeded')
else:
    vs.Message('GetPlantToolInitialized failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Utility](../Categories/Utility.md)
