# Plant_EditPlantDefRB

## Description
Updates the definition when the user edits a plant definition from the resource browser

```pascal
PROCEDURE Plant_EditPlantDefRB(plantToEdit : HANDLE);
```

```python
def vs.Plant_EditPlantDefRB(plantToEdit):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plantToEdit|HANDLE|   |

## Examples
```pascal
Plant_EditPlantDefRB(plantToEdit);
```
```python
import vs

# Updates the definition when the user edits a plant definition from the
# resource browser.
plantToEdit = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Plant_EditPlantDefRB(plantToEdit)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
