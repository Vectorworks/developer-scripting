# IFC_SetStructureGUID

## Description
Sets specified GUID.

```pascal
FUNCTION IFC_SetStructureGUID(
				guidType  : INTEGER;
				iBuilding : INTEGER;
				iStorey   : INTEGER;
				Guid      : STRING): BOOLEAN;
```

```python
def vs.IFC_SetStructureGUID(guidType, iBuilding, iStorey, Guid):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|guidType|INTEGER|   |
|iBuilding|INTEGER|   |
|iStorey|INTEGER|   |
|Guid|STRING|   |

## Version
Availability: from Vectorworks 2024

## Category
* [IFC](../Categories/IFC.md)
