# Plant_ResetPlantInst

## Description
Resets all instances of the plant symbol definition that is edited.

```pascal
PROCEDURE Plant_ResetPlantInst(plantSymbolName : DYNARRAY[] of CHAR);
```

```python
def vs.Plant_ResetPlantInst(plantSymbolName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|plantSymbolName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
Plant_ResetPlantInst(plantSymbolName);
```
```python
import vs

# Resets all instances of the plant symbol definition that is edited.
plantSymbolName = 'MySymbol'

vs.Plant_ResetPlantInst(plantSymbolName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
