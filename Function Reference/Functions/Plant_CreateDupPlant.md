# Plant_CreateDupPlant

## Description
Creates a new plant from the currently selected plant

```pascal
PROCEDURE Plant_CreateDupPlant(plantToCreateFrom : HANDLE);
```

```python
def vs.Plant_CreateDupPlant(plantToCreateFrom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plantToCreateFrom|HANDLE|   |

## Examples
```pascal
Plant_CreateDupPlant(plantToCreateFrom);
```
```python
import vs

# Creates a new plant from the currently selected plant.
plantToCreateFrom = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Plant_CreateDupPlant(plantToCreateFrom)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
