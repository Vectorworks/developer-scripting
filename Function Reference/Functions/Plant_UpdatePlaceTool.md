# Plant_UpdatePlaceTool

## Description
Updates the place plant tool when plant is double clicked from resource browser

```pascal
PROCEDURE Plant_UpdatePlaceTool(plantToUpdateWith : HANDLE);
```

```python
def vs.Plant_UpdatePlaceTool(plantToUpdateWith):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plantToUpdateWith|HANDLE|   |

## Examples
```pascal
Plant_UpdatePlaceTool(plantToUpdateWith);
```
```python
import vs

# Updates the place plant tool when plant is double clicked from resource
# browser.
plantToUpdateWith = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Plant_UpdatePlaceTool(plantToUpdateWith)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
