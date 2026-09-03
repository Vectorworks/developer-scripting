# Plant_ReplacePlantParam

## Description
Replaces plant parameters using information from replacement plant object.

```pascal
FUNCTION Plant_ReplacePlantParam(origPlantObj : HANDLE): HANDLE;
```

```python
def vs.Plant_ReplacePlantParam(origPlantObj):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|origPlantObj|HANDLE|   |

## Examples
```pascal
resultH := Plant_ReplacePlantParam(origPlantObj);
```
```python
import vs

# Replaces plant parameters using information from replacement plant object.
origPlantObj = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.Plant_ReplacePlantParam(origPlantObj)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
