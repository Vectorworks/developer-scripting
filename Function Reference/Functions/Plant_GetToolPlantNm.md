# Plant_GetToolPlantNm

## Description
Gets the current plant that the tool has loaded.

```pascal
FUNCTION Plant_GetToolPlantNm : STRING;
```

```python
def vs.Plant_GetToolPlantNm():
    return STRING
```

## Examples
```pascal
resultStr := Plant_GetToolPlantNm;
```
```python
import vs

# Gets the current plant that the tool has loaded.
text = vs.Plant_GetToolPlantNm()
vs.Message('Plant_GetToolPlantNm returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
