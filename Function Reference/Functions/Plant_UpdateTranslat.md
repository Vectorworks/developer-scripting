# Plant_UpdateTranslat

## Description
Updates the plant record with the new ID.

```pascal
PROCEDURE Plant_UpdateTranslat(
				newSymbolName : DYNARRAY[] of CHAR;
				oldID         : DYNARRAY[] of CHAR;
				newID         : DYNARRAY[] of CHAR;
				masterPlant   : HANDLE;
				currentPlant  : HANDLE);
```

```python
def vs.Plant_UpdateTranslat(newSymbolName, oldID, newID, masterPlant, currentPlant):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|newSymbolName|DYNARRAY[] of CHAR|   |
|oldID|DYNARRAY[] of CHAR|   |
|newID|DYNARRAY[] of CHAR|   |
|masterPlant|HANDLE|   |
|currentPlant|HANDLE|   |

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
