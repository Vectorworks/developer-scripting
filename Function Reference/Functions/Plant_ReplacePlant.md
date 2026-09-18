# Plant_ReplacePlant

## Description
Replaces a the currently selected plant

```pascal
PROCEDURE Plant_ReplacePlant(plantToReplace : HANDLE);
```

```python
def vs.Plant_ReplacePlant(plantToReplace):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plantToReplace|HANDLE|   |

## Examples
```pascal
Plant_ReplacePlant(plantToReplace);
```
```python
import vs

# Replaces a the currently selected plant.
plantToReplace = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Plant_ReplacePlant(plantToReplace)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
