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

## Examples
```pascal
Plant_UpdateTranslat(newSymbolName, oldID, newID, masterPlant, currentPlant);
```
```python
import vs

# Updates the plant record with the new ID.
newSymbolName = 'MySymbol'
oldID = 'Example'
newID = 'Example'
masterPlant = vs.FSActLayer()  # handle to the first selected object on the active layer
currentPlant = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.Plant_UpdateTranslat(newSymbolName, oldID, newID, masterPlant, currentPlant)
```

## Version
Availability: from Vectorworks 2014

## Category
* [PlantObjectCoreTools](../Categories/PlantObjectCoreTools.md)
